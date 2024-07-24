<!-- loioab4657ca9bd84cd6869a750a1d94b5bd -->

# Importing an Application

You can manually import an existing SAP Fiori application from the SAPUI5 ABAP repository to SAP Business Application Studio or VS Code.



<a name="loioab4657ca9bd84cd6869a750a1d94b5bd__section_ffp_qsg_bqb"/>

## Preparation Steps

Before importing an application, in your workspace in either SAP Business Application Studio or VS Code, create new folders with the following names:


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

`restore-from-exported`

</td>
<td valign="top">

This folder contains the restored app.

</td>
</tr>
<tr>
<td valign="top">

`restore-from-exported/webapp`

</td>
<td valign="top">

This folder will contain the content of the downloaded zip/tgz.

</td>
</tr>
</table>



<a name="loioab4657ca9bd84cd6869a750a1d94b5bd__section_kq2_q3k_1qb"/>

## Import Steps

> ### Note:  
> The BSP application code is normally minified before deployment, and so the resulting code that is downloaded is also the minified version. We recommend that you only use this import procedure if the application code is not already available under source control.
> 
> The `-dbg.js` file, for example `(Component-dbg.js)`, contains the original un-minified code. You can copy its contents into the corresponding `.js` file, for example *Component-dbg.js* \> *Component.js* for more human readable code.
> 
> Please remove `-dbg.js`, `-preload.js` and `.js.map` before running UI5 CLI build, otherwise they are recreated in the `dist` folder.

To import SAP Fiori apps from the SAPUI5 ABAP repository, perform the following steps:

1.  Login to your SAPUI5 ABAP back-end system and navigate to the transaction `SE80`.
2.  Run the report `/UI5/UI5_REPOSITORY_LOAD`.
3.  Provide the name of the SAPUI5 application and click *Download*.
4.  Choose an empty folder for the download target.
5.  From the resulting view, download all as a zip using the button *Click here to Download* at the end of the page.
6.  Extract the zip into the folder `restore-from-exported/webapp`.
    -   Verify that the `manifest.json` is located at `restore-from-exported/webapp/manifest.json`.

7.  Create a `package.json` in the folder `restore-from-exported`. The `name` value should match the application name in `manifest.json`.

    ```
    {
       "name": "sap.fe.demo.awesomeapp",
    }
    ```

    You can see the original application name and namespace in the `manifest.json` file. For example:

    ```
    {
    "sap.app": {
    "id": "sap.fe.demo.awesomeapp",
    ..
    }
    ```

8.  In SAP Business Application Studio or VS Code workspace, start the migration command `Fiori: Migrate Project for use in Fiori tools` if not already prompted to do so.
9.  The project should be found in `restore-from-exported` and listed for migration.
10. Choose the appropriate options and migrate the project.
11. Upon successful completion the project should now be compatible with SAP Fiori tools.

