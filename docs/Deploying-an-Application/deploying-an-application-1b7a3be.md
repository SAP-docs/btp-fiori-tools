<!-- loio1b7a3be8d99c45aead90528ef472af37 -->

# Deploying an Application



<a name="loio1b7a3be8d99c45aead90528ef472af37__section_azt_3pj_34b"/>

## Deployment Overview

SAP Fiori tools support deployment to ABAP as well as deployment to Cloud Foundry \(CF\) on SAP Business Technology Platform. In contrast to the SAP Web IDE approach, the deployment target isn't required during the application generation which allows a simplified user experience when the project is first created. This approach means that the decision could be deferred until when the developer is ready to deploy the application.



<a name="loio1b7a3be8d99c45aead90528ef472af37__section_lvz_4nw_3nb"/>

## Deploying to ABAP

**Prerequisite**. Ensure all prerequisites are met when using an [OData service to load data to the SAPUI5 ABAP](https://ui5.sap.com/#/topic/a883327a82ef4cc792f3c1e7b7a48de8) repository.

For deployment to ABAP, the SAPUI5 Repository service exposed by the ABAP system is used to upload a deployment artifact. The ABAP backend provides all functionality to run the application, such as hosting, routing, and authentication. As a result, the deployment artifact is just an SAP Fiori application. In other words, it's a zipped dist folder of the SAP Fiori tools project.

For more information see, [Deployment to ABAP](deployment-of-application-607014e.md#loio607014e278d941fda4440f92f4a324a6__abap)



<a name="loio1b7a3be8d99c45aead90528ef472af37__section_qy3_2qj_34b"/>

## Deploying to SAP Business Technology Platform Cloud Foundry

Similar to the SAPUI5 Repository service in ABAP, SAP Business Technology Platform offers an HTML5 Repository to upload and host application. To access the HTML5 Repository, it is required to create an instance of an HTML Repository service. All other functionality required for running the application in an ABAP system comes out of the box and needs to be made accessible by creating instances of the corresponding services.



### Deployment Process

The process to deploy the application involves the following steps:

-   Generate deployment configurations
    -   [Generate Deployment Configuration ABAP](generate-deployment-configuration-abap-c06b9cb.md)
    -   [Generate Deployment Configuration Cloud Foundry](generate-deployment-configuration-cloud-foundry-41e63bd.md)
    -   [SAP Fiori Launchpad Configuration](sap-fiori-launchpad-configuration-bc3cb89.md)

-   [Deployment of Application](deployment-of-application-607014e.md)



<a name="loio1b7a3be8d99c45aead90528ef472af37__section_qxm_mtm_ylb"/>

## Troubleshooting Tips

The backend system contains the SAP\_UI component version 7.53 or newer, but the SAPUI5 repository service can't be reached.

-   Check if the service is activated. For more information, see [Using an OData Service to Load Data to the SAPUI5 ABAP Repository](https://ui5.sap.com/#/topic/a883327a82ef4cc792f3c1e7b7a48de8).

The SAPUI5 repository service is active and reachable but whenever I deploy an application, I see the following error ***Request failed with status code 400***.

-   This could have multiple reasons, check the console for more information, or open transaction `/IWFND/ERROR_LOG` and check the server logs. A common issue is that during the setup, configuring a virus scan profile is forgotten. This can be corrected in the transaction `/IWFND/VIRUS_SCAN`.

> ### Note:  
> You can retrieve more detailed logging information when deploying to ABAP by executing the following commands during deployment.
> 
> -   For detailed log messages from the backend services during deployment:
> 
>     **MacOs/Linux:** `DEBUG=ux-odata-client npm run deploy`
> 
>     **Windows:** `set DEBUG=ux-odata-client & npm run deploy`
> 
> -   For detailed log messages from archiving and deploying the artefacts:
> 
>     **MacOs/Linux:** `DEBUG=ux-odata-client npm run deploy`
> 
>     **Windows:** `set DEBUG=ux-odata-client & npm run deploy`

> ### Note:  
> For any issues, create an incident in **SAP Support Portal** for the component **CA-UX-IDE**.



<a name="loio1b7a3be8d99c45aead90528ef472af37__section_bzw_kmr_brb"/>

## SAP Fiori tools CLI help

SAP Fiori tools CLI offers additional help options to find more information about the various commands and their options for deployment plus other commands.

-   Execute the following command to list all the available commands: `npx fiori help`.
-   Execute the following command to get the details about a specific command. For example, deploy: `npx fiori deploy help`.

