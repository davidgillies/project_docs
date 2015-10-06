# Project Documentation

##Installation

Set up a local virtualenv in a selected directory.

    virtualenv .

Activate the environment

    Scrits\activate

Download or clone the files from the relevant project from the repository e.g.

    git clone https://github.com/davidgillies/fs_api

The structure looks like:
fs_api/ # Git repo root includes .gitignore, and README.md
    .gitignore # a file list what git should not add to the repo
    README.md 
    requirements.txt # a list of requirements that pip will install.
    fs_proj/ # Project root contains manage.py, apps
        manage.py #
        fs_proj/ # Project Settings root the projects settings
        fs_renderer/ # A project is made up of apps.
        xmlfiles/ # a place for the xml files.

Go into the Git repo root, e.g.

    cd fs_api

Now install the project requirements

    pip install -r requirements.txt

Note in some cases you may receives admin required warnings on Windows, just click `cancel` if they come up.

Most of the requirements will be installed in your virtualenv's lib/site-packages directory.  If any of the requirements are installed from git repos they may be installed in a src directory in your virtualenv's root beside the lib directory.

If you need to make changes to installed code it is best to fork the code yourself, don't edit it in the lib folder.  The src folder contain git checkouts of the installed app code and you can manage these apps from this place as they are attached to git.


