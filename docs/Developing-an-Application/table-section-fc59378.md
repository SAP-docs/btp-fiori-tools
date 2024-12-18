<!-- loiofc593789991c46348b31c1bc3b9d9182 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Table Section

A table section can be added either on the section node or inside the group on the subsection node.

-   [Add Table Section](table-section-fc59378.md#loiofc593789991c46348b31c1bc3b9d9182__section_g5r_hpb_zrb)
-   [Move Table Section](table-section-fc59378.md#loiofc593789991c46348b31c1bc3b9d9182__section_udp_pxx_xrb)
-   [Change Table Section Label](table-section-fc59378.md#loiofc593789991c46348b31c1bc3b9d9182__section_yn2_2qb_zrb)
-   [Delete Table Section](table-section-fc59378.md#loiofc593789991c46348b31c1bc3b9d9182__section_cwh_qxx_xrb)



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_g5r_hpb_zrb"/>

## Adding Table Section

To add a table section, perform the following steps:

1.  Click the *Object/Form Entry Page* to open the *Page Editor*.
2.  Navigate to the section node in the outline and click the :heavy_plus_sign: \(*Add*\) icon.

    As a result, a dropdown menu displaying the supported section types appears.

3.  Select *Add Table Section* from the dropdown list.

    A pop-up window *Add Table Section* appears.

4.  Enter a title in the *Label* text box.
5.  Then, enter *Value Source Entity* to define the table data source and click *Add*.

As a result, you can see the following changes applied:

-   A new `UI.LineItem` with empty collection and a new reference facet with an `annotationPath` pointing to the created `UI.LineItem` is added to the existing `UI.Facets`.
-   If not yet available, a new `UI.Facets` annotation is created under the entity associated with that *Object Page*.
-   If `UI.Facets` exists on an underlying layer, the annotation in the underlying layer will be overridden.
-   For CAP CDS, a using statement is added to the overridden file if not yet there.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_udp_pxx_xrb"/>

## Moving Table Section

The user can change the order of the sections created in the application. By using the drag-and-drop functionality, drag the required section to a different position within its application:

-   When dropped, the records in the `UI.Facets` collection are reordered.

-   When SAP Fiori application is rendered, sections are displayed based on the records sequence in the `UI.Facets` annotation.


**Move multiple sections**

Annotation Library supports mass moving of the sections. To move the multiple sections to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one section.
2.  Drag the selected section to a different position with your pointer/mouse.



<a name="loiofc593789991c46348b31c1bc3b9d9182__section_cwh_qxx_xrb"/>

## Deleting Table Section

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

    As a result, the section is renamed both in the *Page Editor* and in the application preview.


See [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) for more information.

> ### Note:  
> See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.



### Hidden

See, [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)

**Related Information**  


[Table Actions](table-actions-da1931b.md)

[Table Columns](table-columns-a80d603.md)

