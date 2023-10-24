<!-- loioa524d8a307024c07ad59f2b73198ed63 -->

# Maintaining Annotation-Based Elements

> ### Note:  
> The annotation generation features within are *PageEditor* only supported for *List Report*, *Object Page*, and *Form Entry Object Page* applications based on the *OData V4* service. [Contact SAP Support](https://help.sap.com/viewer/1bb01966b27a429ebf62fa2e45354fea/Latest/en-US/5b5d9dc53aac46b69caebb95c1a242eb.html "") :arrow_upper_right: if any issue occurred. We rely on your feedback.

> ### Note:  
> The feature is provided since version 1.4.1 of the application modeler and [@sap/ux-specification](https://www.npmjs.com/package/@sap/ux-specification) versions 1.84.25 and 1.90.14.

Application modeler provides the possibility to develop your application UI in a schematic view. In a [Configure Page Elements](configure-page-elements-047507c.md), you see the basic structure outline of your page layout. You can add, remove, and modify properties of different page elements without knowing which annotations are used for that. The respective annotations are created and updated automatically in the local annotation file.

For example, you can add a section to the *Object Page* or *Form Entry Page* using the [\+\] button on the `Sections` node and a new `UI.FieldGroup` record is automatically generated and referenced in the `UI.Facets` annotation. If the latter isn’t yet available in your application, it gets added. As a next step, you can add fields to the sections and define their properties, such as label, display type \(including value help configuration\), text, text arrangement, criticality, etc.

You can then use [Edit in Source Code](edit-in-source-code-7d8e942.md) feature to see and manually edit the generated annotations. You can also always undo the changes made during the current session and redo them.

