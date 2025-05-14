<!-- loio709f83837b3a4e96a17865baf45e9e2c -->

# Deleting an Application in CAP Project

You can safely delete an SAP Fiori application created inside CAP projects with the SAP Fiori elements or freestyle SAPUI5 generators. The deletion process will delete the folder containing the application along with all changes in global files, such as references to already invalid annotations in a subfolder.

> ### Tip:  
> For more information about CAP projects, see [https://cap.cloud.sap/docs/about/](https://cap.cloud.sap/docs/about/).

Perform the following steps:

1.  Open the Command Palette in Visual Studio Code \([CMD\]/[CTRL\] + [Shift\] + [P\]\) and execute the `Fiori: Delete Application from CAP project` command.
2.  Select the application you want to delete from the dropdown list of applications available. A dialog box *Do you really want to delete application <application\_name\>?* with the following options appears:
    -   *Yes*
    -   *No*
    -   *Cancel*

3.  Click *Yes* to delete the application and revert all changes in global files.

