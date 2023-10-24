<!-- loioc3e3ecd4131a4a90bc20756efe1ab5cc -->

# List-Detail Template

The **SAP Fiori List-Detail Application** template implements a flexible column layout, one of the design patterns that is specified by the SAP Fiori design guidelines .

The flexible column layout is a layout control that displays multiple templates on a single page. This allows faster and more fluid navigation between multipletemplates than the usual page-by-page navigation. The flexible column layout offers different layouts with up to three columns. In the template, we use two colums \(list and detail\). For more information about flexible columns and list-detail apps, see the [SAP Fiori Design Guidelines](https://experience.sap.com/fiori-design-web/).

> ### Note:  
> You have two options: You can use this template to build an **app for the SAP Fiori launchpad ** or to build **standalone apps**.
> 
> -   If the app runs in SAP Fiori launchpad it also contains additional features like *Save as Tile* or *Share in SAP Jam* that depend on SAP Fiori launchpad at runtime. This app cannot be run standalone, meaning no `index.html` file is created but only files for testing the app in the SAP Fiori launchpad sandbox.
> -   Only standalone apps contain an `index.html` file that is used to start the app.

  
  
**Screenshot of the List-Detail App**

![](images/Master-Detail_App_ee6e01b.png "Screenshot of the List-Detail App")

The main control of this app is the `sap.f.flexibleColumnLayout` control. This control first displays only the *List* view with a list of objects. When the user selects an object in the list, the *Detail* view is displayed on the right side, showing the details for the selected item.

The *List* view shows the current number of items and a search field that can be used to search through the list items. The number of items are updated automatically and the search filters for a preconfigured field of the list. Functionality for sorting, filtering, and grouping the list is also included in the template as well.

The *Detail* page contains a dynamic page header displaying more details for the selected object, an `sap.m.Overflowtoolbar` that can be enriched with custom content, and a table of line items that are associated to the selected object in the data model.

The list and the line item table are set to `growing` mode so that initially only the first few items are displayed for performance reasons. Using the `scrollToLoad` feature, the user can display more items by scrolling down or pressing the trigger at the end of the list.

We use the semantic `MasterPage` and `DetailPage` controls for the content aggregations of the `sap.f.FlexibleColumnLayout` control. A `SemanticPage` is an enhanced `sap.f.DynamicPage` that contains controls with semantic-specific meaning and displays them according to the SAP Fiori design guidelines. For more details about semantic controls, see the [sample](https://sapui5.hana.ondemand.com/#/api/sap.f.semantic.SemanticPage/samples), `sap.f.semantic.SemanticPage`, in the Demo Kit.



<a name="loioc3e3ecd4131a4a90bc20756efe1ab5cc__section_els_xvw_k1b"/>

## Where Can I Find the List-Detail Template?

You can find the template in the following places:

-   **SAP Fiori List-Detail Application** template in SAP Fiori tools

-   `openui5-masterdetail-app` in the [SAP Repository on GitHub](https://github.com/SAP)

    For more information on how to clone or download the template from GitHub, refer to the template documentation on [GitHub](https://github.com/SAP/openui5-masterdetail-app/blob/master/README.md) .




<a name="loioc3e3ecd4131a4a90bc20756efe1ab5cc__section_EnhanceTemplate"/>

## How Do I Enhance the Template?

You can find more information about the possibilities of object pages at [SAP Fiori Design Guidelines - Object Page](https://experience.sap.com/fiori-design-web/object-page/).

