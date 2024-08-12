<!-- loio709f83837b3a4e96a17865baf45e9e2c -->

# Deleting an Application in CAP Project

> ### Note:  
> For more information about CAP services, see: [https://cap.cloud.sap/docs/about/](https://cap.cloud.sap/docs/about/).

You can safely delete an SAP Fiori application created inside CAP projects with the SAP Fiori elements or freestyle SAPUI5 generators. The deletion process will delete the folder containing the application along with all changes in global files, such as references to already invalid annotations in a subfolder.

Perform the following steps:

1.  By using **Command Palette** in VS Code \([CMD\]/[CTRL\] + [Shift\] + [P\]\), execute the *Fiori: Delete Application from CAP project* command.
2.  Select the application you want to delete from the dropdown list of applications available.
3.  A dialog box *Do you really want to delete application <application\_name\>?* with the following options appears:
    -   *Yes*
    -   *No*
    -   *Cancel*

4.  Click *Yes* to delete the required application and revert all changes in global files.

    > ### Note:  
    > If you select either *No* or *Cancel*, the application will remain the same without any changes applied.


