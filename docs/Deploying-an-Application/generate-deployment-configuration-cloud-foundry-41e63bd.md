<!-- loio41e63bde991a485ea362fc5ba35cf5bc -->

# Generate Deployment Configuration Cloud Foundry



<a name="loio41e63bde991a485ea362fc5ba35cf5bc__section_m3v_5r3_k4b"/>

## Cloud Foundry Prerequisites

-   **[MTA](https://github.com/SAP/cloud-mta) executable in the path**.

    For SAP Fiori tools application deployment to Cloud Foundry, you must install MTA. It is a tool for exploring and validating the multitarget application descriptor \(`mta.yaml` file\). The tool can be used as a Go library, a command line tool, or as an npm package.

    You can install it globally by running the following command:

    ```
    npm i -g mta
    ```

    -   **macOS users**: When installing `MTA`, the following error may occur:

        ```
        Error: EACCES: permission denied, mkdir bin.
        ```

        In this case, permission needs to be altered by using the following command:

        ```
        sudo chown -R $(whoami) FOLDER-NAME
        ```

    -   **Windows users**: To build an MTA archive from a project source code in a Windows environment, install `GNU Make 4.2.1` on your machine. For more information, see [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/makefile).

    For information on adding a project to MTA config, see [SAP Fiori Elements](../Generating-an-Application/SAP-Fiori-Elements/sap-fiori-elements-1488469.md).

-   **Cloud Foundry CLI tools**.

    To access SAP Business Technology Platform, download and install `CF CLI`, which is the official command line client for Cloud Foundry, from the [Cloud Foundry CLI page](https://github.com/cloudfoundry/cli#installers-and-compressed-binaries-1). We recommend that you follow the [installation instructions](https://docs.cloudfoundry.org/cf-cli/install-go-cli.html) when installing `CF CLI` tools.

    -   **Windows users**: You also need to create a `CF_HOME` variable. To do so, perform the following steps:
        1.  Navigate to *Environment Variables*.
        2.  Click *New* under *User Variables*.
        3.  Enter `CF_HOME` as a variable name.
        4.  Set write permission for the directory.
        5.  Click *OK*.
        6.  Close all command line windows.


-   **MultiApps Cloud Foundry plugin**.

    MultiApps Cloud Foundry plugin performs multitarget application \(MTA\) operations in Cloud Foundry, such as deploying, removing, viewing, and more. To install the Multi-Apps Cloud Foundry CLI plugin, execute the following command:

    ```
    cf install-plugin -r CF-Community "multiapps"
    ```

    We recommend that you follow the [installation instructions](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/27f3af39c2584d4ea8c15ba8c282fd75.html) when installing the MTA plugin.

    For more information on Cloud Foundry plugins, see [https://plugins.cloudfoundry.org](https://plugins.cloudfoundry.org).

-   A correctly configured destination to the back-end system.
-   User authorization on Cloud Foundry to deploy.

    To connect to Cloud Foundry, execute

    > ### Code Syntax:  
    > ```
    > cf login -a https://api.cf.sap.hana.ondemand.com
    > ```




<a name="loio41e63bde991a485ea362fc5ba35cf5bc__section_yw1_d53_k4b"/>

## Generate Deployment Configuration Cloud Foundry

For the deployment to Cloud Foundry, an MTA configuration is created. The command allows to create a new configuration i.e. a new `mta.yaml` file or update an existing `mta.yaml` with the information required for deployment. After successfully creating the configuration, running `npm run build` in the MTA directory that contains the application will try to build a deployable `mta.yaml` file that can then be deployed to CF with `npm run deploy`.

To generate a MTA project, perform the following steps:

1.  Launch the deployment configuration wizard from the Command Palette entry: *Fiori: Add Deployment Configuration* and chose the SAP Fiori project you would like to configure, or you can launch from the command line using the command: `npx fiori add deploy-config` whilst in the required Fiori project folder.
2.  When prompted, enter or select:


    <table>
    <tr>
    <th valign="top">

    Prompt
    
    </th>
    <th valign="top">

    Entry
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Choose Target
    
    </td>
    <td valign="top">
    
    Cloud Foundry
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Destination Name
    
    </td>
    <td valign="top">
    
    If the destination name is empty or not the correct target, enter the destination name.
    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > Any instance-based destinations defined in the project `mta.yaml` file will be available as a destination option in SAP Business Application Studio. These destinations will be displayed with the label: *Instance Based Destination* after the destination name.

3.  Next, the installer runs and you can see updates in the project tree.

    > ### Note:  
    > If no `mta.yaml` file is found in the application folder, you will be given the option to create one during deployment configuration.




### Artifacts & configuration created

Running the command/task results in a directory structure that looks similar to the following:

```
mta_directory
|_ application_directory
   |_ ...
   |_ webapp
      |_ ...
      |_ manifest.json
   |_ ui5-deploy.yaml
   |_ ui5.yaml
   |_ xs-app.json
...
|_ package.json
|_ mta.yaml
|_ xs-security.json
```



<a name="loio41e63bde991a485ea362fc5ba35cf5bc__section_gr1_tvd_l4b"/>

## SAP Business Application Studio Cloud Foundry Support

If you do not have an MTA file in your dev space in SAP Business Application Studio, you can use the provided generators to create the required configuration as follows:

1.  Open *File* \> *New Project from Template*.
2.  Select *Basic Multitarget Application*.
3.  Enter a project name, and then click *Finish*.

The IDE opens again with MTA as a workspace. You can then add app router configuration:

1.  Right-click on the newly generated MTA file, and select *Create MTA Module from Template*.
2.  Select *Approuter Configuration* and provide the relevant details and click *Next*.
3.  As a result, the `mta.yaml` file is updated with the destination-content module. For more information, see [Managed Approuter Project Result](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/0e2ec06ee34742fd9054fabe09c12d35/cb57602041e04cd3910e6c7bd613b4a9.html).

After the app router has been added, you can proceed to add your SAP Fiori project:

1.  Right-click on the newly generated MTA file, and select *Create MTA Module from Template*.
2.  Choose the SAP Fiori application generator.
3.  Provide your application details.
4.  By default, deployment configuration will be enabled and added to the existing MTA file after generation.

