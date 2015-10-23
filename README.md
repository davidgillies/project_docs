# Project Documentation

These project docs will render in Github but can be converted to a pretty html website using MkDocs.  Probably best set up in a virtual environment with virutalenv.

    pip install mkdocs # 
    
Clone this repo:

    git clone https://github.com/cam-mrc-epid/project_docs
    
cd into the project_docs folder and

    mkdocs serve 
    
This will create a website and run it on localhost:8000.  

You can also build a full HTML site using:

    mkdocs build

This will create a folder called `site` which will contain all the files for a website.  You can then copy then to a normal webserver doucment root such as Apache.

