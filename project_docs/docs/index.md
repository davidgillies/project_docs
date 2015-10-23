# Project Documentation

These docs cover the different parts of the project.

Docs have white boxes that denote code that can be run either at prompts or as scripts. 

It can be a pain to manage multiple virtualenvs but it is possible to set up desktops shortcuts to take the pain away! [Desktop Shortcuts](tips/shortcuts.md)

##Projects

###XML Objectifier
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/xml_objectifier](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/xml_objectifier)
* [https://github.com/cam-mrc-epid/xml-objectifier](https://github.com/cam-mrc-epid/xml-objectifier)

This is a base package that the XML Editor prototype and the Form System HTML Renderer Extension are based on.  It converts XML files into an object structure.

###XML Editor - Django-Q-Tree
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/django-q-tree](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/django-q-tree)
* [https://github.com/cam-mrc-epid/django-q-tree](https://github.com/cam-mrc-epid/django-q-tree)

Converts the XML into an object structure that can allow importing and exporting of XML files.

###Django FSQ - Questionnaire Models for Django
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/django-dsq](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/django-dsq)
* [https://github.com/cam-mrc-epid/django-fsq](https://github.com/cam-mrc-epid/django-fsq)

Questionnaire Models.  A set of django models that can be used to connect to the Form System Database.  It also illustrative of a potential multi database approach where an app can be set up to match an existing database then easily installed in multiple projects allowing reuse of the connection to the database. 

###Form System HTML Renderer Extension
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/fs_api2](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/fs_api2)
* [https://github.com/cam-mrc-epid/fs_api2](https://github.com/cam-mrc-epid/fs_api2)

A version of the HTML Renderer that uses the Django FSQ Questionnaire models.

###Python Notebooks
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/python_notebooks](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/python_notebooks)
* [https://github.com/cam-mrc-epid/python_notebooks](https://github.com/cam-mrc-epid/python_notebooks)

A set of python notebooks to help newbies to Python experiment and learn the basics.  

If you click on your Start Menu on Windows and select 'All Programs', click on the Anaconda folder, then click on IPython (Py 2.7) Notebook.  This will start a command prompt screen, just ignore it, then it will start a tab in your browser with a folder and file listing.  

The choice of this location is noted in the properties of the shortcut.  You can instead right click on the IPython (Py 2.7) Notebook shortcut in the menu and select properties, you can then change this location if you wish by editing the 'Start in' line.

You can download the notebooks for the documentation to your directory from **[here](https://github.com/davidgillies/python_notebooks)**.  Click 'Download ZIP' button to get the lot and extract them to the folder inside the target folder iPython ntoebooks is using.  That will make it easy for you to navigate to them in the notebooks interface.    

##Web Dev with Django videos
The videos require a Raven login.  Access is restricted by an Access Control List setup for the collection.  Unfortunately access is setup on a per-video basis.  Currently access is available to Adam Dickinson, David Vaughan, Anna Melachrou, Jasmine Morris and Inge Loudon.

[Web Dev with Django Collection](http://www.sms.cam.ac.uk/collection/2049733)

[Projects Collection](http://sms.cam.ac.uk/collection/2094754)
