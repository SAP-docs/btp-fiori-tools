<!-- loio05f2a9ef5e27402382d1ac9cfb98537f -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create a New Run Configuration in SAP Business Application Studio

> ### Note:  
> *Run Configuration Wizard* requires @sap/ux-ui5-tooling version 1.5.3 and higher.

In SAP Business Application Studio, you can create additional run configurations that define how your project is executed. To do so, perform the following steps:

1.  From the left-side toolbar, click *Run Configurations*.

    The run configuration pane appears.

2.  In the left pane, click the :heavy_plus_sign: \(*Add*\) icon to create a new configuration.

    A dialog box appears.

3.  In the option *What would you like to run?*, you are prompted to select the project for which you want to create the configuration.
4.  Fill in the following sections:

    -   *Name* \(**mandatory**\) - You can change the name.
    -   *Endpoint*\(**mandatory**\) - Select the HTML file that is used when the application is started.
    -   *Mock Data* - Runs your application with a mock server which will mock the OData requests.
    -   *Support Assistant* - Enables application developers to check whether their applications are built according to the best practices for building SAPUI5 applications. The tool uses a set of pre-defined rules to check all aspects of an application.
    -   *URL Components* - Enables application developer to define additional URL parameters and/or hash fragment for the SAP Fiori launchpad intent-based navigation.
    -   *Advanced Settings* - Enables the application developer to define which SAPUI5 version will be used during runtime and/or change the destinations that are used by the application.

        Additionally the application developer can choose to download the SAPUI5 sources for a specific version by selecting *Use local SAPUI5 sources*. The downloaded SAPUI5 libraries are then used when running the preview. When *Use local SAPUI5 sources* is selected for preview, then the option *Run with mock data* is automatically selected.


    Click [Save\]

5.  The new launch configuration appears in the *Run and Debug* pane on the left and also in the table on the UI..
6.  To run the project, click on the [\>\] - icon in the *Actions* section. Alternatively you can select the*Run Configuration* from the drop-down list in the *Run and Debug* pane and click the <span class="SAP-icons-V5"></span> \(*Start Debugging*\) icon.

Additionally, in the *Run Configuration Pane* you can perform the following actions:

-   **Bind/Unbind SAPUI5 Version:** Quick actions for changing the UI5 version of the run configuration.
-   **Bind/Unbind Data Source:**Quick action for changing the destination of the run configuration.
-   **Rename:** right-click on the run configuration and choose Rename to provide a new name for the selected run configuration.
-   **Show in File:** right-click on the run configuration and choose Show File to open the JSON file containing the set of configuration properties, with the name highlighted.
-   **Delete:** right-click on the run configuration and choose Delete to delete the run configuration.

