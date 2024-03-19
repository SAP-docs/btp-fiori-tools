<!-- loiodb44d45051794d778f1dd50def0fa267 -->

# Generating an Application



To create an application in VS Code or SAP Business Application Studio, perform the following steps:

1.  Using **Command Palette** in VS Code \([CMD\]/[CTRL\] + [Shift\] + [P\]\), select `Fiori: Open Application Generator` or *Start from template* in SAP Business Application Studio.

    > ### Note:  
    > In SAP Business Application Studio, use one of the following dev spaces, depending on your development needs:
    > 
    > -   SAP Fiori
    > 
    > -   Full-Stack Application Using Productivity Tools
    > 
    > -   Full Stack Cloud Application

2.  The *Template Wizard* appears.

    > ### Note:  
    > SAP Fiori application generator increases development productivity and ensures consistency across your SAP apps by using standard page types to build applications. This generator follows SAP Fiori elements or freestyle SAPUI5 approach to build an SAPUI5 application.

3.  On the *Template Selection* page, select one of the following options from the *Template Type* dropdown list:
    -   SAP Fiori \(default value\)
    -   Deprecated templates \(includes SAPUI5 templates that have been deprecated\)

4.  Click [Next\].

    Based on your selection, the next page appears.


> ### Note:  
> After the SAP Fiori project is generated, the **Application Information** page opens. You can relaunch the **Application Information** page at any time by executing `Fiori: Open Application Info` command.

For MTA deployment, see [Generating an MTA Deployment File](Additional-Configuration/generating-an-mta-deployment-file-9c41152.md) 



<a name="loiodb44d45051794d778f1dd50def0fa267__section_s13_dsd_mqb"/>

## Generating an Application with SAP Business Application Studio Service Center

In the SAP Business Application Studio Service Center, you can explore services from various service providers.

The Service Center displays the services from subaccount destinations and SAP Business Accelerator Hub. The exposed services can be used as a data source for creating an SAP Fiori application.

For more information, see [Service Center](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/1e8ec75c9c784b51a91c7370f269ff98.html).



<a name="loiodb44d45051794d778f1dd50def0fa267__section_iyl_g4d_35b"/>

## Project

Once a project is generated, you can see its structure:

-   `webapp`. Root folder for SAPUI5 based web applications.
-   `.npmrc`. Lists any npm registry configuration updates required for the generated project.
-   `.gitignore`. Specifies files or folder patterns that should be excluded from source control, such as node\_modules.
-   `package-lock.json`. Ensures that the project node dependencies are fixed to the correct versions; helps improve the speed of the node libraries installation routine.
-   `package.json`. The main configuration file for node-based projects.
-   `README.md`. The readme file providing details on the options chosen to generate the application.
-   `ui5-local.yaml`. Supports local development of an application in preview mode.
-   `ui5.yaml`. Ensures that the application generated locally can connect to the supplied data source and supports dynamically updating the version of SAPUI5.
-   `node_modules`. Contains node modules required to install and run the current project locally \(npm install creates and updates the folder\). This folder doesn’t need to be version-controlled.

> ### Note:  
> The generated project structure differs if you select the option “Use a Local CAP Node.js Project” during its generation. In this case, the preview and deployment functionality are provided by the local CAP project. As a result, the `package.json` file has a more basic content and some files aren’t generated, such as `ui5.yaml`, `.npmrc`, and more. Additionally, instead of local `annotation.xml`, an `annotation.cds` file is generated so that annotations are defined in CAP CDS syntax instead of OData EDMX.

For more information about npm, see, [@sap/generator-fiori-elements](https://www.npmjs.com/package/@sap/generator-fiori-elements) and [@sap/ux-ui5-tooling](https://www.npmjs.com/package/@sap/ux-ui5-tooling).



> ### Note:  
> The SAP Fiori application generator now consumes open source libraries for writing the SAP Fiori elements and SAP Fiori freestyle applications. Please see [Fiori elements writer](https://github.com/SAP/open-ux-tools/tree/main/packages/fiori-elements-writer) and [Fiori freestyle writer](https://github.com/SAP/open-ux-tools/tree/main/packages/fiori-freestyle-writer)documentation for more information on these libraries.

> ### Note:  
> In SAP Fiori application generator, when some of the most common errors are shown during project generations, the generator gives an option to end user to launch [Guided Answers Extension by SAP](https://github.com/SAP/guided-answers-extension) and troubleshoot the error based on the solution provided by SAP experts.

