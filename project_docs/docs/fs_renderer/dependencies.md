#Project Dependencies

arrow==0.6.0 # used in custom_logic example

bunch==1.0.1 # installed by XML Objectifier

diff-match-patch==20121119 # django-import-export dependency

Django==1.7.5

django-extensions==1.5.7 # debugging extension, can be removed for production.

-e git://github.com/davidgillies/django-fsq@cca77b4599366953fc523bf4f58acbd35d052067#egg=django_fsq-master # specific commit of the Django FSQ app.

django-import-export==0.2.8 # dependency of the Django FSQ app.

lxml==3.4.4 # dependency of the XML Objectifier

PyMySQL==0.6.6 # Required to connect to MySQL database

python-dateutil==2.4.2 # dependency of arrow

six==1.9.0 # dependency of django-extensions, can be removed for production

tablib==0.10.0 # dependency of django-import-export
-e git://github.com/davidgillies/xml-objectifier@dd41d57dfbb57b9bad85a0e6f110f3837508b3bd#egg=xml_objectifier-master # used to provide inital Application models, subclassed is fs_renderer/fs_apps.py