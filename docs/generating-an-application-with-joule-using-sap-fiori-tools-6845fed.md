<!-- loio6845fedbb38c4da7a54a2c76081f3abb -->

# Generating an Application with Joule Using SAP Fiori Tools

Joule, SAP's AI copilot, enables you to generate data models, services, sample data for your project with simple language descriptions, as well as an SAP Fiori UI based on your business requirements document.

You can use Joule to kick-start your SAP Fiori development by directly translating your business requirements into a CAP project with a single SAP Fiori elements application. The generated application can consist of just a list report, or a list report page with one or multiple object pages or a form entry object page.



<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_lsy_b1t_51c"/>

## Prerequisites

Ensure the following prerequisites are met:

-   You have a subscription to SAP Build Code. For more information, see [What is SAP Build Code](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/504854f457cc4fbf9f79136dbc773618.html).

-   You have created a dev space of type *Full-Stack Application Using Productivity Tools*.

-   You have created a *Full-Stack Project* in the dev space.




<a name="loio6845fedbb38c4da7a54a2c76081f3abb__section_dbw_jbt_51c"/>

## Procedure

1.  Launch Joule using SAP Fiori tools through one of the following options:

    1.  Command Palette

        Launch the command palette in SAP Business Application Studio and enter the command `Fiori tools AI: Show Fiori tools Joule`.

    2.  Guide Center

        1.  Select the *Guide Center* tool on the left-hand side and expand the *Guides* node.

        2.  Expand the *Generative AI-Powered Development* node and then the SAP Fiori*UI* node.

        3.  Expand the *Create an*SAP Fiori*Application Directly from Your Business Requirement* node.

        4.  Click the *Open Joule* button to launch Joule's AI assistant for SAP Fiori tools.


    > ### Note:  
    > Once you’ve opened Joule, your query must be related to generating an SAP Fiori elements application – you can’t make any general requests to the AI assistant.

2.  Prepare your business requirements document for generating a new application. To get started, see [Example 1: Manage Contracts and Customer Information in the System](example-1-manage-contracts-and-customer-information-in-the-system-c1bccf2.md) and [Example 2: Display Customers with Related Contracts](example-2-display-customers-with-related-contracts-a6c978f.md).

3.  Paste your business requirements document following the pattern provided in the examples.

    > ### Note:  
    > Please ensure your request refers to a single app only.
    > 
    > Please note that Joule cannot generate a second app for the same project.

4.  Click *Send* in Joule.

    Joule now checks your input against the list of features it supports and implements them.

5.  Click *Show Result* to review the generated artifacts.

6.  You can optionally select *Preview App* to launch a preview of the application in a browser window to help determine if it meets your expectations.

7.  If you are happy with the generated application, accept the changes by clicking the *Accept Files* button to move the project into your file system.

8.  Once the project has been moved into your file system, you can launch the command palette and enter the command `Fiori: Preview Application`. Then choose the associated watch script for the new application.


If your request does not contain any instructions for the specific supported feature, the generated app will either not include it, or it will be implemented at Joule's own discretion. For example, if Joule finds no explicit request for the filters in the list report, the app may contain the filter fields of Joules choice.



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

-   Table

-   Multiple views for a table

-   Initial data load




### Object Page Features

-   Section tabs

-   Form sections and fields

-   Table sections

-   Navigation from table section to second object page


> ### Tip:  
> It’s possible that Joule occasionally misunderstands parts of your requirements, or misses a contained feature request. If this happens, please click *Regenerate* to try again, or click the pencil icon, rephrase your input and click *Submit*.

