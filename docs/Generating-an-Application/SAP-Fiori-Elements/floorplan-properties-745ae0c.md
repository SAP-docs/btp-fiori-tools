<!-- loio745ae0c87e994df5acf6bb20ee66b1e1 -->

# Floorplan Properties

After you select a data source for your application, you can customize the application by setting the following properties:



<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_bhf_ts3_nrb"/>

## Floorplan Properties

-   *Main entity*: Represents the entity set that is used to populate the main content area of the list page. For a parametrized entity set, use a result entity set name instead.

-   *Navigation entity*: Represents the association from the main entity to navigate to applications.

-   *Table type*: Represents the type of table to be generated. The *Table type* property is only supported for floorplans that support a list in a table such as the list report page, worklist page, and analytical list page. For more information, see [Table Types](https://experience.sap.com/fiori-design-web/table-types-sap-fiori-elements/).




<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_bx1_4q4_vcc"/>

## Floorplan OData V2 Properties

The following properties are only applicable to floorplans based on OData V2:



### Worklist Page

-   *Variant management*: By default, variant management is hidden. To enable variant management at the table level, set `variantManagementHidden` to `false` in the `manifest.json` file. To enable variant management at the page level, set `smartVariantManagement` to `true` and `variantManagementHidden` to `false` in the `manifest.json` file.



### Analytical List Page

-   *Table type*: Defines the supported table types.

-   *Allow multi select*: Enables a checkbox for selecting multiple items in a table. This setting is only effective using defined actions either through an annotation or manifest.

-   *Auto hide*: Determines the chart or table interaction. If it is set to `true`, the chart acts as a filter for a table. If it is set to `false`, the matching table rows are highlighted but the table is not filtered.

-   *Enable smart variant management*. Enables variant management at the page level.




<a name="loio745ae0c87e994df5acf6bb20ee66b1e1__section_esb_gt4_vcc"/>

## Floorplan OData V4 Properties

The following properties are only applicable to floorplans based on OData V4:



### Analytical List Page

-   *Selection mode*: Defines different row selection modes for the generated table.


