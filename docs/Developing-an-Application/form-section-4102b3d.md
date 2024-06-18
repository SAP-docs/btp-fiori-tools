<!-- loio4102b3d63d9047c881108e6f0caae15e -->

# Form Section

Form sections are based on the annotation `UI.FieldGroup` and can be added, moved, changed, and deleted.



<a name="loio4102b3d63d9047c881108e6f0caae15e__section_d3x_4sx_xrb"/>

## Adding Form Section

To add a Form section, perform the following steps:

1.  Click the *Object/Form Entry Page* to open the *Page Editor*.
2.  Navigate to the section node in the outline and click the *Add* icon [\+\].

    As a result, a dropdown menu displaying currently supported section types appears.

3.  Select *Add Form Section* from the dropdown list.

    A pop-up window *Add Form Section* appears with a field to provide a label for the section to be added.

4.  Enter a title to the *Label* field and click *Add*.

    > ### Note:  
    > See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.

    A new section tab appears in the application preview of the form and *Object Page*. Now you can add fields to the newly created form section. For more information, see [Adding Filter Fields](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__addingfilterfields).


In the `annotation` file, you can see the following changes applied:

-   A new `UI.FieldGroup` with the empty `Data` property is added.
-   A `UI.ReferenceFacet` record is added to the `UI.Facet` annotation with the following properties:
    -   `Target`, as annotation path pointing to the created `UI.FieldGroup`.
    -   `Label`, as a string value containing user-entered text.
    -   `ID`, as a string value auto-generated based on the label.

-   If the `UI.Facet` annotation isn’t yet available, it’s applied to the entity associated with the *Object Page*.
-   If the `UI.Facet` annotation exists on the underlying layer, the annotation on this layer will be overridden in the local file.
-   In the case of CAP CDS, a using statement is added to the overridden file.



<a name="loio4102b3d63d9047c881108e6f0caae15e__section_udp_pxx_xrb"/>

## Moving Form Section

The user can change the order of the sections in the application header. By using the drag-and-drop functionality, drag the required section to a different position within the *Header Sections* node:

-   When dropped, the records in the `UI.Facets` collection are reordered.
-   When SAP Fiori application is rendered, sections are displayed based on the records sequence in the `UI.HeaderFacets` annotation.

**Move multiple sections**

To move the multiple sections to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one section.
2.  Drag the selected section to the desired position with your pointer.



<a name="loio4102b3d63d9047c881108e6f0caae15e__section_cwh_qxx_xrb"/>

## Deleting Form Section

To delete the section in the application, perform the following steps:

1.  Navigate to the section node in the outline.
2.  Click the delete icon ![](../Project-Functions/images/Delete_icon_VS_Code_86e90a9.png) to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes respective `UI.ReferenceFacet` record from `UI.Facets`.

> ### Note:  
> To remove unreferenced `UI.FieldGroup` annotation, run the cleanup procedure that deletes the unreferenced annotation.



<a name="loio4102b3d63d9047c881108e6f0caae15e__changeformsectionlabel"/>

## Maintaining Form Section Properties



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    As a result, the section is renamed both in the *Page Editor* and in the application preview.


See [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) for more information.

> ### Note:  
> See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.



### Display on Demand

`Display On Demand` switch is displayed in the *Property Panel* for the [Form Section](form-section-4102b3d.md) and [Identification Section](identification-section-b83f501.md) section if they are used as a sub section in a [Group Section](group-section-1894c47.md). Switch it on to hide the [Form Section](form-section-4102b3d.md) or [Identification Section](identification-section-b83f501.md) under the [Show More\] button by default. Press the [Show More\] button to make it visible. Switch it off to always display the section.

> ### Note:  
> By default this property is switched off. Once the user switches it on, an embedded annotation `UI.PartOfPreview` is added to the respective `UI.ReferenceFacet` record with boolean value `false`. The embedded annotation will be removed, if the property is switched off again. The embedded annotation is also removed, if the section is moved and not contained in a [Group Section](group-section-1894c47.md) after the move.



### Hidden

See, [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0) in the Appendix.

