<!-- loioc5d62cabf74943ac901e23671bf756fa -->

# Adding Local Annotation Files

This guide describes how to add annotation files to an adaptation project.

<a name="task_afj_2f1_1fc"/>

<!-- task\_afj\_2f1\_1fc -->

## Adding Local Annotation Files from the Wizard



## Procedure

1.  Right click the `manifest.appdescr_variant` file of your adaptation project and select the *Adaptation Project* \> *Add Local Annotation File*.

2.  After the wizard starts, you may be asked to enter the credentials for the system that you created your adaptation project.

3.  From the *Target OData Service* dropdown, choose to which service from the manifest of the base application you want to add annotation file.

4.  Choose if you want to create an empty annotation file that you can edit later or to select already existing annotation file from a workspace.

5.  Click *Finish* to save your changes.


<a name="task_xt5_hf1_1fc"/>

<!-- task\_xt5\_hf1\_1fc -->

## Adding Local Annotation Files from the Adaptation Editor



## Procedure

1.  In Adaptation Editor, in mode *UI Adaptation*, select *Add Local Annotation File* from the *Object Page Quick Actions*.

2.  Save and reload the change using the *Save and reload* button in the header of the Adaptation Editor.

3.  The newly generated local annotation file is available in your *changes/annotations* folder in your adaptation project, in your workspace, in SAP Business Application Studio.


<a name="concept_uzv_zj1_1fc"/>

<!-- concept\_uzv\_zj1\_1fc -->

## Annotation LSP Support

Annotation LSP \(Language Service Provider\) support is now available for annotation files in adaptation projects. You can use the *SAP Fiori Tools – XML Annotation LSP* extension to add and edit annotations in the local annotation files.

More information about code assisting features offered by *SAP Fiori Tools – XML Annotation LSP* can be found in the topic [Maintaining Annotations with Language Server](Developing-an-Application/maintaining-annotations-with-language-server-6fc93f8.md).

