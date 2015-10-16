#Usage

To load an XML file as objects

    from xml_objectifier.objectifier import Application
    my_app = Application('some name', 'somepath/somewhere/FamHist.xml')
    section_obj = my_app.get_section(section_number) # uses position
    qg = section_obj.get_question_group(question_group_number) # uses position
    q = question_group.get_question(question_number) # uses position


The main purpose of this structure is to build a structure that can be passed to the templates and iterated over.  The brief was that a section, question_group or question must be able to be rendered separately.  So templates are rendered to use this structure in the Forms System Renderer extension.  See fs_renderer's views for more details.  