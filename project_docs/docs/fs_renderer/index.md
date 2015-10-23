# Forms System Renderer Extension

* [https://github.com/cam-mrc-epid/fs_api2](https://github.com/cam-mrc-epid/fs_api2)
* [https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/fs_api2/](https://svn.mrc-epid.cam.ac.uk/private/MRC_Webforms_Python/fs_api2/)

## Introduction

This system uses Form System XML and connects to the Forms System Questionnaire database to provide extra functionality for the system.   

It uses the Django Web Framework to provide this functionality.  The Questionnaire models are provided by the django-fsq package and the xml objects by the XML Objectifier package. 

##Features
It provides...

- builtin rendering of Forms System XML 
- ability to extend functionality using a plugin architecture.  

##History

The Forms System Renderer Extension is a stripped down version of the oirginal project stripped down to isolate the functionality solely suited for the use of the Questionnaire models.






