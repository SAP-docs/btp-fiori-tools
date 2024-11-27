<!-- loioc789692fe0fb4aaca5300e3c312d1705 -->

# Preview an Application on External Fiori Launchpad

Learn how to preview an application without redeploying it.

This feature provides the user with the ability to test an application run without its redeployment. Running an application on the existing SAP Fiori launchpad requires the application to be deployed once and configured, so it is visible on the target launchpad.

> ### Note:  
> The SAP Launchpad service on SAP BTP does not support this feature.



<a name="loioc789692fe0fb4aaca5300e3c312d1705__section_fmv_hb5_wqb"/>

## Usage

To run the application on the external SAP Fiori launchpad, perform the following steps:

1.  Open the *Command Palette* \([CMD/CTRL\] + [Shift\] + [P\] \).
2.  Execute the *Fiori: Add FLP Embedded Configuration* command.
3.  Enter the BSP of the deployed application.

    > ### Note:  
    > The BSP needs to be entered in lowercase.

4.  Enter the YAML, which contains the back-end configuration. Usually, it is the`ui5.yaml` file.
5.  Enter the relative link to the SAP Fiori launchpad, such as `sap/bc/ui5_ui5/ui2/ushell/shells/abap/Fiorilaunchpad.html`.
6.  Before starting the preview, you need to build your application first by executing `npm run build`.
7.  To start the application on the existing launchpad, right-click the project folder or any subfolder and click *Preview Application*.
8.  Click *start-embedded*.

The initial load of the application on the external launchpad takes longer than the local preview options. Once the application is loaded and the UI5 resources are cached, the application is loaded quickly.

When a change is made, the application is not refreshed immediately. You need to rebuild the application by executing the `npm run build` command to see the changes on the UI. Once the build is executed, the application running on the external launchpad is automatically refreshed.

