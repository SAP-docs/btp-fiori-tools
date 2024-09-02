<!-- loio99061814ead548808d539861fb27bafb -->

# Data Source

This section provides information on how to connect your application with a data source during generation.

> ### Tip:  
> When running SAP Fiori tools in VS Code, you can save the connection information to a remote system. For more information, see [Managing System Connection](../../Project-Functions/managing-system-connection-78a82b6.md).

> ### Tip:  
> You can create a UI service for your SAP ABAP system. For more information, see [UI Service Generation](../../Project-Functions/ui-service-generation-1a7aad3.md).



<a name="loio99061814ead548808d539861fb27bafb__section_tpk_mzx_v4b"/>

## Connect to an SAP System

-   **Connect to an SAP system using** **VS Code.**

    In either case, you can create a new system to connect to, or select one of the saved systems you may have already used.

    *Adding a new system*

    1.  **Enter a system name** that you use to save the connection details for either an on-premise SAP ABAP system or SAP Business Technology Platform system.
    2.  **Select the SAP ABAP system type**.

        For the SAP ABAP system hosted in the SAP Business Technology Platform, you can choose from the following authentication types:

        -   Service Key

        -   Reentrance Ticket


        If you choose Service Key authentication, you must provide a service key that contains the key information for the required SAP ABAP system. Your administrator needs to provide this service key for the selected SAP ABAP system. Once this information is available, a browser tab launches and prompts you to authenticate against the system.

        For more information about how to create a service key, see [Create Service Keys Using the Cockpit](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/cdf4f200db3e4c248fa67401937b2f78.html).

        If you choose Reentrance Ticket authentication, provide the URL to your SAP S/4HANA Cloud system and log in when the browser window appears.

        > ### Note:  
        > Authenticating with reentrance tickets requires SAP S/4HANA Cloud 2408 or higher.

        > ### Note:  
        > Once you have authenticated your user for the new system in the browser, SAP Fiori application generator shows you the list of OData services available for the user you’ve used to log in. Please see the *Service* dropdown with the title *Service \(for user \[<USERNAME\>\]\)*.

        For an on-premise SAP ABAP system, you need to provide the system URL and optional client ID, along with the authentication details for that system if required.

        > ### Example:  
        > https://someurl:12345, client: 010


    In both scenarios, you can store the system details in the secure storage of your operating system:

    -   Microsoft Windows: Credential Manager

    -   macOS: Keychain


    Saving the system in this way ensures that you don’t need to continually provide these details for generating an application or running it locally.

    The saved connections can be viewed and deleted in the *SAP Systems* view in VS Code.

    If you want to update the connection, we recommend that you delete the system from the *SAP Systems* view and recreate it in the project generator. For more information, see [Managing System Connection](../../Project-Functions/managing-system-connection-78a82b6.md).

    > ### Note:  
    > When connecting for the first time, only the *New System* option is available.

    *Using a saved system*

    1.  Select a previously saved system.

        The wizard skips the authentication if your saved system credentials are still valid.

    2.  If saved authentication details are invalid, you’ll be prompt to reauthenticate. For example, if your password is expired.

-   **Connect to an SAP system using** **SAP Business Application Studio.**

    When using the SAP Fiori application generator in SAP Business Application Studio, you can select from a list of destinations that are configured for the SAP Business Application Studio instance. The generator automatically retrieves the available destinations to select from. If you do not have the correct access to use the destination endpoint, an error occurs.

    The destinations are expected to have a catalog service that provides a list of V2 and V4 OData services that are available.

    If you want to use a destination to reference a service URL endpoint, see [Connect to an OData Service with a customized URL](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_i2d_yzx_v4b).

    > ### Note:  
    > In SAP Business Application Studio, to create SAP Fiori elements application in SAP BTP ABAP environment, you must be assigned to one of the following roles:
    > 
    > -   OrgManager
    > -   SpaceManager
    > -   SpaceDeveloper




<a name="loio99061814ead548808d539861fb27bafb__section_i2d_yzx_v4b"/>

## Connect to an OData Service with a Customized URL

If the OData endpoint that you want to use in your application can't be accessed directly, you can set it up as a destination and directly reference it in the generator. To do so, perform the following steps:

1.  In SAP Business Application Studio, launch the SAP Fiori application generator and select the required template.
2.  Select *Connect to an OData Service* from the data source drop-down list.
3.  For the data source URL field, use the destination name followed by `.dest`. In this case, SAP Business Application Studio should be able to route to your service with the destination name.

> ### Example:  
> If the URL defined in the Destination is `https://someurl.com/someservice` with the destination name “MyDestination”, the following URL will be used in the SAP Fiori application generator:
> 
> `https://MyDestination.dest/someservice`



<a name="loio99061814ead548808d539861fb27bafb__section_sx1_chy_v4b"/>

## Connect to an OData Service

Enter the OData endpoint URL to generate your application.

-   All OData endpoints that are either **authenticated** or **unauthenticated** are supported.

-   The OData endpoint must be the correct version of the template that you’ve selected. For example, a V2 endpoint must be provided for a V2 template. The wizard informs you in case of any mismatch between the OData version and the template version

> ### Note:  
> If necessary, the system prompts you to provide your name and password.



<a name="loio99061814ead548808d539861fb27bafb__section_xk3_nhy_v4b"/>

## Upload a Metadata Document

Upload a `metadata XML` file that you want to use. Now, you can generate the application without relying on a back-end service being available.

-   Only [EDMX format](https://docs.microsoft.com/en-us/openspecs/windows_protocols/mc-edmx/5dff5e25-56a1-408b-9d44-bff6634c7d16) is supported for the `metadata XML` file.

-   Once the `metadata XML` file is validated, you can select the required entity options for the application.

> ### Note:  
> Using the `metadata.xml` file restricts the generated application to only mock data.



<a name="loio99061814ead548808d539861fb27bafb__section_rgz_xhy_v4b"/>

## Connect to SAP Business Accelerator Hub

> ### Caution:  
> SAP Business Accelerator Hub has been deprecated from the Application Generator as a data source and will be removed in a future release. We strongly recommend that you use the Service Center in SAP Business Application Studio to generate applications if you intend to still use SAP Business Accelerator Hub.
> 
> For more information, see [Service Center](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/1e8ec75c9c784b51a91c7370f269ff98.html).

When users don't have their data source available, they can generate an application with the SAP Business Accelerator Hub. This data source is only intended to support the development and should be replaced with a real one before going live.

> ### Note:  
> Ensure that you logged in to [https://api.sap.com/](https://api.sap.com/) at least once before connecting to SAP Business Accelerator Hub.

-   In the *Data Source and Service Selection* wizard page, select “Connect to SAP Business Accelerator Hub” from the *Data source* drop-down list.
-   When the SAP Business Accelerator Hub option is selected, a list of predefined services relevant to different industries appears. Select a service that you want to generate an application with. For example, Just-In-Time Calls, Transaction Classifications, Content, Request of Quotation, and more.
-   Once the service is selected, two more fields appear for authentication purposes: *Enter your Username* and *Enter your Password*.
-   Fill in the fields and click *Next* to proceed with the application generation.

> ### Caution:  
> SAP Business Accelerator Hub services are not intended for use with SAP Fiori UI development.

> ### Note:  
> It is not recommended to deploy applications that use the SAP Business Accelerator Hub, as this is a sandbox data source and is intended for local development only. See [Run Your HTML5 Application with the SAP Business Accelerator Hub](https://help.sap.com/docs/bas/developing-html5-application/run-your-html5-application-with-sap-api-business-hub), for more details on running your application with SAP Business Accelerator Hub.

For more information, see [https://api.sap.com/](https://api.sap.com/).



<a name="loio99061814ead548808d539861fb27bafb__section_fgh_m3y_v4b"/>

## Use a Local CAP Project

You can either select a local SAP Cloud Application Programming Model \(CAP\) project that has been detected in your workspace, or manually select the CAP project folder path and the generator will retrieve the services that are defined for that project.

> ### Note:  
> A local CAP Project data source is limited to the List Report Object Page and Analytical List Page templates that are based on the OData V4. This option is not available for the Worklist and Overview Page templates.

> ### Note:  
> [OData V2 Support for CAP](https://cap.cloud.sap/docs/advanced/odata#odata-v2-support) - While CAP defaults to OData V4, the latest protocol version, some projects need to fallback to OData V2, for example, to keep using existing V2-based UIs. SAP Fiori tools does not recommend and support having both OData V2 and OData V4 applications in the app folder within the CAP project. In case, you have a requirement to create both OData V2 and ODataV4 applications, it is recommended that you generate the OData V2 app outside of the CAP project.

For more information about CAP services, see: [https://cap.cloud.sap/docs/about/](https://cap.cloud.sap/docs/about/).

**SAP Fiori tools support two types of SAP CAP Projects:**



### **SAP CAP Node.js Project**

**Project Prerequisites**

-   [Node.js](../../Getting-Started-with-SAP-Fiori-Tools/visual-studio-code-17efa21.md#loio17efa217f7f34a9eba53d7b209ca4280)
-   Sample Projects:
    -   [CAP Node.js Teched2020](https://github.com/SAP-samples/teched2020-IIS360).
    -   [Cloud CAP Samples](https://github.com/SAP-samples/cloud-cap-samples).

        > ### Note:  
        > If you use one of the sample projects, ensure the workspace root is set to the cloned repository and execute `npm install`.



**SAP CAP Node.js Project steps**

1.  Perform the steps identified in the [SAP Fiori Elements](sap-fiori-elements-1488469.md) section.
2.  On the *Data Source and Service Selection* wizard page, in the *Data source* drop-down list, select *Use a Local CAP Project*. If there is only one CAP project in the workspace, the project is auto selected.
3.  If there are **CAP projects** detected in your workspace, you can then choose from the list of **CAP projects** that have been found. If your **CAP project** is not in the list, select *Manually select CAP project folder path* and browse to your **CAP project** location. If the generator is unable to find any local **CAP projects** in your workspace, you can provide the **CAP project** folder path manually.

    > ### Note:  
    > If the generator cannot find a major version of @sap/CDS in your workspace – either globally or as part of the project – that matches the version specified in your CAP project, then you won't be permitted to generate your application because the generated application would be using an invalid @sap/CDS version.

4.  In the *OData service* drop-down list, select a service, and click *Next*.
5.  On the *Entity Selection* wizard page, select the main entity from a drop-down list.

    > ### Note:  
    > The properties of this entity are used to display data on the List Report from the entity collection.

6.  Leave the value for the *Navigation Entity* field as *None* and click *Next*.
7.  On the *Project Attributes* wizard page, add the required attributes to the application project. For example:

    -   *Module name*: `incidents`.
    -   *Application title*: `My Incidents`.
    -   *Application namespace*: `sap.fe.demo`

    For the rest of the attributes, keep the default values.

    For more information on the Project Attributes wizard page, see [SAP Fiori Elements Application](sap-fiori-elements-1488469.md#loio1488469a315c442fa116ab4449d4ad27__project_attributes).

8.  Click *Finish* to start the app generation.



### **SAP CAP Java Project**

**Project Prerequisites**

-   Ensure `cds`, `java`, and `mvn` are installed on your computer to be able to execute these commands in the terminal and identify their version numbers:

    ```
     cds --version
     java --version
     mvn --version
    ```

    For more information, see [Setting Up Local Development](https://cap.cloud.sap/docs/java/getting-started#local) in the CAP Java documentation.

-   Sample Projects:

    -   [CAP Samples for Java](https://github.com/SAP-samples/cloud-cap-samples-java/).

        > ### Note:  
        > If you use one of the sample projects, confirm that all system requirements are met. Execute `mvn` command:
        > 
        > ```
        > cd cloud-cap-samples-java
        > mvn spring-boot:run
        > ```


    It takes some time for the command to install dependencies, build, and start the project. After the command is executed, click the `http://localhost:8080` link to open a browser and see the services, such as `admin` or `browse`. You can cancel the command by entering `Ctrl + C` in the terminal.


**SAP CAP Java Project steps**

1.  Perform the steps identified in the [SAP Fiori Elements](sap-fiori-elements-1488469.md) section.
2.  On the *Data Source and Service Selection* wizard page, in the *Data source* drop-down list, select *Use a Local CAP Project*. If there is only one CAP project in the workspace, the project is auto selected.
3.  If there are **CAP projects** detected in your workspace, you can then choose from the list of **CAP projects** that have been found. If your **CAP project** is not in the list, select *Manually select CAP project folder path* and browse to your **CAP project** location. If the generator is unable to find any local **CAP projects** in your workspace, you can provide the **CAP project** folder path manually.
4.  In the *OData service* drop-down list, select a service, for example, CatalogService, and click *Next*.
5.  On the *Entity Selection* wizard page, select the main entity from a drop-down list.

    > ### Note:  
    > The properties of this entity are used to display data on the List Report from the entity collection.

6.  Leave the value for the *Navigation Entity* field as *None* and click *Next*.
7.  On the *Project Attributes* wizard page, add the required attributes to the application project. For example:

    -   *Module name*: `books`.
    -   *Application title*: `Books`.

    For the rest of the attributes, keep the default values.

    For more information on the *Project Attributes* wizard page, see [SAP Fiori Elements Application](sap-fiori-elements-1488469.md#loio1488469a315c442fa116ab4449d4ad27__project_attributes).

8.  Click *Finish*.
9.  In the terminal, execute the command `mvn spring-boot:run`.
10. Open the file `app/books/README.md` and find the link leading to the application, such as `http://localhost:8080/books/webapp/index.html`.
11. Click the link to the application.
12. When prompted, enter the username and password. For example, `user/user` or `admin/admin`.

    > ### Note:  
    > You can check the terminal output to see the username and password credentials to be used.

    The SAP Fiori launchpad sandbox with a newly created application appears.


