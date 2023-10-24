<!-- loio543675ffa6e54564a0b9e63cd400c008 -->

# App-to-App Navigation Preview



With the command `Fiori: Enable App-to-App Navigation Preview`, you can enable the preview function to follow a configured external navigation from one application to another if both applications are located in the same workspace.

To learn how to configure external navigation with SAP Fiori elements, follow this [link](https://sapui5.hana.ondemand.com/sdk/#/topic/1d4a0f94bfee48d1b50ca8084a76beec).

1.  In VS Code \([CMD\]/[CTRL\] + [Shift\] + [P\]\) or SAP Business Application Studio, open **Command Palette** and enter *Fiori: Enable App-to-App Navigation Preview*.
2.  Select the source application from where the navigation shall originate.
3.  Select the target application to which the navigation shall lead.

    As a result, the following message is displayed: **App-to-App Navigation enabled**.

4.  Start the preview of the source application and follow the configured external navigation.

The command generates a new configuration `appconfig\fioriSandboxConfig.json` to the source application folder and updates the `ui5.yaml` file. Also, it is possible to add multiple target navigations to the same source application.

