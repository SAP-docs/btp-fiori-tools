<!-- loio616b1a4bd4314070a9fa5bf79ecb3909 -->

# Freestyle SAPUI5

**Generating an freestyle SAPUI5 application**.

> ### Note:  
> In SAP Business Application Studio, use SAP Fiori elements Dev Space.

1.  Select [Supported Templates](supported-templates-20d1146.md), click *Next*.
2.  Select [Data Source](data-source-37a0fcf.md), click *Next*.

    -   **Connect to an SAP system**
    -   **Connect to an OData service**
    -   **Connect to SAP Business Accelerator Hub**
    -   **Use a local CAP Node.js project**
    -   **Upload a Metadata Document**
    -   **None**

    > ### Note:  
    > If username and password are required, enter these credentials and click the *Login* icon \(person with an arrow\).
    > 
    > ![](../SAP-Fiori-Elements/images/Login_button_App_Gen_fb8dd99.png)

3.  Select [Template Properties](template-properties-c2a3c82.md).
4.  Add project attributes:

    > ### Tip:  
    > Mandatory fields are prefilled with default text.

    -   **Module Name** \(Required\). Must be alphanumeric and can’t contain spaces. The generated Node.js application uses the module name as its package name. It’s used as the folder name of the generated application.
    -   **App Title** \(Required\). The title in the header of the generated application.
    -   **App Namespace** \(Required\). The SAPUI5 project namespace to be used. It must start with a letter and contain letters, digits, and periods only.
    -   **Description**. The text description of the application.
    -   **Project Folder** \(Required\). The parent folder in which the new application is generated. The new application is generated in a new folder with the module name. If a folder with the same name already exists, the user must choose a new module name.
    -   **Minimum SAPUI5 version**. From the dropdown list, select the minimum SAPUI5 version that the application will require.

        -   The dropdown will show the list of available versions of SAPUI5, with the current default version being preselected. The dropdown will list SAPUI5 versions grouped by maintenance status as listed [here](https://ui5.sap.com/versionoverview.html).
        -   If the source system during generation is an ABAP on-premise system, then the default version selected in the dropdown will be equal to the SAPUI5 version on that ABAP system where possible.

        > ### Note:  
        > For an application generated with the `OData V4` data source, the list of SAPUI5 versions supported is limited to the most recent ones.

    -   **[Adding Deployment Configuration to an Existing MTA Deployment File](../Additional-Configuration/adding-an-sap-fiori-application-to-an-mta-deployment-file-with-5a17ba6.md#loio5a17ba6b62b2462aa0e25ffae7b8d728)**

        If a project is generated inside an app router configuration project that has an MTA file, then it will use its deployment configuration by default. You can select *No* to skip the deployment configuration step.

    -   **[Add deployment configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_itv_dk5_t4b)**. The default value is *No*.

        Provide values to the prompts and click *Finish*.

    -   **[Add FLP configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_hbd_gzy_t4b)**. The default value is *No*.

        Provide values to the prompts and click *Finish*.

    -   **Configure virtual endpoints for local preview**. The default value is *Yes*.

        With this option, virtual endpoints for local preview is used and these files do not need to be created during generation.

    -   [Configure advanced options](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_uhj_l2z_t4b). The default value is *No*.

5.  Click *Next* to generate the application.

