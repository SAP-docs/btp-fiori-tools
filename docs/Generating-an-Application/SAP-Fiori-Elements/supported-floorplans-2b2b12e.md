<!-- loio2b2b12e708944d85a40d087194cc1edd -->

# Supported Floorplans

The SAP Fiori generator provides the following SAP Fiori elements floorplans to choose from to create your SAP Fiori elements application:

-   *List Report Page*

    With the list report page, users can view and work with a large set of items. This floorplan offers powerful features for finding and acting on relevant items. It’s often used as an entry point for navigating to the item details, which are shown on the object page.

    For more information, see [List Report](https://experience.sap.com/fiori-design-web/list-report-floorplan-sap-fiori-element/) and [Object Page](https://experience.sap.com/fiori-design-web/object-page/).


-   *Worklist Page*

    The worklist page displays a collection of items that the user needs to process. Working through the list usually involves reviewing details of the items and taking action. In most cases, the user has to either complete a work item or delegate it.

    The focus of the worklist floorplan is on processing items. This differs from the list report floorplan, which focuses on finding and acting on relevant items from a large dataset.

    You can use any*List Report* and *Object Page* to configure the *Worklist Page*.

    For more information, see [Worklist Floorplan](https://experience.sap.com/fiori-design-web/work-list/).

    > ### Note:  
    > For worklist floorplans using an OData V4 data source, only `SAPUI5` versions 1.99 and above are supported.

    For information on what the worklist page supports for OData V2, see [Floorplan Properties](floorplan-properties-745ae0c.md).


-   *Analytical List Page*

    The analytical list page offers a unique way to analyze data step by step from different perspectives to investigate the root cause of any deviations, spikes, and abnormalities through drilldown, and to act on transactional content. All this can be done seamlessly within a single page. The purpose of the analytical list page is to identify problem areas within datasets or significant single instances using data visualization and business intelligence.

    Visualization helps users to recognize facts and situations, and to reduce the number of interaction steps needed to gain insights or to identify significant single instances. Chart visualization enables users to spot relevant data more quickly.

    The main target group are users who work on transactional content. They benefit from fully transparent business object data and direct access to business actions. In addition, they have access to analytical views and functions without having to switch between systems. These include KPIs, a visual filter where filter values are enriched by measures and visualizations, and a combined table or chart view with drill-in capabilities \(hybrid view\). Users can interact with the chart to look deep into the data. The visualization enables them to identify spikes, deviations, and abnormalities more quickly, and to take appropriate action right away.

    For more information, see [Analytical List Page](https://experience.sap.com/fiori-design-web/analytical-list-page/).

    > ### Note:  
    > For analytical list page floorplans using an OData V4 data source, only `SAPUI5` versions 1.90 and above are supported.


-   *Overview Page*

    The overview page is a data-driven SAP Fiori floorplan that provides all the information the user needs on a single page, based on the user specific domain or role. It allows the user to focus on the most important tasks, and view, filter, and react to the information quickly.

    Each task or topic is represented by a card or a content container. The overview page acts as a UI framework for organizing multiple cards on a single page.

    The overview page uses annotated views of app data, meaning that the app content can be tailored to the domain or role. Different types of cards allow you to visualize information in an attractive and efficient way.

    For more information, see [Overview Page](https://experience.sap.com/fiori-design-web/overview-page/).

-   *Form Entry Object Page*

    The form entry object page allows users to create an application with an object page and a generated form. The object page floorplan enables end-users to provide data entry in the generated application.

    For more information, see [Object Page](https://experience.sap.com/fiori-design-web/object-page/).

-   *Custom Page*

    The custom page floorplan makes it easy for you to extend apps based on SAP Fiori elements for OData V4. You can use any `SAPUI5` coding or controls in extension points, and take advantage of the provided building blocks.

    For more information and live examples, see the SAP Fiori development portal at [Custom Page](https://ui5.sap.com/test-resources/sap/fe/core/fpmExplorer/index.html#/controllerExtensions/customPage).


