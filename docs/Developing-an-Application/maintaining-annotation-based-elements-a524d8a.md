<!-- loioa524d8a307024c07ad59f2b73198ed63 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Maintaining Annotation-Based Elements

> ### Note:  
> The annotation generation features are only supported in the Page Editor for list reports, object pages, and form entry object pages based on OData V4.

The Application Modeler provides the ability to develop your application UI using a structured outline. In [Configure Page Elements](configure-page-elements-047507c.md), you can see the basic structural outline of your page layout. You can add, remove, and modify properties of different page elements without needing to know which annotations are used. The respective annotations are created and updated automatically in the local annotation file.

For example, you can add a section to the *Object Page* or *Form Entry Object Page* using the :heavy_plus_sign: \(*Add*\) icon on the *Sections* node and a new `UI.FieldGroup` record is automatically generated and referenced in the `UI.Facets` annotation. If no `UI.Facets` annotation exists yet, it is created. Then, you can add fields to the sections and define their properties.

You can also use the [Edit in Source Code](edit-in-source-code-7d8e942.md) feature to view and manually edit the generated annotations.

