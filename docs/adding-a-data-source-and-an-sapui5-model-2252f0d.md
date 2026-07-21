<!-- loio2252f0deb96940609081a8a19f60da8e -->

# Adding a Data Source and an SAPUI5 Model

This guide describes how to add an external data source with the option to also add a new SAPUI5 model.



## Context

You can add one of the following types of data source:

-   OData V2
-   OData V4
-   HTTP

To add an OData V2 service using annotations, you need to add a new annotation data source.



## Procedure

1.  Right click the `manifest.appdescr_variant` file of your adaptation project and select the *Adaptation Project* \> *Add Data Source and SAPUI5 Model*.

2.  Select the service type you want to add.

3.  Select the Destination that points to the system that hosts the service.

4.  Enter the Service URI.

5.  If you selected *HTTP* as your service type, enter a name for your data source. If you selected *OData* as your service type, enter a name for your model and data source.

6.  \(Optional for OData V2/V4\) Enter settings for the OData Service SAPUI5 Model in the format of `"key1":"value1","key2":"value2", …`.

7.  \(Optional for OData V2/V4\) Choose whether to add annotation or not.

    If you choose yes, provide the following information:

    1.  Enter the OData Annotation Data Source name.

    2.  Enter the OData Annotation Data Source URI.

    3.  \(Optional\) Enter settings for the annotation in the format of `"key1":"value1","key2":"value2", …`.


8.  Choose *Finish* to create the change.


