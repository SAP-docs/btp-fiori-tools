<!-- loio4102b3d63d9047c881108e6f0caae15e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Form Section

Form sections are based on the annotation `UI.FieldGroup` and can be added, moved, changed, and deleted.



<a name="loio4102b3d63d9047c881108e6f0caae15e__section_d3x_4sx_xrb"/>

## Adding Form Section

To add a Form section, perform the following steps:

1.  Click the *Object/Form Entry Page* to open the *Page Editor*.
2.  Navigate to the section node in the outline and click the :heavy_plus_sign: \(*Add*\) icon.

    As a result, a dropdown menu displaying currently supported section types appears.

3.  Select *Add Form Section* from the dropdown list.

    A pop-up window *Add Form Section* appears with a field to provide a label for the section to be added.

4.  Enter a title to the *Label* field and click *Add*.

    > ### Note:  
    > See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if there is none.

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

You can change the order of sections in the application header. Drag and drop the required section to a different position within the *Header Sections* node:

-   When dropped, the records in the `UI.Facets` collection are reordered.
-   When the SAP Fiori application is rendered, sections are displayed based on the records sequence in the `UI.HeaderFacets` annotation.

**Move multiple sections**

To move multiple sections to another position, perform the following steps:

1.  Press [Ctrl\] + [Click\]  to select more than one section.
2.  Drag the selected section to the desired position with your pointer.



<a name="loio4102b3d63d9047c881108e6f0caae15e__section_cwh_qxx_xrb"/>

## Deleting Form Section

To delete a section, perform the following steps:

1.  Navigate to the section node in the outline.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* pop-up window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes the `UI.ReferenceFacet` record from `UI.Facets`.

> ### Note:  
> To remove the unreferenced `UI.FieldGroup` annotation, run the cleanup procedure to delete the unreferenced annotation.



<a name="loio4102b3d63d9047c881108e6f0caae15e__changeformsectionlabel"/>

## Maintaining Form Section Properties



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    The section is renamed both in the *Page Editor* and in the application preview.


For more information, see [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301).



### Display on Demand

The `Display On Demand` switch is displayed in the *Property Panel* for the [Form Section](form-section-4102b3d.md) and [Identification Section](identification-section-b83f501.md) section if they are used as a sub section in a [Group Section](group-section-1894c47.md). Activate it to hide the [Form Section](form-section-4102b3d.md) or [Identification Section](identification-section-b83f501.md) under the *Show More* by default. Click *Show More* to make it visible. Deactive it to always display the section.

> ### Note:  
> By default, this property is deactivated. Once the user activates it, an embedded annotation `UI.PartOfPreview` is added to the respective `UI.ReferenceFacet` record with boolean value `false`. The embedded annotation will be removed, if the property is switched off again. The embedded annotation is also removed, if the section is moved and not contained in a [Group Section](group-section-1894c47.md) after the move.



### Hidden

For more information, see [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0).

