<!-- loio6845fedbb38c4da7a54a2c76081f3abb -->

# Generating an Application with the Project Accelerator or Joule Using SAP Fiori Tools AI

You can use the Project Accelerator from SAP Fiori tools AI, or Joule, to generate data models, services, sample data, and an SAP Fiori UI for your project based on your business requirements.

You can use the Project Accelerator or Joule to kick-start your SAP Fiori development by directly translating your business requirements into a CAP project with a single SAP Fiori elements application. Your business requirements can consist of text, images, or text and images. The generated application can consist of just a list report, a list report page with one or multiple object pages, or a form entry object page.

The following video shows an overview of the Project Accelerator: [Project Accelerator: Elevate Development with AI​ in SAP Fiori tools](https://dam.sap.com/mac/u/a/b4EL9s7?rc=10&doi=SAP1185906).[![](images/Project_Accelerator_Video_8a3b039.png)](https://dam.sap.com/mac/u/a/b4EL9s7?rc=10&doi=SAP1185906)

> ### Tip:  
> The Project Accelerator no longer has a staging area to approve the generated project. Instead, it automatically creates a project in the project folder that you choose.



<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_lsy_b1t_51c"/>

## Prerequisites

Ensure the following prerequisites are met:

-   You have a subscription to SAP Build Code or have signed up for [SAP Build Code Test Drive](https://developers.sap.com/mission.sap-build-code-test-drive.html?sap-outbound-id=4E44C2A19D38B160BF5539329FA7ECC83942C1AD). For more information, see [What is SAP Build Code](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/504854f457cc4fbf9f79136dbc773618.html).

-   You have created a dev space that contains both SAP Fiori tools and CAP tools extensions.

-   You are using SAP Business Application Studio as your integrated development environment \(IDE\).



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

-   Entities and entity labels

-   Entity properties and property labels

-   Entity associations \(1:1 and 1:n\)

-   Entities with code lists based on the explicit values in the user input

-   Value help based on 1:1 associations and code lists

-   Criticality highlighting for eligible properties in code lists

-   A single list report application

-   A single application with a list report and one or multiple object pages

-   A single application with the Form Entry Object Page floorplan




### List Report Features

-   Filter fields

-   Basic table columns

    Features such as charts and icons are not supported.

-   Multiple views for a table in multiple table mode

    For more information, see [Defining Multiple Views on a List Report Table - Multiple Table Mode](https://ui5.sap.com/sdk/#/topic/37aeed74e17a42caa2cba3123f0c15fc).

-   Initial data load

    For more information, see [Loading Behavior of Data on Initial Launch of the Application](https://ui5.sap.com/#/topic/9f4e1192f1384b85bc160288e17f69c4).




### Object Page Features

-   Section tabs

-   Form sections with basic fields

-   Table sections with basic columns

-   Navigation from table section to second object page


If your request does not contain any instructions for a specific supported feature, the generated app will either exclude it, or it will be implemented at SAP Fiori tools AI's own discretion. For example, if SAP Fiori tools AI finds no explicit request for the filters in the list report, the app may contain the filter fields of SAP Fiori tools AI's choice.

If your request contains instructions for unsupported features, they will either be implemented at SAP Fiori tools AI's own discretion, or not be considered.

If your request only contains text, SAP Fiori tools AI does not generate object page header features based on your specific requirements, but may use the general description of your app to generate some basic header features.

SAP Fiori tools AI uses your input to create UI features such as fields and columns but chooses random values to fill these columns with test data. In addition, data from images you have used to represent the page layout is also used to generate test data. The generated test data is only intended for testing the app in preview mode and is stored in a test folder of the generated project. The only exception is the code lists or enum values that are based on the explicit values from your input. These values are treated as properties of associated entities and stored in a data folder.

By default, all generated apps are draft-enabled and contain standard actions. Other actions are not supported.

To learn more about how SAP Fiori tools AI generates your application, observe the logs. For more information, see [Viewing Generation Logs](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/4ecc286176b1429b98f6f0a243e49ee2.html?state=DRAFT).

