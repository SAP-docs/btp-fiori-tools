<!-- loio6845fedbb38c4da7a54a2c76081f3abb -->

# Generating an Application with the Project Accelerator Using SAP Fiori Tools AI

You can use the Project Accelerator to generate projects that include SAP Fiori elements applications based on the following programming models:

-   SAP Cloud Application Programming Model \(CAP\)
-   ABAP RESTful Application Programming Model \(RAP\)

The following video shows an overview of the Project Accelerator: [Project Accelerator: Elevate Development with AI​ in SAP Fiori tools](https://dam.sap.com/mac/u/a/b4EL9s7?rc=10&doi=SAP1185906):

[![](images/Project_Accelerator_Video_8a3b039.png)](https://dam.sap.com/mac/u/a/b4EL9s7?rc=10&doi=SAP1185906)



## Using the Project Accelerator with CAP

You can use the Project Accelerator to generate a project based on the SAP Cloud Application Programming Model \(CAP\) by translating your business requirements into a CAP project with a single SAP Fiori elements application.

For CAP-based projects, the Project Accelerator can generate:

-   Data models, services, and mock data.
-   An SAP Fiori elements application.

You can provide your business requirements as text, images, or a combination of both. Depending on your business requirements, the generated CAP application includes:

-   An SAP Fiori elements application with a list report page, one or more object pages, or a form entry object page.

-   Local mock data to support previewing at application runtime.


The generated CAP project does not include any business logic, which can be manually implemented later by CAP developers.



## Using the Project Accelerator with RAP

You can also use the Project Accelerator to generate a project based on the ABAP RESTful Application Programming Model \(RAP\).

For RAP-based projects, the Project Accelerator can generate:

-   An SAP Fiori elements application.

-   A RAP back-end artifact.
-   An OData V4 service endpoint, which is automatically generated and activated.

You can provide your business requirements as text, images, or a combination of both. Depending on the requirements, the generated RAP artifacts include:

-   An SAP Fiori elements application with a list report page and one or more object pages, or a form entry object page.

-   Local mock data to support previewing at application runtime.

-   RAP back-end artifacts created in the SAP BTP, ABAP environment, which are required to expose the OData service used by the application.


The generated RAP project does not include any business logic, which can be manually implemented later by RAP developers.



<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_lsy_b1t_51c"/>

## Prerequisites

Ensure the following prerequisites are met:

-   You have a subscription to SAP Build Code or have signed up for [SAP Build Code Test Drive](https://developers.sap.com/mission.sap-build-code-test-drive.html?sap-outbound-id=4E44C2A19D38B160BF5539329FA7ECC83942C1AD). For more information, see [What is SAP Build Code](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/504854f457cc4fbf9f79136dbc773618.html).

-   You are using SAP Business Application Studio as your integrated development environment \(IDE\).

**CAP**

-   You have created a dev space that contains both SAP Fiori tools and CAP tools extensions.


**RAP**

-   You have created a dev space that contains SAP Fiori Tools.

-   Your RAP back end \(cloud only\), such as SAP BTP ABAP Environment or SAP S/4HANA Public Cloud Edition, must run on version 2602 or higher.

-   The connection to your back-end system \(destination\) is configured in SAP Business Application Studio.

-   You must have the **S\_DEVELOP** authorization to perform operations in your ABAP back-end system.




<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_axr_kk5_gdc"/>

## Procedure

Prepare your business requirements for generating a new application. Your business requirements can consist of text, images, or text and images.

> ### Tip:  
> Field values and restrictions, such as an alphanumeric string, are easier to describe using text. Columns are easier to describe using images.

-   To generate an application using text, proceed with the following: [Generating an Application Using Text](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/e7f9f8c26ebb4ab181372d09bb054cac.html?state=DRAFT).

-   To generate an application using an image, proceed with the following: [Generating an Application Using an Image](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/39193dfef3654ded850d39e7008e77d3.html?state=DRAFT).
-   To generate an application using text and images, proceed with the following: [Generating an Application Using Text and Images](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/5dd43dc5dcab4c36b8a654ce20bac71e.html?state=DRAFT).


> ### Caution:  
> SAP Fiori tools does not filter personal or sensitive data. Therefore, you should not share personal or sensitive data in your business requirements document.



<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_wcj_5ft_51c"/>

## Supported Features

You can define the following features as requirements in your input:



### General Features

**CAP**

The Project Accelerator supports the following CAP-related features:

-   Entities and entity labels.

-   Entity properties and property labels.

-   Entity associations \(1:1 and 1:n\).

-   Entities with code lists based on the explicit values in the user input.

-   Value help based on 1:1 associations and code lists.

-   Criticality highlighting for eligible properties in code lists.


The generated application is draft-enabled by default and supports the following features:

-   A single list report page application.
-   A single application with a list report page and one or multiple object pages.
-   A single application with the form entry object page floorplan.

**RAP**

The Project Accelerator contains the following features for the generated service:

-   Entities
-   Entity type properties
-   Compositions \(created as required\)

The generated application is draft-enabled by default and supports the following features:

-   A single list report page application.
-   A single application with a list report page and one or multiple object pages.
-   A single application with the form entry object page floorplan.
-   Standard actions



### List Report Page Features

The following features are suported for list report page applications in both CAP and RAP:

-   Filter fields

-   Basic table columns

    Features such as charts and icons are not supported.

-   Multiple views for a table in multiple table mode.

    For more information, see [Defining Multiple Views on a List Report Table - Multiple Table Mode](https://ui5.sap.com/sdk/#/topic/37aeed74e17a42caa2cba3123f0c15fc).

-   Initial data load

    For more information, see [Loading Behavior of Data on Initial Launch of the Application](https://ui5.sap.com/#/topic/9f4e1192f1384b85bc160288e17f69c4).




### Object Page Features

The following features are supported for object pages in both CAP and RAP:

-   Section tabs

-   Form sections with basic fields.

-   Table sections with basic columns.

-   Navigation from a table section to a second object page.




## Restrictions

If your request does not contain any instructions for a specific supported feature, the generated app either excludes it, or it is implemented at SAP Fiori tools AI's own discretion. For example, if SAP Fiori tools AI finds no explicit request for the filters in the list report, the app may contain the filter fields of SAP Fiori tools AI's choice.

If your request contains instructions for unsupported features, they are either implemented at SAP Fiori tools AI's own discretion, or are not considered.

If your request only contains text, SAP Fiori tools AI does not generate object page header features based on your specific requirements, but may use the general description of your app to generate some basic header features.

SAP Fiori tools AI uses your input to create UI features such as fields and columns but chooses random values to fill these columns with test data. In addition, data from images you have used to represent the page layout is also used to generate test data. The generated test data is only intended for testing the app in preview mode and is stored in a test folder of the generated project. The only exception is the code lists or enum values that are based on the explicit values from your input. These values are treated as properties of associated entities and stored in a data folder.

By default, all generated apps are draft-enabled and contain standard actions. Other actions are not supported.

To learn more about how SAP Fiori tools AI generates your application, observe the logs. For more information, see [Viewing Generation Logs](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/4ecc286176b1429b98f6f0a243e49ee2.html?state=DRAFT).

**RAP**

-   You can only use the greenfield approach. Existing artifacts in your back end OData services and databases are not used, reused, or referenced in the generated project.
-   Integration with on-premise or private cloud systems is not available. These capabilities are exclusively available on SAP BTP, ABAP environment.
-   Multiple business objects and cross-BO associations are not supported. Multiple entities are connected using compositions.
-   Code lists are not generated. Enum values are not supported.
-   Value help and criticality highlighting is not supported in the generated application.
-   The annotations required for the application UI are stored in the local `annotation.xml` file of the project.
-   Semantic keys are not supported.
-   You cannot automatically remove the artifacts generated in the back end. The application project and artifacts must be removed manually, if no longer needed. For more information, see [Deleting RAP Artifacts Manually](deleting-rap-artifacts-manually-2386ce8.md).
-   Charts and icons are not supported.
-   Custom actions are not supported.

