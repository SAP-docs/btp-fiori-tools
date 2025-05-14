<!-- loio630ddec5190344d6b9c8d6447085f8a1 -->

# Convert a Project to Use Virtual Endpoints

Using virtual endpoints allows developers to focus on developing applications. Virtual endpoints are automatically kept up-to-date with new package versions and best practises.



<a name="loio630ddec5190344d6b9c8d6447085f8a1__prereq_tlp_3r4_c2c"/>

## Prerequisites

-   You have `SAPUI5 CLI` version 3.0.0 or higher installed. For more information, see [Migrate to v3](https://sap.github.io/ui5-tooling/v3/updates/migrate-v3).
-   If you have `@sap/ux-ui5-tooling` installed, it must be version 1.15.4 or higher.
-   You have `@sap-ux/ui5-middleware-fe-mockserver` or `cds-plugin-ui5` installed.
-   If you use `sap/ui/core/util/MockServer` or `@sap/ux-ui5-fe-mockserver-middleware`, you must migrate to `@sap-ux/ui5-middleware-fe-mockserver`. For more information, see [@sap-ux/ui5-middleware-fe-mockserver](https://www.npmjs.com/package/@sap-ux/ui5-middleware-fe-mockserver).
-   If you use `@sap/grunt-sapui5-bestpractice-build`, you must migrate to `@ui5/cli`. For more information, see [@ui5/cli](https://www.npmjs.com/package/@ui5/cli).



<a name="loio630ddec5190344d6b9c8d6447085f8a1__section_lnc_byj_f2c"/>

## Context

Use the `sap-ux` converter to convert your project to use virtual endpoints. The converter renames the local HTML files, deletes the JavaScript, TypeScript, and test files used for the existing preview functionality, and configures virtual endpoints instead. For more information, see [sap-ux convert preview-config](https://github.com/SAP/open-ux-tools/blob/f07ab9c3010c1cb9828cbf0cb0e730cc3313b4fe/packages/create/README.md#preview-config).

To convert your application to use virtual endpoints, perform the following steps:



<a name="loio630ddec5190344d6b9c8d6447085f8a1__section_bxl_hyj_f2c"/>

## Procedure

1.  Launch the converter using one of the following options:
    1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori: Convert Preview Config` command.
    2.  Open *Application Info* and click *Convert Preview Config*.

2.  Press [Y\] to simulate the conversion or [N\] to convert the project.
3.  Press [Y\] to convert the test runners or [N\] to decline.



<a name="loio630ddec5190344d6b9c8d6447085f8a1__result_egy_ys4_c2c"/>

## Results

Your application has been converted to use virtual endpoints. For more information about the conversion, see the output in the terminal.

> ### Tip:  
> If you have modified the local HTML files, such as `flpSandbox.html`, move the modified content to a custom init script for the preview middleware. For more information, see [preview-middleware - Migration](https://github.com/SAP/open-ux-tools/blob/f07ab9c3010c1cb9828cbf0cb0e730cc3313b4fe/packages/create/README.md#sap-ux-convert). If you have not modified the local HTML files, you can delete them.

