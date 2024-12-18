<!-- loio70872c402edd425d8612ea722ad81287 -->

# Undeploy an Application

SAP Fiori tools support undeployment from ABAP systems as well as undeployment from Cloud Foundry \(also known as CF\) on the SAP Business Technology Platform.



<a name="loio70872c402edd425d8612ea722ad81287__section_mr1_m14_5pb"/>

## Undeployment from ABAP

To undeploy an application that is deployed to an ABAP system, perform the following steps:

1.  In the terminal, within your project, execute the following command:

    ```
    npm run undeploy
    ```

2.  When prompted, check undeployment configuration and press `Y` \(Yes\) for confirmation.

    > ### Tip:  
    > If a `package.json` file does not contain an undeployment script, update `@sap/ux-ui5-tooling` and add the following script to the `package.json` file:
    > 
    > ```
    > "undeploy": "fiori undeploy --config ui5-deploy.yaml"
    > ```




### Undeploy an application from outside a specific project

To undeploy an application from outside a specific project, replace a placeholder and enter the command depending on the environment you work in.

-   In VS Code, execute the following command:

    ```
    npx @sap/ux-ui5-tooling fiori undeploy --url <Target_ABAP_system_url> --name <Application_name> --transport <Transport_request> --client <Client_number> --noConfig
    ```

-   In SAP Business Application Studio, execute the following command:

    ```
    npx @sap/ux-ui5-tooling fiori undeploy --destination <Destination_name> --name <Application_name> --transport <Transport_request> --client <Client_number> --noConfig
    ```


To find the correct values for each command, see the `ui5-deploy.yaml` file in your application.



<a name="loio70872c402edd425d8612ea722ad81287__section_sj2_hz4_5pb"/>

## Undeployment from Cloud Foundry

To undeploy an application from Cloud Foundry, perform the following steps:

1.  Connect to Cloud Foundry:

    ```
    cf login -a
    ```

    For more information, see [https://api.cf.sap.hana.ondemand.com/](https://api.cf.sap.hana.ondemand.com/).

2.  In the terminal, execute the following command:

    ```
    cf undeploy <mta-id> --delete-services --delete-service-keys
    ```


