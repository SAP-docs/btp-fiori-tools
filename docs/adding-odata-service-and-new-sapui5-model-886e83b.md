<!-- loio886e83beac364e4ebc1eaee14f73ecee -->

# Adding OData Service and New SAPUI5 Model

This guide describes how to add an OData service with the option to add a new SAPUI5 model.



## Context

When adding a OData V2 service using annotations, it's necessary to add the new annotation data source. This requirement doesn't apply to OData V4 services.



## Procedure

1.  Right click the `manifest.appdescr_variant` file of your adaptation project and select the *Adaptation Project* \> *Add OData Service And SAPUI5 Model*.

2.  After the wizard starts, enter the OData Service name for the service you want to add.

3.  Enter the OData Service URI.

4.  Choose the OData version of the service you are adding.

5.  Enter the OData Service SAPUI5 Model name of the model you want to add.

6.  \(Optional\) Enter settings for the OData Service SAPUI5 Model in the format: `"key1":"value1","key2":"value2",`.

7.  \(Optional\) Choose whether to add an annotation.

    If you choose yes, provide the following information:

    1.  Enter the OData Annotation Data Source name.

    2.  Enter the OData Annotation Data Source URI.

    3.  \(Optional\) Enter settings for the annotation in the format: `"key1":"value1","key2":"value2",`.


8.  Click *Finish* to save your changes.


