<!-- loio2953503145dd428194c6dff252744ac1 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Basic Fields



<a name="loio2953503145dd428194c6dff252744ac1__section_al5_jjr_35b"/>

## Adding Basic Fields

To add a new field to an existing section, perform the following steps:

1.  Expand the required section and navigate your pointer to the field layer.
2.  Click the plus icon [\+\] to open the *Add Fields* pop-up window.
3.  In the *Add Fields* pop-up window, search for or select one or several fields from the drop-down menu.
4.  Click *Add* to add new fields to the Form section.

> ### Note:  
> The following entity properties are excluded from the fields dialog creation process:
> 
> -   Properties of the type `Edm.Guid`.
> 
> -   Draft-specific properties, such as `IsActiveEntity`, `HasActiveEntity`, and `HasDraftEntity`.
> 
> -   Draft-specific navigation properties such as `SiblingEntity`, `DraftAdministrativeData`.
> 
> -   The properties already referenced in this or other sections.

> ### Note:  
> You can't add the field twice to the same section.



<a name="loio2953503145dd428194c6dff252744ac1__movebasicfields"/>

## Moving Basic Fields

To move a field within a section or to a different section in the application, use one of the following functionalities:

-   **Drag-and-drop**

    By using the drag-and-drop functionality, drag the required field and place it in a different position within its section or in a different section once the field is highlighted in green.

-   **Arrow buttons**

    By using the *Move up* and *Move down* buttons next to the field name, you can move the field either within its section or to the different section.




### Move Fields to Another Section

To move a field to another section, drag and drop to a desired section.

> ### Note:  
> Fields can be moved to a different section if the `FieldGroup` or `Identification` annotation are applied to the **same entity** as the originating section.



### Move Multiple Fields

To move the multiple fields to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one field.
2.  Drag the selected fields to a different position with your pointer/mouse.

> ### Note:  
> You can't move the field to the section if the same field is already part of it.



<a name="loio2953503145dd428194c6dff252744ac1__section_ud3_lvz_35b"/>

## Deleting Basic Fields

To delete the fields, perform the following steps:

1.  Expand the required section and navigate your pointer to the field layer.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

    > ### Note:  
    > During deletion of the field, `UI.DataField` record is removed from the `UI.FieldGroup` annotation. The annotations applied to the entity properties aren't deleted.




<a name="loio2953503145dd428194c6dff252744ac1__section_mtm_x32_s5b"/>

## Maintaining Basic Field Properties

Field properties are associated with fields in the Field section and the application with the help of annotations. The following field properties can be edited:

-   [Label](basic-fields-2953503.md#loio2953503145dd428194c6dff252744ac1__label)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Hide by Property](appendix-457f2e9.md#loio4e8bb3df433546f8a80f16e53b29e4c1)
-   [Restrictions](basic-fields-2953503.md#loio2953503145dd428194c6dff252744ac1__restrictions)
-   [Text](appendix-457f2e9.md#loio5d1cc16e80ce48de8a47f2835a42cc47)
-   [Text Arrangement](appendix-457f2e9.md#loioecd5568919bf43c5a04dd6b5e8e173f6) 
-   Display Type
-   [Criticality](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed)
-   [Semantic Object Name](appendix-457f2e9.md#loio90e03983431d4bfd927b51593a937955)
-   [Semantic Object Property Mapping](appendix-457f2e9.md#loio7726cb0d97194461973e3ec176c8a888)

See [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0) for more information.



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    As a result, the section is renamed both in the *Page Editor* and in the application preview.


See [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) for more information.

> ### Note:  
> See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.



### Restrictions

Define whether the field input in create/edit mode is mandatory, optional, or read-only. Use field *Restrictions* to control the state of a property.

The following options are displayed in the restriction value drop-down menu:


<table>
<tr>
<th valign="top">

Option

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*None*

</td>
<td valign="top">

No annotations are applied. Therefore, this field by default is considered optional.

</td>
</tr>
<tr>
<td valign="top">

*Optional*

</td>
<td valign="top">

This field can be left empty, no obligatory data input is required.

</td>
</tr>
<tr>
<td valign="top">

*Mandatory* 

</td>
<td valign="top">

This field value must be provided, can't be empty.

</td>
</tr>
<tr>
<td valign="top">

*ReadOnly*

</td>
<td valign="top">

This field is displayed as read-only data with no editing allowed.

</td>
</tr>
</table>

> ### Note:  
> When the Object Page entity isn't draft enabled \(read-only\), Display Type and Restrictions fields aren't available in the property panel as the fields aren't editable and are only used for displaying the value.

> ### Note:  
> If restriction value is defined in the lower layer \(e.g. in the service\), the respective option is displayed with the suffix \(base layer\) and option *None* isn't available. If the back-end restriction value can't be resolved because unsupported annotation complexity, then the base layer value is displayed as a *Complex*\(base layer\).

