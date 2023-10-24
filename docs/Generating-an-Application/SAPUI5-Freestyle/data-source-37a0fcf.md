<!-- loio37a0fcf2388c4e8e9e9e4942e6c5cff4 -->

# Data Source

This section provides information on how to connect your application with a data source during generation. In the Data Source and Service Selection wizard page, you can select from one of the following options:



<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_l4w_krq_qpb"/>

## Connect to an SAP system

-   **Connect to an SAP system using** **VS Code.**

    In either case, you can create a system to connect to or select from any saved systems you may have already used.

    *Adding a new system*

    **Enter a system name** to identify the new system that will be unique to use in SAP Fiori application generator or in the **SAP Systems View**.

    **Select a Service Key**. For an SAP ABAP system hosted in the SAP Business Technology Platform, you must provide a service key that contains the key information for the required SAP ABAP system. This service key should be provided by your administrator for the selected SAP ABAP system. Once this information is provided, a browser tab launches and prompts you to authenticate against the system.

    For more information on how to create a service key, please see [Create Service Keys Using the Cockpit](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/cdf4f200db3e4c248fa67401937b2f78.html).

    > ### Note:  
    > Once you have authenticated your user for the new system in the browser, SAP Fiori application generator displays you the list of OData services available for the user you have used to log in. Please see the *Service* dropdown with the title *Service \(for user \[<USERNAME\>\]\)*.

    For an on-premise SAP ABAP system, you need to provide the system URL and optional client ID, along with the authentication details for that system if required.

    > ### Example:  
    > https://ldciu1y.wdf.sap.corp:44355, client: 010

    In both scenarios, you can store the system details in the secure storage of your operating system.

    -   Microsoft Windows: Keychain.
    -   MacOS: Credential Manager.

    Saving the system in this way ensures that you do not need to continually provide these details for generating an application or running the generated application locally.

    A saved system can be deleted from either of these places, as needed.

    > ### Note:  
    > When connecting for the first time, only the *New System* option is available.

-   **Connecting to an SAP System using** **SAP Business Application Studio.**

    When using the SAP Fiori application generator in SAP Business Application Studio, you can select from a list of destinations that are configured for *Business Application Studio* instance. The generator automatically retrieves the available destinations, and you can select from the list. If you do not have the correct access to use the destination end point, an error occurs.




<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_i2d_yzx_v4b"/>

## Connect to an OData Service with a Customized URL

If the OData endpoint that you want to use in your application can't be accessed directly, you can set it up as a destination and directly reference it in the generator. To do so, perform the following steps:

1.  In SAP Business Application Studio, launch the SAP Fiori generator and select the required template.
2.  Select *Connect to an OData Service* from the data source drop-down list.
3.  For the data source URL field, use the destination name followed by `.dest`. In this case, SAP Business Application Studio should be able to route to your service with the destination name.

> ### Example:  
> If the URL defined in the Destination is `https://someurl.com/someservice` with the destination name “MyDestination”, the following URL will be used in the SAP Fiori generator:
> 
> `https://MyDestination.dest/someservice`



<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_cxb_trq_qpb"/>

## Connect to an OData Service

Enter the OData endpoint URL to generate your application. All OData endpoints that are either **authenticated** with Basic authentication or **unauthenticated** are supported.

> ### Note:  
> The provided OData endpoint must be the correct version for the template that you select. For example, a V2 endpoint must be provided for the V2 template. The wizard informs you if there is any mismatch between the OData version and the template version.

If necessary, the system prompts you to provide your name and password.



<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_pmx_hvq_qpb"/>

## Upload a Metadata Document

To generate the application without relying on a backend service being available, upload a metadata xml file that you want to use.

Only [EDMX format](https://docs.microsoft.com/en-us/openspecs/windows_protocols/mc-edmx/5dff5e25-56a1-408b-9d44-bff6634c7d16) is supported for metadata xml file.

Once the metadata xml file has been validated, the system allows you to select the required entity options for the application.

> ### Note:  
> When using a `metadata.xml` file, the generated application is limited to only mock data.



<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_rqx_lsq_qpb"/>

## Connect to SAP Business Accelerator Hub

When users do not have their data source available, they can generate an application with the SAP Business Accelerator Hub. This data source is only intended to support the development and should be replaced with a real one before going live. When the SAP Business Accelerator Hub option is selected, a list of predefined services relevant to different industries appears.

-   Select a service that you want to generate an application with. For example, Just-In-Time Calls, Transaction Classifications, Content, Request of Quotation, and more.
-   Once the service is selected, two more fields appear for authentication purposes: *Enter your Username* and *Enter your Password*.
-   Fill in the fields and click *Next* to proceed with the application generation.

> ### Note:  
> You cannot deploy applications that use the SAP Business Accelerator Hub, as this data source is intended for local development only.

For more information, see [https://api.sap.com/](https://api.sap.com/).



<a name="loio37a0fcf2388c4e8e9e9e4942e6c5cff4__section_fbg_tsq_qpb"/>

## Use a Local CAP Project

You can select a local SAP Cloud Application Programming Model \(CAP\) project in your filesystem and the generator retrieves the services that are defined for that project. The folder location you provide is validated to ensure it is an SAP Cloud Application Programming Model \(CAP\) Node.js project that the generator can support.

For more information about CAP services, see: [https://cap.cloud.sap/docs/about/](https://cap.cloud.sap/docs/about/).

