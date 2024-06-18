<!-- loio17efa217f7f34a9eba53d7b209ca4280 -->

# Visual Studio Code

This chapter describes how you can install and start working with Microsoft Visual Studio Code \(also known as VS Code\) and provides links to important step-by-step procedures.

<a name="loio002ae80eac034e6588af81827ab97332"/>

<!-- loio002ae80eac034e6588af81827ab97332 -->

## System Requirements

Ensure that the minimum system requirements for installing VS Code are met. For more information, see [Requirements for Visual Studio Code](https://code.visualstudio.com/docs/supporting/requirements).

-   Before VS Code installation, you must have Node.js installed. Ensure you’re using version 16.18 or higher of Node.js. Furthermore, the version of Node.js you install must also have the corresponding version of npm installed. See [Node.js releases](https://nodejs.org/en/download/releases/) for details on the versions of Node.js marked as LTS, and their associated npm versions.

    > ### Tip:  
    > To check the version of Node.js installed, type `node-v` in the terminal. Similarly, to check the version of npm installed, type `npm -v` in the terminal. Ensure that the npm version and Node.js version are compatible.

    You can download Node.js here: [https://nodejs.org/en/download/](https://nodejs.org/en/download/).

    > For Windows, we recommend installing Node.js using the prebuilt installer if possible, however, it requires administrator access. If this is not possible, perform the following setps:

    **Installing Node.js prebuilt binaries \(Windows only\)**
    1. Download the prebuilt binaries from https://nodejs.org/en/download/prebuilt-binaries
       > if downloading the prebuilt binaries is blocked by your IT policies, then please reach out to your IT department and ask them to download the binaries for you
    3. Extract the content of the downloaded zip to C:\Users\<your_user>\AppData\Local\Programs
    4. Open "Edit Environment Variables for your user account"
    5. Create `NODE_PATH` with value C:\Users\<your_user>\AppData\Local\Programs\<your_node_folder>
    6. Add `%NODE_PATH%` to `PATH`
    ###
    > For Mac OS, we don’t recommend installing Node.js from the executable download. It’s recommended to install Node.js with **[Home Brew](https://brew.sh/)**.

    **Installing Node.js with Home Brew \(Mac OS only\)**

    To install Node.js with [Home Brew](https://brew.sh/), perform the following steps:

    1.  In the terminal, at the command line, enter the following command to install **[Home Brew](https://brew.sh/):**

        ```
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        ```

    2.  Install the required version of Node.js by entering the following command at the command line:

        ```
        brew install node@16
        ```

        Where 16 refers to the version of Node.js you would like to install.

    3.  Before continuing with other installation steps using terminal, close and start a new terminal.

-   The SAP Fiori application generator requires the [MTA tool](https://www.npmjs.com/package/mta) Node.js package \(version 1.0 or higher\) to be installed globally.

    At the command line, enter the following command to install MTA:

    ```
    npm install -g mta
    ```


<a name="loiobdd272ac4d964fbfa59e956460e0e686"/>

<!-- loiobdd272ac4d964fbfa59e956460e0e686 -->

## Cloud Foundry CLI tools

To access Cloud Foundry services from SAP Business Technology Platform, download and install the latest version of Cloud Foundry Command Line Interface \(CF CLI\) by following the [installation instructions](https://docs.cloudfoundry.org/cf-cli/install-go-cli.html).

<a name="loio5701672c35354d5b91759a911eaf1171"/>

<!-- loio5701672c35354d5b91759a911eaf1171 -->

## Prerequisites

Ensure that you have the following scope set in your `npm` configuration. Execute the following command:

```
npm config get @sap:registry
```

One of the following values should be returned:

-   https://registry.npmjs.org
-   undefined

If it is set incorrectly to the `@sap`, open your **`.npmrc`** file in your home directory and remove this entry.

<a name="loio4ce76a049bab42b0843111af4c7dcb4c"/>

<!-- loio4ce76a049bab42b0843111af4c7dcb4c -->

## Set up Visual Studio Code

To set up VS Code, you need to perform the following steps:

1.  Download VS Code from the [Visual Studio Code website](https://code.visualstudio.com/download).

    > ### Note:  
    > To learn how to get started with VS Code, see [https://code.visualstudio.com/docs/setup/setup-overview](https://code.visualstudio.com/docs/setup/setup-overview).
    > 
    > **Windows**: VS Code provides both user and system level setups. If you do not have administrator rights, please chose the user level installation.

2.  You must have a working knowledge of VS Code.

    Using VS Code requires a working knowledge of this environment. We encourage you to use the following resources to obtain answers to your VS Code questions and keep yourself informed:

    -   [Visual Studio Code Basic Layout](https://code.visualstudio.com/docs/getstarted/userinterface#_basic-layout).
    -   [Visual Studio Code Introductory Videos](https://code.visualstudio.com/docs/getstarted/introvideos).

3.  Check if Node.js is already installed. You can check this by executing the following in the VS Code terminal. If you don't get a version number, see above on how to install Node.js.

    ```
    node -v
    ```


<a name="loiof533419b114f476e98b55622eabaf0f7"/>

<!-- loiof533419b114f476e98b55622eabaf0f7 -->

## Install Extensions

1.  Start VSCode

    > ### Note:
    > In restricted IT environments, executing VSCode (or node) might be blocked by your IT department. Please contact your IT department and ask for an exception for both, VSCode and node.

3.  Navigate to *VS Code* \> *Extensions*.

    For more information, see [Install Visual Studio Code extensions](https://code.visualstudio.com/learn/get-started/extensions).

4.  Search for SAP Fiori tools and select *SAP Fiori tools - Extension Pack*.

    Alternatively, you can navigate to [SAP Fiori tools - Extension Pack](https://marketplace.visualstudio.com/items?itemName=SAPSE.sap-ux-fiori-tools-extension-pack) and click [Install\].

5.  Click [Install\].
6.  Then, the SAP Fiori tools install the latest release of the following extensions:

    -   Application Wizard
    -   SAP Fiori Tools – Application Modeler
    -   SAP Fiori tools - Guided Development
    -   SAP Fiori tools - Service Modeler
    -   SAP Fiori tools - XML Annotation Language Server
    -   XML Toolkit

    You can also install each extension separately.

    > ### Note:  
    > SAP CDS Language Support is an optional extension that can be installed for annotation LSP in CAP CDS. For more information, see [CDS Editor](https://cap.cloud.sap/docs/get-started/tools/#cds-editor).




<a name="loiof533419b114f476e98b55622eabaf0f7__section_mp4_xfh_3qb"/>

## SAP CDS Language Support

For applications based on CAP, you can install **SAP CDS Language Support** extension. To do so, perform the following steps:

1.  Open [SAP CDS Language Support extension page](https://marketplace.visualstudio.com/items?itemName=SAPSE.vscode-cds#overview) in Visual Studio Marketplace.
2.  Click [Install\] to open a new page with the **SAP CDS Language Support** extension in VS Code.
3.  On the VS Code page, click *Install* to enable the extension.

For more information, see [Add CDS Editor](https://cap.cloud.sap/docs/get-started/tools/#add-cds-editor) and [CDS Editor](https://cap.cloud.sap/docs/get-started/tools/#cds-editor).



<a name="loiof533419b114f476e98b55622eabaf0f7__section_h4f_1gh_3qb"/>

## UI5 Language Assistant Support

**UI5 Language Assistant Support** is an openSource extension that can be optionally installed to perform control ID checks when `flexEnabled` property is set to true in the `manifest.json` file for either SAP Fiori elements or SAPUI5 freestyle projects. It also provides additional support for relevant filters to suggestions and text for ease of use.

To install the UI5 Language Assistant Support extension or read about what features it supports, click *Install* in the [UI5 Language Assistant VS Code marketplace](https://marketplace.visualstudio.com/items?itemName=SAPOSS.vscode-ui5-language-assistant&ssr=false#overview) page.

<a name="loio7b329a74721047808368fca5c28702c3"/>

<!-- loio7b329a74721047808368fca5c28702c3 -->

## Supported Authentication Type

The following are supported authentication types with SAP Fiori tools running in VS Code.


<table>
<tr>
<th valign="top">

Authentication Type



</th>
<th valign="top">

SAP on-Premise



</th>
<th valign="top">

SAP BTP, ABAP Environment



</th>
<th valign="top">

SAP BTP, Cloud Foundry



</th>
<th valign="top">

SAP S/4HANA Cloud



</th>
</tr>
<tr>
<td valign="top">

OAuth 2.0 \([Client Credentials](https://help.sap.com/viewer/38c3df3f8da44a809f937220b3579607/Cloud/en-US/efdfb3a299904c9bb16948a53b6d8b16.html)\)



</td>
<td valign="top">

No



</td>
<td valign="top">

Yes



</td>
<td valign="top">

No



</td>
<td valign="top">

No



</td>
</tr>
<tr>
<td valign="top">

Basic Authentication



</td>
<td valign="top">

Yes



</td>
<td valign="top">

No



</td>
<td valign="top">

Yes



</td>
<td valign="top">

No



</td>
</tr>
</table>

We recommend using SAP Business Application Studio for the extensive support of the authentication types especially when your required authentication type that is not supported in VS Code. Please refer to this Note:[0002577263](https://me.sap.com/notes/0002577263) for more information.

If applicable, disable `SAML` for selected `OData` services. Below are the list of `OData` services:


<table>
<tr>
<th valign="top">

OData Services



</th>
<th valign="top">

Path



</th>
</tr>
<tr>
<td valign="top">

OData V2 catalog



</td>
<td valign="top">

/sap/opu/odata/IWFND/CATALOGSERVICE;v=2



</td>
</tr>
<tr>
<td valign="top">

OData V4 catalog \(dev\)



</td>
<td valign="top">

/sap/opu/odata4/iwfnd/config/default/iwfnd/catalog/0001



</td>
</tr>
<tr>
<td valign="top">

OData V4 catalog \(prod\)



</td>
<td valign="top">

/sap/opu/odata4/iwfnd/config/default/iwfnd/catalog/0002



</td>
</tr>
<tr>
<td valign="top">

ATO Catalog



</td>
<td valign="top">

/sap/bc/adt/ato/settings



</td>
</tr>
<tr>
<td valign="top">

SAPUI5 repository service \(for deploy & undeploy\)



</td>
<td valign="top">

/sap/opu/odata/UI5/ABAP\_REPOSITORY\_SRV



</td>
</tr>
</table>

