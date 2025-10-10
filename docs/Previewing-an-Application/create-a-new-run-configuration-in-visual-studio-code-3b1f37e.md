<!-- loio3b1f37edf22c4d3dbc14472d6dcb6e2a -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create a New Run Configuration in Visual Studio Code

> ### Note:  
> The *Run Configuration Wizard* requires `@sap/ux-ui5-tooling` version 1.5.3 or higher.

In Visual Studio Code, you can create additional run configurations that define how your project is executed. To do so, perform the following steps:

1.  From the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \), execute the`Fiori: Open Run Configurations` command.
2.  Select the project to which you want to add a new configuration and press [Enter\] to confirm.
3.  The existing run configurations for the selected project are displayed. Click *Create*.
4.  Provide the following information:

    -   *Name* \(**mandatory**\): You can change the provided default name.
    -   *Endpoint*\(**mandatory**\): Select the HTML file that is used when the application is started.
    -   *Mock Data*: Runs your application with a mock server which mocks the OData requests.
    -   *Support Assistant*: Enables you to check whether your applications are built according to the best practices for building SAPUI5 applications. The tool uses a set of pre-defined rules to check all aspects of an application.
    -   *Enable Remote Access*: Enables remote access to the application so you can test your application on a different device such as a mobile phone or tablet. The server accepts connections from all hosts on your network, so do not use it in a productive environment. It is only intended for development purposes. When enabled, information is provided in the terminal about how to connect to the server using a URL or QR code.

        This feature requires `@sap/ux-ui5-tooling` version 1.19.1 or higher.

    -   *URL Components*: Enables you to define additional URL parameters and a hash fragment for the SAP Fiori launchpad intent-based navigation.
    -   *Advanced Setting*: Enables you to define which SAPUI5 version is used during runtime and change the destinations that are used by the application.

        Additionally, you can choose to download the SAPUI5 sources for a specific version by selecting *Use local SAPUI5 sources*. The downloaded SAPUI5 libraries are then used when running the preview. When *Use local SAPUI5 sources* is selected for preview, then *Run with mock data* is automatically selected.


    Click *Save*.

5.  The new launch configuration appears in the *Run and Debug* pane on the left and also in the *Run Configurations* table.
6.  To run the project, click on the \> icon underneath the *Actions* column of the table. Alternatively, you can select *Run Configuration* from the dropdown list in the *Run and Debug* pane and click the <span class="SAP-icons-V5"></span> \(*Start Debugging*\) icon.

