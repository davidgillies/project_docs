#Project Structure

Within the repository root the **fs_proj** folder is the Django project root.

**fs_proj/fs_proj** is the Django project settings folder containing settings and urls files.

**fs_proj/fs_proj/settings.py** is a standard settings file.  It contains a sample database connection for a MySQL database with the Forms System setup.  The key 'db3' is used by the **questionnaire** app's routers to connect to the MySQL database.  You need to change the settings to reflect your setup.  There is also a DATABASE_ROUTERS setting which points to the **questionnaire** app's router class (see Installation section). 

**fs_proj/fs_proj/urls.py** has the project urls.  They simply use /althtml/<section>/<question_group>/<question>/ style.  The original setup used /html hence /althtml was a later addition.  The urls, with the exception of the admin one all use the same view and pass the parts of the url as positional arguments to the same view class.

**fs_proj/fs_renderer** is the Django app.  The app is different from the standard Django app structure in that it imports the models from the *questionnaire* which is installed by the Django-FSQ package.  The questionnaire app provides its own admin screens for its models and also routers for the database (See Django FSQ docs.).  

**fs_proj/fs_renderer/fs_apps.py** contains the Application objects that reflect the XML file.  It is imported in the views.py file.

**fs_proj/fs_renderer/local_settings.py** contains the project settings (See configuration section).

**fs_proj/fs_renderer/plugins.py** contains some sample plugin classes and is the location for any plugin classes you need.

**fs_proj/fs_renderer/views.py** is a normal Django style views file using class based views.  These separate out GET and POST requests to use the class get() and post() methods.  

**fs_proj/fs_renderer/templates** conatins the app html templates.  These follow an include pattern as was necessary to allow question html to rendered on its own.

**fs_proj/xmlfiles** contains some example XML files.


