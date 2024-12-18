<!-- loio6b51df20afde4b10aa24bff0b3d6ae25 -->

# Replacing OData Service

Learn how to replace an OData service.



## Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and click *Replace OData Service*.

2.  From the *Target OData Service* dropdown, choose which service from the manifest of the base application you want to replace.

3.  Enter the URI of the OData service you want to use instead.

4.  \(Optional\) Enter the `maxAge` of the new OData service.

5.  \(Optional\) Enter the URI of the OData Annotation Data Source you want to use instead.

    This field will be visible if the service you are using supports annotations.

    > ### Note:  
    > The new OData service must be compatible with the OData service of the original app. The entity set names, properties in the entity set, and function imports used from the original service must also exist in the new service. For OData V2 services using annotations, the annotation data source must be changed and the new annotation must also be compatible with the annotation of the original application.

6.  Click *Finish* to save your changes.


