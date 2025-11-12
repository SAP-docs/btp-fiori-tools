<!-- loioe913fbf28f6f4fa5986c5a25ecc3a8f5 -->

# Replacing OData Service

This guide describes how to replace an OData service in an adaptation project without tooling support.



<a name="loioe913fbf28f6f4fa5986c5a25ecc3a8f5__context_lwq_2ll_21c"/>

## Context

> ### Note:  
> The new OData service must be compatible to the OData service of the original app. The entity set names, properties in the entity set, and function imports used from the original service must also exist in the new service. For OData V2 services using annotations, the annotation data source must be changed and the new annotation must also be compatible with the annotation of the original app.



## Procedure

1.  Right click the `manifest.appdescr_variant` file of your adaptation project and select the *Adaptation Project* \> *Replace OData Service*.

2.  After the wizard starts, you may be asked to enter the credentials for the system that you created your adaptation project.

3.  From the *Target OData Service* dropdown, choose which service from the manifest of the base application you want to replace.

4.  Enter the URI of the OData service you want to use instead.

5.  \(Optional\) Enter the maxAge of the new OData service.

6.  \(Optional\) Enter the URI of the OData Annotation Data Source you want to use instead.

    This field is visible if the service you are using supports annotations.

7.  Click *Finish* to save your changes.


