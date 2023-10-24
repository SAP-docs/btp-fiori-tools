<!-- loioceb845a45dd94f4c8bd52f2976f99090 -->

# Developer Variant Creation

With variant creation provided by SAP Fiori tools, developers can create variants for applications or individual tables, which can be distributed together with the application. The variants are stored as SAPUI5 flexibility changes in the project's `webapp/changes` folder and packaged with the application during the build step.

> ### Note:  
> Variants store view settings, such as filter settings or control parameters. On the UI, these variants are referred to as views.

The feature is delivered with the `@sap/ux-ui5-tooling` node module and its preview feature. Developer variant creation is supported from the SAPUI5 version 1.90 \(OData V2 based applications\) and 1.84 \(OData V4 based applications\). Currently, `@sap/ux-ui5-tooling` supports only ABAP service- based projects.

To create development variants for your Fiori project with SAP Fiori tools perform the following steps:

1.  Execute the `start-variants-management` from the *Preview Application* context menu.

    In case this script is not present, configure the feature for the first time:

    -   Open the Command Palette [Ctrl\] + [Shift\] + [P\] .
    -   Use the `Fiori: Add Configuration for Variants Creation` command.

2.  After the script is executed, a new browser tab appears. It displays the preview of the application switched to the UI adaptation mode.
3.  For creating developer variants, follow the steps described in [Creating and Adapting Views](https://help.sap.com/viewer/DRAFT/6583b46f6c164aad818a3891bc91d8d8/dev_internal/en-US/91ae3492323b42a79ca66fbfaf5af3f9.html).

    > ### Note:  
    > Visibility and role assignment are not supported for developer variants.

4.  Click *Save & Exit* to save the changes.
5.  For each new variant, one or multiple SAPUI5 change files are created in the `webapp/changes` folder of your project. You can open each file and replace static texts of your application with translatable text, such as `{i18n>textKey}` and maintain the text in the corresponding `i18n` file of your project.

> ### Note:  
> For more technical information see [`@sap/ux-ui5-tooling`](https://www.npmjs.com/package/@sap/ux-ui5-tooling#4-preview)

