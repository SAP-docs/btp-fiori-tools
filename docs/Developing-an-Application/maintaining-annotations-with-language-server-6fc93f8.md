<!-- loio6fc93f80827940809437365abdf85b75 -->

# Maintaining Annotations with Language Server



<a name="loio6fc93f80827940809437365abdf85b75__section_ghs_fs5_hrb"/>

## CAP CDS Files

Maintaining OData annotations in `.cds` files is accelerated by the [SAP Fiori tools - CDS OData Language Server](https://www.npmjs.com/package/@sap/ux-cds-odata-language-server-extension) comprised in [SAP CDS Language Support](https://marketplace.visualstudio.com/items?itemName=SAPSE.vscode-cds) plugin. It assists you with adding and editing OData annotations in CDS syntax with:

-   Code completion for annotations applied to entities and entity elements
-   Validation against the OData vocabularies and project metadata
-   Navigation to the referenced annotations
-   Quick view of vocabulary information
-   Internationalization \(i18n\) support for language-dependent strings

See[CAP CDS](https://cap.cloud.sap/docs/about/) and [Serving Fiori UIs: Adding Fiori Annotation](https://cap.cloud.sap/docs/advanced/fiori#fiori-annotations) for more information about CDSODataLanguage Server.

> ### Note:  
> The SAP Business Application Studio SAP Fiori dev space doesn’t include the CDSODataLanguage Server extension.



<a name="loio6fc93f80827940809437365abdf85b75__XML_Code_Editor"/>

## XML Annotation Files

Maintaining OData annotations in `annotation.xml` files is accelerated by the XML annotation language server extension of SAP Fiori tools. It assists you with adding and editing OData annotations in XML syntax with the code completion, validation, and other assisting features, same as CDSODataLanguage Server in CAP CDS files. To get this assistance, just open the local annotation file in the code editor. You can either open local annotation file from [Service Modeler](visualizing-annotations-with-service-modeler-58784b5.md#loio58784b52f2284532afe2ab161e0312c9__section_uph_2rk_xlb) or single/double-click on the local annotation file of your project: `/webapp/annotations/<filename>.xml`.



### Using XML Annotation Language Server

**Prerequisites**

To maintain the annotations using XML annotation language server features, project needs to meet the following criteria:

-   OData service

    Your project contains the local copy of service metadata. The path to this copy is provided in the SAP OData vocabularies `manifest.json` file as a local `Uri`.

    > ### Note:  
    > The local copies of the metadata and back-end annotations are used for code completion and diagnostics in local annotation file, it’s important that it stays in sync with the service metadata state in back end. It is not synced automatically with the metadata on the back-end system. You can sync the local copy of the service metadata with the back end. For more information, see [Syncing Annotations](../Project-Functions/managing-service-and-annotation-files-8182ff3.md#loio8182ff3b19574f038bd636b9991aa24e__sync).

    The metadata of the OData service SAP OData must include one or multiple *<edm:Schema\>* definitions within the *<edmx:DataServices\>* element.

    According to the OData CSDL, your metadata file must contain a single `EntityContainer`.

    > ### Note:  
    > The namespace of the OData service should not contain `/` \(slashes\). The OData specification requires namespaces to consist of one or more SimpleIdentifiers separated by dots. Slashes aren’t supported. A SimpleIdentifier must start with a letter or underscore, followed by a maximum of 127 letters, underscores, and digits.

-   Local Annotation File

    Your project contains at least one valid annotation XML file that includes the *< /edmx:DataServices/Schema\>* node and references to the metadata. The metadata namespace must match that of the metadata file.

    > ### Note:  
    > If your project does not contain an `annotation.xml` file or you need more than one, you can create a new annotation file automatically registered in `manifest.json`. For more information, see [Visualizing Annotations with Service Modeler](visualizing-annotations-with-service-modeler-58784b5.md).

-   `manifest.json` file

    Your project contains a `manifest.json` file with the following information:

    -   `Uri` and `localUri` of the OData service
    -   List of OData annotation sources
    -   `@i18n` model with the `uri` to the `i18n.properties` file

    > ### Note:  
    > All paths used in annotation file are relative to the location of the `manifest.json` file.

    > ### Note:  
    > For more information on how to maintain the configuration in the `manifest.json` file, see [Visualizing Annotations with Service Modeler](visualizing-annotations-with-service-modeler-58784b5.md).




### Supported Vocabularies

The XML annotation language server is based on the [official OASIS vocabularies](https://github.com/oasis-tcs/odata-vocabularies/tree/master/vocabularies/) and [https://github.com/SAP/odata-vocabularies](https://github.com/SAP/odata-vocabularies) \(OData version 4.0\) The following vocabularies are supported:

**OData org**

-   [Aggregation](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Aggregation.V1.html)
-   [Authorization](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Authorization.V1.html)
-   [Capabilities](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Capabilities.V1.html)
-   [Core](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Core.V1.html)
-   [JSON](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.JSON.V1.html)
-   [Measures](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Measures.V1.html)
-   [Repeatability](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Repeatability.V1.html)
-   [Temporal](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Temporal.V1.html)
-   [Validation](https://oasis-tcs.github.io/odata-vocabularies/vocabularies/Org.OData.Validation.V1.html)

SAP

-   [Analytics](https://sap.github.io/odata-vocabularies/vocabularies/Analytics.html)
-   [CodeList](https://sap.github.io/odata-vocabularies/vocabularies/CodeList.html)
-   [Common](https://sap.github.io/odata-vocabularies/vocabularies/Common.html)
-   [Communication](https://sap.github.io/odata-vocabularies/vocabularies/Communication.html)
-   [Data Integration](https://sap.github.io/odata-vocabularies/vocabularies/DataIntegration.html)
-   [Direct-Edit](https://sap.github.io/odata-vocabularies/vocabularies/DirectEdit.html)
-   [Graph](https://sap.github.io/odata-vocabularies/vocabularies/Graph.html)
-   [Hierarchy](https://sap.github.io/odata-vocabularies/vocabularies/Hierarchy.html)
-   [HTML5](https://sap.github.io/odata-vocabularies/vocabularies/HTML5.html)
-   [ODM](https://sap.github.io/odata-vocabularies/vocabularies/ODM.html)
-   [PDF](https://sap.github.io/odata-vocabularies/vocabularies/PDF.html)
-   [Personal Data](https://sap.github.io/odata-vocabularies/vocabularies/PersonalData.html)
-   [Session](https://sap.github.io/odata-vocabularies/vocabularies/Session.html)
-   [UI](https://sap.github.io/odata-vocabularies/vocabularies/UI.html)



### OData

**For more information about OData:**

-   [OData specifications](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part3-csdl.html)




### Limitations

-   Annotations directly embedded in the metadata are not supported.

-   Dynamic expressions are not supported.


