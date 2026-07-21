<!-- loioece91bcf4aba45568acbfa694cc2901c -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Using the Card Editor When Previewing Your Application

You can use the Card Editor to create cards when previewing a CAP Node.js project or an ABAP-based application.



## Prerequisites

-   You have a CAP Node.js project or ABAP-based application. CAP Java is not supported.
-   You are using the minimum SAPUI5 version 1.149 or above for CAP Node.js projects or 1.121 or above for ABAP-based applications.
-   **CAP Node.js**: The `cds-plugin-ui5` node module is installed in the root `package.json` file.

    This requires CDS workspace mode and the `@sap/cds` node module 6.8.2 and above to be installed.

-   **CAP Node.js**: You have registered the `fiori-tools-proxy` middleware in the `ui5.yaml` file with the paths configured under the `ui5.path` property, for example, `/resources` and `/text resources`, as shown in the following sample code:

    > ### Sample Code:  
    > `ui5.yaml`
    > 
    > ```
    > - name: fiori-tools-proxy
    >       afterMiddleware: compression
    >       configuration:
    >         ignoreCertErrors: false # If set to true, certificate errors are ignored, for example, self-signed certificates are accepted
    >         ui5:
    >           path:
    >             - /resources
    >             - /test-resources
    >           url: https://sapui5.hana.ondemand.com
    > ```




## Adding the Card Editor Configuration

To add the configuration for the Card Editor to your project, proceed as follows:

1.  Open the *Application Info* page.
2.  Under *Configuration*, click *Add for Card Editor*.

The `npx --yes @sap-ux/create@latest add cards-editor` command runs and performs the following changes:

-   The `fiori-tools-preview` middleware is added to the `ui5.yaml` file and a `cardGenerator` entry is added to the `configuration.editors` property.
-   A `start-cards-generator` script is added to the root `package.json` file.



## Using the Card Editor

To use the Card Editor, click <span class="SAP-icons-V5"></span> \(*Refresh*\) next to *Application Info* and then perform the following:

1.  Under *Manage*, click *Open Card Editor*.

    The npm script to start the Card Generator runs and the application preview opens in a new tab in your browser.

2.  Click the *User Menu*, which is a colored circle with your initials, and select :heavy_plus_sign: *Generate Card*.

    The *Select: Service Details* dialog opens.

3.  **\(Optional\)**: You can select a different *Service* from the one that is pre-selected.
4.  Select an *Entity Set Path*.
5.  Select a *Context Path*.
6.  Click *Apply*.

The card is generated and displayed.

