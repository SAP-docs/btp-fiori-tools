<!-- loio9c41152c5b8d4a658d7ef9f318b28917 -->

# Generating an MTA Deployment File

In the MTA deployment scenario, developers can generate an app router configuration, that contains the `mta.yaml` file, and then add multiple generated SAP Fiori apps to the app router configuration project. To do so, open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori: Open CF Application Router Generator` command.

![](images/Application_Router_Generator_c4b6125.png)

The user can manage the source code of the app router configuration and multiple SAP Fiori elements projects under a single root directory.

The app router configuration project has the following structure:

-   `router` - The folder that contains the app router configuration.

    > ### Note:  
    > This folder can have a different name, such as `configurable`.

-   `.gitignore` - The file that contains the list of files to be ignored by source control.
-   `mta.yaml` - The file that contains the MTA configuration.
-   `package-lock.json` - The file is generated automatically for any operations where npm modifies either the `node_modules` tree or `package.json` file and describes the exact tree that was generated.
-   `package.json` - The file that contains specifics of `npm package.json`.

Once the app router configuration project is generated, one or more SAP Fiori apps can be generated inside its root directory by using the SAP Fiori application generator.

> ### Note:  
> There are the following router types: managed, Application Frontend service, and standalone. For more information, see [SAP Tech Bytes: FAQ Managed Approuter vs. Standalone Approuter](https://blogs.sap.com/2021/05/17/sap-tech-bytes-faq-managed-approuter-vs.-standalone-approuter/) or [Developing HTML5 Applications in the Cloud Foundry Environment](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/11d77aa154f64c2e83cc9652a78bb985.html).

