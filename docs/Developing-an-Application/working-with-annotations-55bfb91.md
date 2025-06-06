<!-- loio55bfb91591d84f658e6c9474a3c657c4 -->

# Working with Annotations



<a name="loio55bfb91591d84f658e6c9474a3c657c4__section_ogs_rr5_hrb"/>

## Overview of Annotations

Local annotation files are created directly in the project. When you generate a project using SAP Fiori tools, one local annotation file gets generated in the `webapp/annotations` folder and is automatically registered in the `manifest.json` file. You can also [create additional annotation](overriding-annotations-2f1bb9c.md#loio2f1bb9ce466b4e6fac37431f1343b95d__SM_CREATING_ANNOT_FILE) files as needed using the annotation file manager or [Maintaining Annotation-Based Elements](maintaining-annotation-based-elements-a524d8a.md).

The service metadata and back end annotation files \(if any\) are copied and stored in the `webapp/localService` folder during the project generation. The reference to these local copies are maintained in `manifest.json` using the `localUri`, whereas the `uri` parameter contains the relative path to these sources in the back end. For more information about back end annotation, see [Visualizing Annotations with Service Modeler](visualizing-annotations-with-service-modeler-58784b5.md).

It is important to define new annotation terms in the local annotation file of your project, as all the changes made in local copies of back end annotation file or metadata do not have an impact on the deployed application. If you need to change the annotation defined in the back end, you need to copy this annotation along with the target and qualifier to the local annotation file and adjust it there. For more information, see [Overriding backend Annotations](overriding-annotations-2f1bb9c.md). The annotation terms defined in the local annotation file will always win over the same annotation with the same qualifier and applied to the same target in the back end sources. The overriding sequence of multiple local annotation files is defined in the `manifest.json` file and can be viewed and changed in the annotation manager. For more information, see [Visualizing Annotations with Service Modeler](visualizing-annotations-with-service-modeler-58784b5.md) - **How to change the hierarchy of local annotation file** section.

You can either maintain your local annotations using the XML annotation language server or you can use the support in the Page Editor for a more schematic view. For more information, see [Maintaining Annotation-Based Elements](maintaining-annotation-based-elements-a524d8a.md).

> ### Note:  
> Maintaining local annotation files with Service Modeler is only applicable to theOData service, not CAP CDS.

