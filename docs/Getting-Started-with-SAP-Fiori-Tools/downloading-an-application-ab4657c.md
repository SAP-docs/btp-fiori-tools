<!-- loioab4657ca9bd84cd6869a750a1d94b5bd -->

# Downloading an Application

You can download SAP Fiori applications from the SAPUI5 ABAP repository and migrate them to be compatible with SAP Fiori tools. This is supported for systems using SAP S/4HANA, SAP S/4HANA Public Cloud Edition, and SAP S/4HANA Private Cloud Edition.

> ### Note:  
> The application code is normally minified before deployment, and so the resulting code that is downloaded is also the minified version. We recommend that you only use this procedure if the application code is not already available under source control.
> 
> The `-dbg.js` file, such as `(Component-dbg.js)`, contains the original un-minified code. You can copy its contents into the corresponding `.js` file, for example, *Component-dbg.js* \> *Component.js* for more human readable code.
> 
> Remove `-dbg.js`, `-preload.js` and `.js.map` before running UI5 CLI build, otherwise they are recreated in the `dist` folder.



## Downloading an SAP Fiori Application

To do so, perform the following steps:

-   Open an empty folder or workspace.
-   Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori: Download App from SAPUI5 ABAP Repository` command.
-   Select the *System* you want to download the application from. The system must be added in the Connection Manager for SAP Systems and if you haven't saved your credentials, you must provide a *Username* and *Password*. All systems except for those with the *Service URL Endpoint* connection type are supported. For more information, see [Managing SAP System Connections](../Project-Functions/managing-sap-system-connections-78a82b6.md).
-   Select the *Application*.
-   Select a folder as the *Project Folder Path*.

    > ### Note:  
    > Ensure the *Project Folder Path* is a folder in your workspace for the migration to work correctly.

-   Click *Finish*. Your SAP Fiori application has been downloaded and the *SAP Fiori Migration Tool* opens.



## Migrating an SAP Fiori Application

After downloading an SAP Fiori application from the SAPUI5 ABAP repository, you must migrate the project to be compatible with SAP Fiori tools.

To do so, perform the following:

-   Select the app you downloaded.
-   Configure the migration settings. For more information, see [Migration](migration-70d41f3.md).
-   Click *Start Migration*.

Your application is now compatible with SAP Fiori tools.

