# Configuration

There is a limited number of configuration options in fs_renderer/local_settings.py

##Plugins

PLUGINS is a dictionary matching plugin name to a plugin class.

TESTING is a boolean which if set to True will add HTML header and footer to the templates along aith a submit button for testing.  This is set for each section object and can be used in the templates to show html you would only like to show in testing.  This is done in the following way:

```
    {% if section.testing %}
        <p>Some additional code, can be anything, javascript, styling etc.</p>
    {% endif %}
```

CUSTOM is set to False by deafult but if set to True will use the CustomApplication object in fs_renderer/custom_logic.py.  Recently a new requirement to possibly load multiple XML files will require a change in this style.  Application objects can be loaded per request for different XML files or instantiated at startup and reused.  This is not set up by deafult.

XML_FILE is set to point to Questionnaire XML file as the application objects instantiated in the views depend on it.  The new requirement of having to load multiple XML files may make it redundant.




