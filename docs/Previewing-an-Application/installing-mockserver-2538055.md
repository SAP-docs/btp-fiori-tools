<!-- loio253805578f04461a9741983a630ce4f1 -->

# Installing MockServer



<a name="loio253805578f04461a9741983a630ce4f1__installmockserver"/>

## Installing Mock Server

> ### Note:  
> For a new project that is created with SAP Fiori application generator the mock server configuration is automatically added. For more information, see [Capabilities Overview](../Getting-Started-with-SAP-Fiori-Tools/capabilities-overview-f540ae1.md).

If you haveve created a project and want to install mock server, you can either:

-   Execute: *Fiori: Open Application Info*.

    -   Under *What you can do*, click *Add Mock server Config*.

-   In the project root, open the terminal, and run the `npx @sap-ux/create add mockserver-config` command. For more information on opening the terminal, see [Use Mock Data](use-mock-data-bda83a4.md).

    > ### Note:  
    > To remove mock server, run the `npx @sap-ux/create remove mockserver-config` command.


Once the mock server is installed, the following configuration is included in your application:

-   `package.json` includes `start-mock`script.
-   `package.json` includes [`@sap-ux/ui5-middleware-fe-mockserver`](https://www.npmjs.com/package/@sap-ux/ui5-middleware-fe-mockserver) as `devDependency` and `UI5` dependency.
-   `ui5-mock.yaml` file is included in your project.

You can use the `Add Mock server Config` to update an outdated or missing mock server configuration in your project. This allows you to ensure that your mock server is configured correctly and is up to date. For more information on the available commands, you can run the command `npx @sap-ux/create help` in your project root terminal.

