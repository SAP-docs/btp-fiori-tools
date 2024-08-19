<!-- loio3b1f37edf22c4d3dbc14472d6dcb6e2a -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create a New Run Configuration in Visual Studio Code

> ### Note:  
> *Run Configuration Wizard* requires @sap/ux-ui5-tooling version 1.5.3 and higher.

A new run configuration is created with the command `Fiori: Open Run Configurations`. To add custom configuration files for your project, perform the following steps:

1.  From the command palette, select `Fiori: Open Run Configurations`.
2.  Select the project that you want to add a new configuration and click [Enter\] to confirm your input.
3.  Existing run configurations for the selected project is displayed. Click [Create\].
4.  Fill in the following sections:

    -   *Name* \(**mandatory**\) - You can change the name.
    -   *Endpoint*\(**mandatory**\) - Select html file that is used when application is started.
    -   *Mock Data* - Runs your application with a mock server which will mock the OData requests.
    -   *Support Assistant* - Enables application developers to check whether their applications are built according to the best practices for building SAPUI5 applications. The tool uses a set of pre-defined rules to check all aspects of an application.
    -   *URL Components* - Enables application developer to define additional URL parameters and/or hash fragment for the SAP Fiori launchpad intent-based navigation.
    -   *Advanced Setting*- Enables the application developer to define which SAPUI5 version will be used during runtime and/or change the destinations that are used by the application.

        Additionally the application developer can choose to download the SAPUI5 sources for a specific version by selecting [Use local SAPUI5 sources\]. The downloaded SAPUI5 libraries are then used when running the preview. When [Use local SAPUI5 sources\] is selected for preview, then the option [Run with mock data\] is automatically selected.


    Click [Save\]

5.  The new launch configuration appears in the *Run and Debug* pane on the left and also in the table on the UI.
6.  To run the project, click on the [\>\] - icon in the *Actions* section of the table. Alternatively you can select *Run Configuration* from the drop-down list in the *Run and Debug* pane and click the <span class="SAP-icons-V5"></span> \(*Start Debugging*\) icon.

