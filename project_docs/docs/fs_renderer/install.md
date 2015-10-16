# Project Documentation

##Installation

Set up a local virtualenv in a selected directory.

```sh
virtualenv .
```

Activate the environment

    Scripts\activate

Download or clone the files from the relevant project from the repository e.g.

```sh
git clone https://github.com/davidgillies/fs_api
```

The structure looks like:
<pre>
fs_api/ 
    .gitignore 
    README.md 
    requirements.txt 
    fs_proj/ 
        manage.py
        fs_proj/ 
        fs_renderer/
        xmlfiles/ 
</pre>

Go into the Git repo root, e.g.

```sh
cd fs_api
```

Now install the project requirements

```sh
pip install -r requirements.txt
```

Note in some cases you may receive admin required warnings on Windows, just click `cancel` if they come up.  Some modules want to install C modules for accelerating things but provide standard backups if they aren't installed.

Most of the requirements will be installed in your virtualenv's lib/site-packages directory.  If any of the requirements are installed from git repos they may be installed in a src directory in your virtualenv's root beside the lib directory.

If you need to make changes to installed code it is best to fork the code yourself, don't edit it in the lib folder.  The src folder contain git checkouts of the installed app code and you can manage these apps from this place as they are attached to git but you will likely have to make a few changes before git allows it.


