#Extending the Renderer

There are a number of ways of extending the functionality of the renderer.  

##Subclassing

You can subclass the Application class (fs_renderer/fs_apps.py) and override functionality there.  There is an example file in the app (fs_renderer/custom_logic.py).  The initial development of this expected a single XML file per app so a custom class could be written and used for that app and the CUSTOM variable set to True (fs_renderer/local_settings.py).  This is set to False by default.  

More recent requirements suggested that multiple XML files may be used in a single app.  Therefore it may be necessary to change this approach by having a custom class per XML file and loading them in the views as necessary.  For custom functionality it may be easier to use the plugins architecture.

##Plugins

Plugins arose from the need to have extra functionality in the section interfaces that required the interface to build an unknown number of rows etc. or any more complicated interface that would be difficult to describe in the XML.  

They can be set up as follows:

In the XML you can replace a section, question group or question with a plugin by using the rendering hint:

```xml
                <epi:renderingHint>
                    <epi:rhType>plugin</epi:rhType>
                    <epi:rhData>some_plugin</epi:rhData>
                </epi:renderingHint>
```

where the `some_plugin` is the name of your plugin.  

Now register the plugin in fs_renderer/local_settings.py

```
PLUGINS = {'childlist': ChildList, 'some_plugin': SomePlugin}
```

where the key 'some_plugin' is the name you used in the XML and SomePlugin is a class you will create in fs_renderer/plugins.py.

In fs_renderer/plugins.py you build a plugin class e.g.

```
class SomePlugin():
    def __init__(self, data, caller):
        self.data = data
        self.caller = caller # 
        if isinstance(caller,fs_apps.Question):
            self.template = 'fs_renderer/some_plugin_q.html'
        else:
            self.template = 'fs_renderer/some_plugin.html'

    def do_it(self):
        if isinstance(self.caller,fs_apps.Question):
            results = Results.objects.filter(var_name__startswith='child_age')
            tally = 0
            number = 0
            for result in results:
                if result.var_value != '':
                    tally = tally + int(result.var_value)
                    number = number + 1
            average = tally/number        
            return average
        if isinstance(self.caller,fs_apps.QuestionGroup):
            profile = {}
            profile['name'] = self.caller.title
            profile['type'] = 'QuestionGroup'
            profile['position'] = self.caller.position
            profile['section'] = self.caller.section.title
            return profile
```

In this example the plugin class SomePlugin accepts two arguments data and caller.  data is a dictionary pulled from the questionnaire database relating to the participant and their data for the questionnaire they are completing.  The caller is the section, question group or question that the plugin will replace.  This example will return different things based on the type of caller it receives.   

A plugin must set a template that will be used to render the plugin.  The plugin instance will be passed to the template so the template can access its properties and methods directly.

An example template in this case would be fs_renderer/templates/fs_renderer/some_plugin.html:

```html
<div>
    <ul>
        <li>{{ question_group.plugin.do_it.name }}</li>
        <li>{{ question_group.plugin.do_it.type }}</li>
        <li>{{ question_group.plugin.do_it.position }}</li>
        <li>{{ question_group.plugin.do_it.section }}</li>
    </ul>
</div>
```
This plugin is for question groups and must use question_group.plugin to run its plugin methods.  Likewise it would be question.plugin for a question and section.plugin for a section.

You can import models from any app to use in the plugins and therefore can access different databases via their models.  You can use any python module available to do processing.
