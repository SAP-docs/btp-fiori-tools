<!-- loio616b1a4bd4314070a9fa5bf79ecb3909 -->

# Freestyle SAPUI5

Learn how to generate a freestyle SAPUI5 application.

> ### Note:  
> If you are using SAP Business Application Studio, ensure you use a SAP Fiori dev space.

1.  In the *SAP Fiori generator*, select a template that supports freestyle SAPUI5 applications and click *Next*. For more information, see [Supported Templates](supported-templates-20d1146.md).
2.  Select a *Data source* and click *Next*. For more information, see [Data Source](data-source-37a0fcf.md).
3.  Enter a name for your view and click *Next*. For more information, see [Template Properties](template-properties-c2a3c82.md).
4.  Configure the project attributes and click *Finish*. A list of project attributes is provided below:

    > ### Tip:  
    > Mandatory fields are prefilled with default text.

    -   **Module name** \(Required\): The module name attribute is used as the folder and package name for the generated application. The module name must be alphanumeric and cannot contain spaces.
    -   **Application title** \(Required\): The application title attribute is used as the title in the header of the generated application.
    -   **Application namespace** \(Required\): The application namespace attribute is used as the SAPUI5 project namespace. It must start with a letter and only contain letters, digits, and periods.
    -   **Description**: The description attribute is used as the description of the application.
    -   **Project folder** \(Required\): The project folder attribute is used as the parent folder in which the new application is generated. The new application is generated in a new folder with the module name. If a folder with the same name already exists, you must choose a new module name.
    -   **Minimum SAPUI5 version**: The minimum SAPUI5 version attribute is used as the minimum SAPUI5 version required in the application.
        -   The dropdown shows the list of available SAPUI5 versions grouped by maintenace status and the default version is preselected. For more information on the maintenace status of SAPUI5 versions, see [SAPUI5 Versions Maintenance Status](https://ui5.sap.com/versionoverview.html).
        -   If the source system is an ABAP on-premise system, then the default version selected in the dropdown is equal to the SAPUI5 version on the ABAP system.

    -   **Add deployment configuration to MTA project**

        The add deployment to MTA project attribute is used if an MTA file already exists in the project folder path. If a project is generated inside an app router configuration project that has an MTA file, then uses its deployment configuration by default. For more information, see [Adding Deployment Configuration to an Existing MTA Deployment File](../Additional-Configuration/adding-an-sap-fiori-application-to-an-mta-deployment-file-with-5a17ba6.md#loio5a17ba6b62b2462aa0e25ffae7b8d728).

    -   **Add deployment configuration**: The add deployment configuration attribute is used to determine whether to configure deployment settings. For more information, see [Add Deployment Configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_itv_dk5_t4b).
    -   **Add FLP configuration:** The Add FLP configuration attribute is used to determine whether to add a SAP Fiori launchpad configuration. For more information, see [Add FLP configuration](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_hbd_gzy_t4b).
    -   **Configure virtual endpoints for local preview**:

        The configure virtual endpoints for local preview attribute is used to determine whether to activate virtual endpoints for preview. When active, preview files are not created during generation and virtual endpoints are used instead.

    -   **Configure advanced options**: The configure advanced options attribute is used to determine whether to display advanced options. For more information, see [Configure advanced options](../Additional-Configuration/additional-configuration-9bea64e.md#loio9bea64e63b824261932d90037ce3c5ae__section_uhj_l2z_t4b).

5.  Click *Finish* to generate the application.

