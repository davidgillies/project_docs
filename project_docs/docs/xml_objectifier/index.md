# XML Objectifier

This package is hosted at:


This package does the basic conversion of XML into an object structure of sections, question groups and questions.  It was separated out from the main project so it could be used in other projects.  It is ued in the XML Editor and the Forms System Renderer extension.  

The structure is

* Aplication class - The main class is a container object for the sections, it represents the complete XML file.
* Section class - This class conatins question groups and properties about itself.
* Question Group class - This contains Question and TextNodes as well as having properties relevant to itself.
* Question class 
* TextNode - These are just instances of a Bunch.  A Bunch is class that extends a simple python dictionary so that keys can be accessed using standard python object notation e.g. `my_thing.myproperty` rather than the standard dictionary key `mything['myproperty']`.  This allows looping through a mixture of textnodes and other objects without having to use other notations.
* MethodMixin - a support class that provides shared functionality and some extra passing functions that allow looping through mixed objects without errors. 
