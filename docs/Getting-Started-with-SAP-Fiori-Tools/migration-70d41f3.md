<!-- loio70d41f3ee29d453a90efab3ce025d450 -->

# Migration

SAP Fiori tools provide a migration utility to help move your SAP Fiori projects from other services, such as SAP SAP Web IDE, to VS Code or SAP Business Application Studio.

Some of the key points for migration:

-   Projects cloned or imported into the workspace are auto-detected for migration.
-   The migration tool supports SAP Fiori elements, SAP Fiori freestyle, SAPUI5Adaptation Projects, and SAPUI5 Extensibility.
-   Migration tools allow the migration of multiple projects at once.
-   Projects that have been migrated don't update any deployment configuration that was already defined. Please run `npm run deploy-config` after migration to configure the migrated application for deployment.
-   A project must have the main data source specified in the `manifest.json` file.

For more information about extensibility, please see [Extending an SAP Fiori Application](https://help.sap.com/docs/bas/developing-sap-fiori-app-in-sap-business-application-studio/extending-sap-fiori-application).



<a name="loio70d41f3ee29d453a90efab3ce025d450__section_dl4_dvs_ypb"/>

## Prerequisites

-   Ensure that you've the latest SAP Fiori tools extensions installed. For more information, see [Getting Started with SAP Fiori Tools](getting-started-with-sap-fiori-tools-2d8b1cb.md).
-   Ensure that your SAP Fiori project is running as expected in SAP SAP Web IDE and belongs to the supported project types:
    -   SAP Fiori elements V2.
    -   SAP Fiori elements V4.
    -   SAP Fiori freestyle.
    -   Extension project.




### Recommended

-   In SAP Business Application Studio, a destination of the target system needs to be defined that reflects the system used in the original application. For more information, see [SAP Business Application Studio Help Portal](https://help.sap.com/webcomponents/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/545ba7d9b3034679b7ea08bc36617c6c.html).

    > ### Note:  
    > If the target system isn’t defined, previewing an application with a live data won’t succeed.

-   In VS Code, you need to know the target system hostname and/or client.
-   We recommend that the project to be migrated is under a version control system.



<a name="loio70d41f3ee29d453a90efab3ce025d450__section_tn2_dys_ypb"/>

## Migration Steps

1.  Clone your project from git by using the command line or import your project to the workspace as follows:
    -   Click *File* \> *Open Workspace* and create a workspace in the projects folder.

    -   Export the project from SAPSAP Web IDE to your computer.
    -   Unzip the project on your computer.
    -   Drag the project to the workspace of VS Code or SAP Business Application Studio.

2.  Click *Start Migration* from the pop-up window appeared.

    A new *Migration* view opens listing all the projects from your workspace. For each project listed, the type of the project is also displayed. If the tool finds no suitable project for migration in your workspace, a message is shown.

    > ### Tip:  
    > You can also open the Migration view anytime by starting typing `Fiori: Migrate Project for use in Fiori tools` in the *Command Palette*.

3.  Select the project that you want to migrate from the list of projects by selecting the corresponding checkbox. You can choose to manually add a project from the filesystem by clicking [Add Project\]. If the supplied folder has an application that can be migrated, it's added to your list of projects. At any point, you can click the *Refresh* button to reload the projects from your workspace again.
4.  For each listed project, if applicable, fill in the respective columns based on the information provided low:


    <table>
    <tr>
    <th valign="top">

    Name


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Application Identifier


    
    </td>
    <td valign="top">
    
    The identifier of the project from the `manifest.json` or `pom.xml`.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Project Path


    
    </td>
    <td valign="top">
    
    The file path to the location of the project.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    SAP System


    
    </td>
    <td valign="top">
    
    A dropdown detailing the SAP system that should be used in migration. The dropdown lists all the saved systems in VS Code or all the destinations available in SAP Business Application Studio. In SAP Business Application Studio, an entry is preselected if the destination name found in `neo-app.json` matches exactly with a destination available to the user in their subaccount. Selecting an SAP System from the dropdown sets the hostname and client automatically.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Destination


    
    </td>
    <td valign="top">
    
    A free-text field that by default contains the system name from the project being migrated. It should default to the destination from the source project `neo-app.json`. Destination is only used by SAP Fiori tools in SAP Business Application Studio and not in VS Code. To allow a project to be compatible, please provide a Destination and Hostname that is accessible to both. Use a destination for the front-end Server that has SAPUI5 libraries installed rather than connecting to the back-end OData server directly.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Hostname


    
    </td>
    <td valign="top">
    
    An input box detailing the back-end hostname to be used in migration. Should be a valid **URL** or blank. This hostname is only used by SAP Fiori tools in VS Code.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    SAP Client


    
    </td>
    <td valign="top">
    
    An optional numeric field detailing the SAP client to be used in migration. Should be provided in case the client isn’t the system default.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    SAPUI5 Version


    
    </td>
    <td valign="top">
    
    A dropdown detailing the version of SAPUI5 to be used when previewing the migrated application locally. Defaults to the version from `neo-app.json` if defined, otherwise uses the `minUI5Version` in the `manifest.json` file.

    > ### Note:  
    > For SAPUI5 Extensibility Projects, currently the minimum version required is 1.71.0.


    
    </td>
    </tr>
    </table>
    
5.  Click *Start Migration*.

    At this point, your selected projects are migrated and required packages are installed.

    > ### Note:  
    > After the successful migration of the SAP Fiori elements project, you can view the *Application Information* for the respective project. To do so, click *View Info* under the *Action* column of the migration results view. The *Application Information* tab is displayed automatically if only one SAP Fiori elements project is migrated.
    > 
    > To migrate more projects, press the [Back\] button from the results view.
    > 
    > For more details, see [Application Information](../Project-Functions/application-information-c3e0989.md).




<a name="loio70d41f3ee29d453a90efab3ce025d450__section_vkc_m1t_ypb"/>

## Files Updated During Migration

The migration process modifies several files in your existing project. The following table lists the files to be updated during migration.


<table>
<tr>
<th valign="top">

Name



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

`.gitignore`



</td>
<td valign="top">

A new file to be added with the build artifacts and libraries ignored.



</td>
</tr>
<tr>
<td valign="top">

`package-lock.json`



</td>
<td valign="top">

A file deleted and re-created during migration to reflect updated libraries.



</td>
</tr>
<tr>
<td valign="top">

`package.json`



</td>
<td valign="top">

-   Removes SAPUI5 SAP Web IDE specific libraries.
-   Updates the npm scripts with SAP Fiori tooling targets and dependencies.
-   Presence of `sapux:true` and `ui5-tooling` library identifies the project as one that supports SAP Fiori tools.



</td>
</tr>
<tr>
<td valign="top">

`ui5-local.yaml`



</td>
<td valign="top">

A new file that supports offline development, downloads ui5 libraries locally, and runs against mock data.



</td>
</tr>
<tr>
<td valign="top">

`ui5.yaml`



</td>
<td valign="top">

-   Removes the SAP SAP Web IDE builder tasks. SAP Fiori deployment tasks are added later when you add deployment configuration to your project.
-   Reminds of file changes, supports the proxy middleware and live reload functionality.



</td>
</tr>
<tr>
<td valign="top">

`index.html`



</td>
<td valign="top">

A new file supporting a stand-alone preview of your application without SAP Fiori launchpad. Now, you can start your app with or without SAP Fiori launchpad.



</td>
</tr>
<tr>
<td valign="top">

`manifest.json`



</td>
<td valign="top">

It’s populated by SAP Fiori tools. Previously, it was populated by Maven.



</td>
</tr>
<tr>
<td valign="top">

`changes_loader.js`



</td>
<td valign="top">

A new static file that supports live reload of the application.



</td>
</tr>
<tr>
<td valign="top">

`changes_preview.js`



</td>
<td valign="top">

A new static file that supports `.changes` file from adaptation updates.



</td>
</tr>
<tr>
<td valign="top">

`flpSandbox.html`



</td>
<td valign="top">

This file is updated by migration to support the preview and changes loader. The following differences to the old file version can be defined:

-   The migration tool changes the paths to the ui5 libraries so that they’re proxied through the back end and allows the update of the ui5 version at runtime.
-   Updated to recommended config.



</td>
</tr>
<tr>
<td valign="top">

`locate-reuse-libs.js`



</td>
<td valign="top">

A new static file that finds any custom reuse libraries referenced in your manifest file and queries them with the back-end server to see if the libraries are installed. If so, it registers them at runtime so that they’re available.



</td>
</tr>
<tr>
<td valign="top">

`flpSandboxMockServer.html`



</td>
<td valign="top">

Applies the same changes as the `flpSandbox.html` file but with the mock server support.



</td>
</tr>
</table>

> ### Note:  
> If the source project doesn’t contain a `webapp` folder, then one is created during migration and the relevant HTML and JavaScript files are moved to this location.



<a name="loio70d41f3ee29d453a90efab3ce025d450__section_g5b_qpt_ypb"/>

## Verification

1.  Review the file changes in the **Source Control** view. Check for any project-specific changes that may be overwritten and consider reapplying as appropriate.
2.  To ensure your SAP Fiori tools application works as expected, launch any of the SAP Fiori tools commands, such as *Page Map*, *Fiori: Open Application Generator*, or *Fiori: Open Guided Development*.

    > ### Note:  
    > Some SAP Fiori apps might be missing files like `metadata.xml` before migration, which can impact some of the SAP Fiori tools features. To avoid this, after migration, make sure that you sync the `OData` service using *Service Manager* as described here: [Managing Service and Annotations Files](../Project-Functions/managing-service-and-annotations-files-8182ff3.md).


**Related Information**  


[Blog: Migrate SAP Fiori projects from SAP Web IDE to SAP Business Application Studio](https://blogs.sap.com/2022/01/06/migrate-sap-fiori-projects-from-sap-web-ide-to-sap-business-application-studio/)

