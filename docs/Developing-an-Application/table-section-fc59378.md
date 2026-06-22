<!-- loiofc593789991c46348b31c1bc3b9d9182 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Table Section

A table section can be added either on the section node or inside the group on the subsection node.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_g5r_hpb_zrb"/>

## Adding a Table Section

To add a table section, perform the following steps:

1.  Open the *Page Editor*.
2.  Navigate to the section node in the outline and click the :heavy_plus_sign: \(*Add*\) icon.

    As a result, a dropdown menu displaying the supported section types appears.

3.  Select *Add Table Section* from the dropdown list.

    The *Add Table Section* pop-up window appears.

4.  Enter a title in the *Label* text box.
5.  Select *Use Existing Table* or *Create New Table*.
    1.  *Use Existing Table*: Select a *Value Source* and then choose a `UI.LineItem` annotation, a `UI.PresentationVariant` annotation which references a `UI.LineItem` annotation or a `UI.SelectionPresentationVariant` annotation which references a `UI.LineItem` annotation.

        > ### Note:  
        > The `UI.SelectionPresentationVariant` annotation is available in applications with a minimum SAPUI5 version of 1.121 and higher.

    2.  *Create New Table*: Select a *Value Source*.


6.  *Table Type*: Select the appropriate table type from the available options.

    > ### Note:  
    > The list of available option depends on the service. `AnalyticalTable` and `TreeTable` are only available if the service metadata contains the respective annotations.

7.  Click *Add*.

The following changes are applied:

-   *Create New Table*: A new `UI.LineItem` annotation with an empty collection is created.
-   *Use Existing Table*: A new reference facet with an `annotationPath`, which points to the chosen `UI.LineItem` annotation, is added to the existing `UI.Facets` annotation.
-   If not yet available, a new `UI.Facets` annotation is created under the entity associated with that *Object Page*.
-   If `UI.Facets` exists on an underlying layer, the annotation in the underlying layer will be overridden.
-   For CAP CDS, a `using` statement is added to the overridden file if not yet there.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_udp_pxx_xrb"/>

## Moving a Table Section

The user can change the order of the sections created in the application. By using the drag-and-drop functionality, drag the required section to a different position within its application:

-   When dropped, the records in the `UI.Facets` collection are reordered.

-   When SAP Fiori application is rendered, sections are displayed based on the records sequence in the `UI.Facets` annotation.


**Move multiple sections**

Annotation Library supports mass moving of the sections. To move the multiple sections to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one section.
2.  Drag the selected section to a different position with your pointer/mouse.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_cwh_qxx_xrb"/>

## Deleting a Table Section

To delete the section in the application, perform the following steps:

1.  Navigate to the section layer.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes the referenced facet record from `UI.Facets` of the section in the Appendix.

> ### Note:  
> To clean up the orphaned `UI.LineItem` annotation, you need to explicitly run the cleanup procedure that deletes the unreferenced annotation.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_yn2_2qb_zrb"/>

## Maintaining Table Section Properties



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    The section is renamed both in the *Page Editor* and in the application preview.


For more information, see [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301).



### Hidden

For more information. see [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0).

**Related Information**  


[Table Actions](table-actions-da1931b.md)

[Table Columns](table-columns-a80d603.md)

