<!-- loio745ae0c87e994df5acf6bb20ee66b1e1 -->

# Floorplan Properties

Once the data source is supplied, you can customize the application by selecting from the list of entities in the data source.



<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_bhf_ts3_nrb"/>

## Generic Options Across Multiple Floorplan Types

-   *Main Entity*: Represents the entity set that is used to populate the main content area of the list page. For a parametrized entity set, use a result entity set name instead.

-   *Navigation Entity*: Represents the association from the main entity to navigate to apps.

-   *Table Type*: For floorplans that support a list in a table \(List Report Page, Worklist Page, and Analytical List Page\), you can choose the type of table to be generated. For more information about the list of table type options you can use, see [Table Types](https://experience.sap.com/fiori-design-web/table-types-sap-fiori-elements/).




<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_jbn_5cd_wtb"/>

## Worklist Page V2-Sspecific Properties

-   The worklist does not contain a smart filter bar. The search field is available in the table toolbar.

-   *Variant management*: By default, variant management is hidden. You can customize the worklist to provide variant management at table level. To do so, set the the *variantManagementHidden* flag to false in the `manifest.json`. You can enable page-level variant management by setting *smartVariantManagement* to true and the *variantManagementHidden* flag to false in the `manifest.json`. Variants can also be shared. The **Execute on Select** action is not available.
-   *Smart table*: The multiselect function is enabled for all tables. If there are only line item actions, a no-selection table is enabled. The **Export to Microsoft Excel** feature is not available. The default table type is **responsive**. The table title contains the row count. A fixed layout and growing using the scrolling function is enabled.



<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_otl_ws3_nrb"/>

## Analytical List Page V2-Specific Properties

-   *Table type*: Defines different table types supported in the *Analytical List Page*.

-   *Allow multi select*: Enables a checkbox for selecting multiple items in a table to be displayed. This setting is effective only in the case of defined actions either through an annotation or manifest.

-   *Auto hide*: Determines the chart or table interaction. If it is set to true, the chart acts as a filter for a table. If it is set to false, the matching table rows are highlighted but the table is not filtered.

-   *Enable smart variant management*. Enables page-level variant.




<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_wpn_1t3_nrb"/>

## Analytical List Page V4 specific properties

-   *Selection mode*: Defines different row selection modes for the generated SmartTable.




<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_edn_mt3_nrb"/>

## Overview Page

For each floorplan type, except for the *Overview Page*, you can select a main entity from the drop-down list to be used in the generated application.

Select the entity to be used as the filter type from the drop-down list of entities, which is a mandatory field. After the main entity is selected, a list of navigation entities that are filtered depending on the main entity is displayed.

> ### Note:  
> The navigation entity is an optional field.

