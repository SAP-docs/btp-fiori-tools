<!-- loio1488469a315c442fa116ab4449d4ad27 -->

# SAP Fiori Elements

In SAP Fiori elements, perform the following steps:

1.  Select a [**Floorplan**](supported-floorplans-2b2b12e.md) for your application and click *Next*. The following options are available:
    -   [List Report Object Page](supported-floorplans-2b2b12e.md#loio2b2b12e708944d85a40d087194cc1edd__ul_emp_5pt_rlb)
    -   [Worklist](supported-floorplans-2b2b12e.md#loio2b2b12e708944d85a40d087194cc1edd__ul_v3k_15v_54b)
    -   [Analytical List Page](supported-floorplans-2b2b12e.md#loio2b2b12e708944d85a40d087194cc1edd__ul_jxj_25v_54b)
    -   [Overview Page](supported-floorplans-2b2b12e.md#loio2b2b12e708944d85a40d087194cc1edd__ul_dcr_h5v_54b)

2.  Select a [**Data Source**](data-source-9906181.md) and click *Next*.

    -   [Connect to an SAP System](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_tpk_mzx_v4b)
    -   [Connect to an OData Service with a customized URL](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_i2d_yzx_v4b)
    -   [Connect to an OData service](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_sx1_chy_v4b)
    -   [Upload a Metadata Document](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_xk3_nhy_v4b)
    -   [Connect to SAP Business Accelerator Hub](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_rgz_xhy_v4b)
    -   [Use a Local CAP Project](data-source-9906181.md#loio99061814ead548808d539861fb27bafb__section_fgh_m3y_v4b)

    > ### Note:  
    > If a username and password are required, enter your credentials and click the *Login* icon \(person with an arrow\).
    > 
    > ![](images/Login_button_App_Gen_fb8dd99.png)

3.  Select [**Associated floorplan properties**](floorplan-properties-745ae0c.md), such as the *Main entity* and *Navigation entity*.
4.  On the *Project Attributes* wizard page, configure the main project attributes.

    > ### Note:  
    > Some fields are already prefilled with default text, which can be modified if needed. Mandatory fields are marked with an asterisk \(\*\).

    -   **Module name** \(required\): Must be alpha-numeric and cannot contain spaces. The generated Node.js application uses the module name as its package name. It is used as the folder name of the generated application.

        > ### Note:  
        > Module names can only contain URL-friendly characters.

    -   **Application title**: The title that is displayed in the launchpad tile and header of the generated application.
    -   **Application namespace**: The SAPUI5 project namespace to be used. Must start with a letter and contain letters, digits, and periods only.
    -   **Description**: The description of the application.
    -   **Project folder path** \(required\): The parent folder in which the new application is generated. The new application is generated in a new folder with the module name. If a folder with the same name already exists, the user must choose a new module name.

        > ### Note:  
        > You cannot select a project folder path that already contains an SAP Fiori application. If you want to create an application as part of a CAP project, you must select *Local CAP Project* as the *Data Source* in Step 2.

    -   **Minimum SAPUI5 version**: From the dropdown list, select the minimum SAPUI5 version that the application will require.

        -   The dropdown will show the list of available versions of SAPUI5, with the current default version being preselected. The dropdown will list SAPUI5 versions grouped by maintenance status as listed [here](https://ui5.sap.com/versionoverview.html).
        -   If the source system during generation is an ABAP on Premise system, then the default version selected in the dropdown will be equal to the version of SAPUI5 version on that ABAP system where possible.

        > ### Note:  
        > For an application generated with the OData V4 data source, the list of SAPUI5 versions supported is limited to the most recent versions.

    -   **[Adding Deployment Configuration to an Existing MTA Deployment File](../Additional-Configuration/adding-an-sap-fiori-application-to-an-mta-deployment-file-with-5a17ba6.md#loiod7525cef6f6c4aa4acf3ec09c5a8eacb)**.

        If a project is generated inside an app router configuration project that has an MTA file, then it will use the deployment configuration by default. In this case, you can still select *No* and skip the deployment configuration step.

    -   **[Add deployment configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_itv_dk5_t4b)**. The default value is *No*.

        Provide values to the prompts and click *Finish*.

    -   **[Add FLP configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_hbd_gzy_t4b)**. The default value is *No*.

        Provide values to the prompts and click *Finish*.

    -   **[Configure virtual endpoints for local preview](../../Previewing-an-Application/convert-a-project-to-use-virtual-endpoints-630ddec.md)**. The default value is *Yes.*

        With this option, virtual endpoints for local preview are used and these files do not need to be created during generation.

    -   **[Configure advanced options](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_uhj_l2z_t4b)**. The default value is *No*.

5.  Click *Finish* to generate the application.

