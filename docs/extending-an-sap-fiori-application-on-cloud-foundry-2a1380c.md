<!-- loio2a1380cc08ad434f87f730aff6f39c3c -->

# Extending an SAP Fiori Application on Cloud Foundry

Create an adaptation project from an existing SAPUI5 application created by SAP or provided by SAP Partner, exposed as a business service and available in the Cloud Foundry environment.



<a name="loio2a1380cc08ad434f87f730aff6f39c3c__section_yvc_qdc_t2c"/>

## Context

An adaptation project in the Cloud Foundry environment is actually a module inside an MTA project. Therefore, you either have to create a new blank MTA project beforehand using the SAP Business Application Studio MTA Project Generator, where you can create your adaptation project as a module, or you will need to use an already existing MTA project from your workspace.

Adaptation projects do not support the following applications:

-   A base application with an SAPUI5 version lower than 1.30.
-   A scaffolding application- an application that uses `sap.ca.scfld.md` in its `manifest.json` file
-   An application without a `manifest.json` file
-   An application that requires a mandatory parameter to start
-   An application variant that has already been deployed with an adaptation project
-   An application whose SAPUI5 version in the system is lower than 1.71



## Adaptation Project Prerequisites

-   Before you use a generator or editor for a SAPUI5 Adaptation Project, install the Cloud Foundry CLI. For installation instructions, see the[V8 CLI Installation Guide](https://github.com/cloudfoundry/cli/wiki/V8-CLI-Installation-Guide).



<a name="loio2a1380cc08ad434f87f730aff6f39c3c__businessservices"/>

## Scenario 1: New or Existing MTA Project without an added Business Service

Create a new MTA Project or use an existing MTA project from your workspace. Before using the application of a certain business service as base app in an adaptation project, you need to add it manually to your MTA project.

You need to first create the service instance that you want to reference in the `.yml` file. Your user has to be a member of the Cloud Foundry space that this instance belongs to. You can do this in the Cloud Foundry cockpit, or in SAP Business Application Studio in the *View/Find Command* \> *CF: Create a new service instance* menu.

1.  Create new, or use already existing, MTA project. To create an MTA project, you need to first create an empty folder that will be the main folder of the project, and under it, create a file called `mta.yaml` with the following content:

    ```
    ID: <name-of-the-folder>
    version: 0.0.1
    _schema-version: '3.2'
    
    ```

2.  Add the business service that you want to use to the `mta.yml` file manually, following this pattern:

    ```
    resources:
      - name: {your service name}
        type: {existing/managed service instance type}
        parameters:
          service: {service technical name}
          service-name: {service instance name}
          service-plan: {service instance plan}
    
    ```

    1.  Under the `resources` node, you should add the following structure:
        -   `name` – the name of the service resource, which is referenced from within the MTA

        -   `type` – the type of the existing service instance. Possible values are `org.cloudfoundry.existing-service` or `org.cloudfoundry.managed-service`

    2.  Add a `parameters` node and add the following properties:

        -   `service` – the technical name of the service offering that you want to add. You can find it in the Cloud Foundry service marketplace page as the secondary title for that service.

        -   `service-name` – the name of the instance of the service that is created. You can find it in the column named *Instance* in the table on the service instances page, in the cockpit.
        -   `service-plan` – the plan for the service instance. You can find it in the column named *Plan* in the table on the service instances page, in the cockpit.


        Example:

        > ### Sample Code:  
        > ```
        > resources:
        > - name: risk_service
        > 	type: org.cloudfoundry.existing-service	
        > 	parameters:
        > 		service: grc-risk
        > 		service-name: risk_service
        > 		service-plan: standard
        > 
        > ```





<a name="loio2a1380cc08ad434f87f730aff6f39c3c__section_ljm_5fc_t2c"/>

## Scenario 2: Existing MTA Project with an already added Business Service

Use an existing MTA Project that already includes a Business Service.



<a name="loio2a1380cc08ad434f87f730aff6f39c3c__section_apl_jkw_rxb"/>

## Typical Workflow for Extending an SAP Fiori Application

For both Scenario 1 and Scenario 2 follow the below steps to complete extending the SAP Fiori application:

1.  [Create the Adaptation Project](create-the-adaptation-project-e304922.md).
2.  \(Optional\) Use source control, such as Git, to maintain your project source code.

    It is recommended to use the project source code to preview and modify it.

3.  [Make Adaptations](make-adaptations-3c56e5b.md) to your project.
4.  [Preview the Adaptation Project](preview-the-adaptation-project-29c92fa.md).
5.  [Deploy the Adaptation Project to Cloud Foundry](deploy-the-adaptation-project-to-cloud-foundry-cc728d8.md).

