<!-- loiof09752ebcf63473e9194ea29ca232e56 -->

# Developing SAP Fiori Elements Applications with SAP Fiori Tools

SAP Fiori tools provides a fast and convenient way to create and maintain SAP Fiori elements applications.

Here are some of the most important features provided by SAP Fiori tools:

-   Generate SAP Fiori elements applications as standalone projects or within CAP projects, using one of the SAP Fiori elements floorplans or a custom layout that both contain building blocks. For more information, see [Generating an Application](Generating-an-Application/generating-an-application-db44d45.md).

-   Preview your application during development with live or mock data. For more information, see [Previewing an Application](Previewing-an-Application/previewing-an-application-b962685.md).

-   Add, delete, and configure pages, navigation, and consumed services of your application. For more information, see [Developing an Application](Developing-an-Application/developing-an-application-a9c0043.md).

-   Modify manifest and annotation-based settings using a schematic overview of your applications. For more information, see [Visualizing Annotations with Service Modeler](Developing-an-Application/visualizing-annotations-with-service-modeler-58784b5.md).

-   Use intelligent code assistance when writing annotations with the annotation LSP. For more information, see [Maintaining Annotations with Language Server](Developing-an-Application/maintaining-annotations-with-language-server-6fc93f8.md).

-   Learn how to add new features to your application with guided development. For more information, see [Use Feature Guides](Developing-an-Application/use-feature-guides-0c9e518.md).

-   Use AI-powered generation and modification assistants. For more information, see [Generating an Application with the Project Accelerator or Joule Using SAP Fiori Tools AI](generating-an-application-with-the-project-accelerator-or-joule-using-sap-fiori-tools-ai-6845fed.md).




<a name="loiof09752ebcf63473e9194ea29ca232e56__section_pnf_3nd_xmb"/>

## What Is SAP Fiori Elements?

SAP Fiori elements is a framework that empowers you to effectively develop scalable, efficient, and modern SAP Fiori applications that align with SAP's design principles and user-centric approach. App developers can use SAP Fiori elements to create SAP Fiori applications based on OData services and annotations that don't need JavaScript UI coding.

> ### Tip:  
> You can also develop a SAP Fiori elements for OData V2 application with SAP Fiori tools. However, we recommend that you use SAP Fiori elements for OData V4 instead to take advantage of building blocks and custom pages.
> 
> You can also develop a freestyle SAPUI5 application with SAP Fiori tools. However, we recommend that you use the Custom Page floorplan provided by SAP Fiori elements for OData V4 instead because freestyle SAPUI5 templates are deprecated.



### Developing Apps with SAP Fiori Elements for OData V4

Here are some of the most important features provided by SAP Fiori elements for OData V4:

**Building Blocks**

SAP Fiori elements for OData V4 provides building blocks: reusable artifacts that are the cornerstone for every SAP Fiori elements for OData V4 application. They contain standardized layout patterns or interaction behaviors to provide enterprise readiness, support UI consistency, and boost developer efficiency.

For more information and live examples, see the SAP Fiori development portal at [Building Blocks](https://ui5.sap.com/test-resources/sap/fe/core/fpmExplorer/index.html#/buildingBlocks/buildingBlocks).

**Standard Floorplans**

To enable efficient development, SAP Fiori elements for OData V4 provides standard floorplans which are predefined layouts of building blocks. These floorplans inherit all the qualities of their building blocks while adding optimizations for component interaction at the floorplan level.

SAP Fiori elements for OData V4 provides the following standard floorplans:

-   List Report Page

-   Worklist Page

-   Analytical List Page

-   Object Page

-   Overview Page


Use standard floorplans for the most efficient approach for building your SAP Fiori elements application. For specific deviations, you can leverage extension points.

For more information and live examples, see the SAP Fiori development portal at [Standard Floorplans](https://ui5.sap.com/test-resources/sap/fe/core/fpmExplorer/index.html#/topic/floorplans).

**Custom Page**

For more flexibility, you can use custom pages which serve as the basis for custom layouts that can utilize building blocks with all their framework qualities. These custom pages can contain a layout building block for optimal support while offering maximum flexibility.

Use custom pages for the most flexible approach for building your SAP Fiori elements for OData V4 application and for added flexibility, select custom pages with their building blocks and options for additional SAPUI5 coding.

For more information and live examples, see the SAP Fiori development portal at [Custom Page](https://ui5.sap.com/test-resources/sap/fe/core/fpmExplorer/index.html#/controllerExtensions/customPage).



### Developing Apps with SAP Fiori Elements for OData V2

Here is the most important feature provided by SAP Fiori elements for OData V2:

**Standard Floorplans**

SAP Fiori elements for OData V2 provides standard floorplans which are predefined layouts to enable efficient development. These floorplans add optimizations for component interaction at the floorplan level.

SAP Fiori elements for OData V2 provides the following standard floorplans:

-   List Report Page

-   Worklist Page

-   Analytical List Page

-   Object Page

-   Overview Page


Use standard floorplans for the most efficient approach for building your SAP Fiori elements application. For specific deviations, you can leverage extension points.

For more information, see [Using SAP Fiori Elements Floorplans](https://sapui5.hana.ondemand.com/#/topic/797c3239b2a9491fa137e4998fd76aa7).

For more information about SAP Fiori elements, see [Developing Apps with SAP Fiori Elements](https://sapui5.hana.ondemand.com/#/topic/03265b0408e2432c9571d6b3feb6b1fd).



<a name="loiof09752ebcf63473e9194ea29ca232e56__section_o1p_3kz_51c"/>

## Generating an Application with the Project Accelerator or Joule Using SAP Fiori Tools AI

You can use the Project Accelerator from SAP Fiori tools AI, or Joule, to generate data models, services, sample data, and an SAP Fiori UI for your project based on your business requirements.

You can use the Project Accelerator or Joule to kick-start your SAP Fiori development by directly translating your business requirements into a CAP project with a single SAP Fiori elements application. Your business requirements can consist of text, images, or text and images. The generated application can consist of just a list report page, a list report page with one or multiple object pages, or a form entry object page.

For more information, see [Generating an Application with the Project Accelerator or Joule Using SAP Fiori Tools AI](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/6845fedbb38c4da7a54a2c76081f3abb.html).

