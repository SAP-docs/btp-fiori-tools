<!-- loiob83f501a5b284e768a8e2ed53ea98428 -->

# Identification Section



<a name="loiob83f501a5b284e768a8e2ed53ea98428__section_d3x_4sx_xrb"/>

## Adding Identification Section

An Identification Section can be added if `UI.Identification` annotation isn’t yet defined for the page entity or not referenced in `UI.Facets` annotation.

> ### Note:  
> More than one identification section can't be added for a page. Identification sections cannot be added as subsections. Actions cannot be added to the identification section. Header or Footer actions can be added instead.

To add an Identification section, perform the following steps:

1.  Click the *Object/Form Entry Page* to open the *Page Editor*.
2.  Navigate to the section node in the outline and click the *Add* icon [\+\].

    As a result, a drop-down menu displaying currently supported section type appears.

3.  Select *Add Identification Section* from the drop-down list.

    A pop-up window *Add Identification Section* appears with a field to provide a label for the section to be added.

4.  Enter a title to the *Label* field and click *Add*.

    A new section tab appears in the application preview of the form and object page.

    > ### Note:  
    > As a result a `UI.Identification` annotation with no qualifier is generated and referenced in the `UI.Facets` annotation. If `UI.Identification` already exists, a new one isn’t generated, but the existing one is referenced in `UI.Facets`.


You can prepare the section label for translation.

-   For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md).




<a name="loiob83f501a5b284e768a8e2ed53ea98428__section_udp_pxx_xrb"/>

## Moving Identification Section

The user can change the order of the sections created in the application. By using the drag-and-drop functionality, drag the required section to a different position within its application:

-   When dropped, the records in the `UI.Facets` collection are reordered.

-   When SAP Fiori application is rendered, sections are displayed based on the records sequence in the `UI.Facets` annotation.


**Move multiple sections**

To move the multiple sections to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one section.
2.  Drag the selected section to a different position with your pointer/mouse.



<a name="loiob83f501a5b284e768a8e2ed53ea98428__section_yjl_s5b_zrb"/>

## Deleting Identification Section

To delete the section in the application, perform the following steps:

1.  Navigate to the section node in the outline.
2.  Click the *Delete* icon.

    The *Delete Confirmation* pop-up window appears.

3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes respective `UI.ReferenceFacet` record from `UI.Facets`.



<a name="loiob83f501a5b284e768a8e2ed53ea98428__section_dpk_pp2_s5b"/>

## Maintaining Identification Section Properties



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    As a result, the section is renamed both in the *Page Editor* and in the application preview.


See [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) for more information.

> ### Note:  
> See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.



### Display on Demand

See [Display on Demand](form-section-4102b3d.md#loio4102b3d63d9047c881108e6f0caae15e__displayondemand).



### Hidden

See, [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0) in the Appendix.

