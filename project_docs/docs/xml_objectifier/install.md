#Installation

This is best installed inside a virtualenv where you are running your Django project but it will install anywhere.

    pip install git+git://github.com/davidgillies/xml_objectifier

##Dependecies

XML Objectifier's install process will install lxml and bunch.



##Issues

Installation problems maybe had with Canopy's version of python.  If you are using Canopy ,use Canopy's backported from python3 virtual environment venv rather than virtualenv.  This is due to install problems with the lxml package.