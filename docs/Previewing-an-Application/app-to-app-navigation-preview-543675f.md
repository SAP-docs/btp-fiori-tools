<!-- loio543675ffa6e54564a0b9e63cd400c008 -->

# App-to-App Navigation Preview



With the *Fiori: Enable App-to-App Navigation Preview* command, you can enable the preview function to follow a configured external navigation from one application to another if both applications are located in the same workspace.

For more information on configuring external navigation with SAP Fiori elements, see [link](https://sapui5.hana.ondemand.com/sdk/#/topic/1d4a0f94bfee48d1b50ca8084a76beec).

1.  Open the *Command Palette* \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the *Fiori: Enable App-to-App Navigation Preview* command.
2.  Select the source application from where the navigation shall originate.
3.  Select the target application to which the navigation shall lead.

    As a result, the following message is displayed: App-to-App Navigation enabled.

4.  Start the preview of the source application and follow the configured external navigation.

The command generates a new `appconfig/fioriSandboxConfig.json` file in the source application folder and updates the `ui5.yaml` file. You can add multiple target navigations to the same source application.

