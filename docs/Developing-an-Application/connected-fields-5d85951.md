<!-- loio5d85951736f84ee19ffb2abedbc739f2 -->

# Connected Fields



<a name="loio5d85951736f84ee19ffb2abedbc739f2__section_pjn_c44_tyb"/>

## Adding Connected Fields

You can add two semantically connected fields under the same label to the [Form Section](form-section-4102b3d.md) or [Identification Section](identification-section-b83f501.md) in the content area of an *Object Page*. For that, perform the following steps:

1.  Expand the required section and navigate your pointer to the *Fields* node.

2.  Click the plus icon [\+\] and choose [Add Connected Fields\].

3.  In the [Add Connected Fields\] popup window, set the common label. Then choose two semantically related properties as *Field 1* and *Field 2*.

    > ### Note:  
    > If the field is already used as part of another connected fields node in the section, you can't choose it when adding a new one.

4.  You can optionally set the delimiter to be displayed between the field values.

5.  Click *Add* to add connected fields to the *Form section*.

> ### Note:  
> You can't add the property that is already used in another connected fields node of the section.



<a name="loio5d85951736f84ee19ffb2abedbc739f2__section_pt4_jx4_tyb"/>

## Moving Connected Fields

You can move the connected fields node within a section or to a different section in the content area and swap the sequence of the fields within the connected fields node. For that, use one of the following functionalities:

**Drag and drop**

-   Drag the connected fields node and place it in a different position within its section or in a different section within the content area once the field is highlighted in green. Use the [Ctrl\] + [Click\] combination to select the connected fields node along with other fields for moving.

-   Drag the field in the connected fields node and place it above or below the other field within the node once the field is highlighted in green.


**Arrow buttons**

-   Use the *Move up* and *Move down* buttons next to the connected fields label to move the connected fields either within its section or to the different section in the content area.

-   Use the *Move up* or *Move down* button next to the field within the connected fields node to swap the sequence of the connected fields within the node.


> ### Note:  
> You can't move connected fields to the [Header Section](header-a05d7fc.md#loio8a127fc36f5640abaab0056e632fe630).



<a name="loio5d85951736f84ee19ffb2abedbc739f2__section_qtf_th5_tyb"/>

## Deleting Connected Fields

You can delete the connected fields node along with its subnodes, whereas deleting the individual fields within it isn’t possible.

To delete the connected fields node, perform the following steps:

1.  Expand the required section and navigate your pointer to the connected fields node.

2.  Click the delete icon to open the *Delete Confirmation* popup window.

3.  Click *Delete* to confirm the action.


> ### Note:  
> During deletion of the field, `UI.DataField`record is removed from the `UI.FieldGroup` or `UI.Identification` annotation. The annotations applied to the entity properties aren’t deleted.

> ### Note:  
> To clean up the orphaned `UI.ConnectedFields` annotation, you need to explicitly run the cleanup procedure that deletes the unreferenced annotations.



<a name="loio5d85951736f84ee19ffb2abedbc739f2__section_xyx_vj5_tyb"/>

## Maintaining Connected Field Properties

You can update the connected fields label and delimiter as well as set the complete connected fields node as hidden.

**Label**

The label for connected fields is maintained the same as the label for the basic fields. For more information, see [Fields](https://help.sap.com/docs/SAP_FIORI_tools/bdf9573a206b492382cc747e731cf34b/457f2e9699b5437fb09d56311055a4a0.html?state=DRAFT&version=DEV&q=label#fields).

**Delimiter**

You can choose one or multiple text characters such as `:`, `/`, or `-` to be displayed between the connected fields. If the delimiter isn’t set, the fields will be separated by space.

> ### Note:  
> The delimiter value isn’t translatable.

**Hidden**

Similar to the basic fields, connected fields nodes can be set hidden either statically with the boolean value or dynamically based on the boolean property.

For more information, see [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0).

You can’t change the properties used as connected fields. If you need to do so, delete the complete connected fields node and add it again with different properties.

You can set all the basic field properties other than **Label** and **Hidden** on the individual fields level.

**Hide by Property**

Once you’ve activated the *Hidden* feature with the toggle button, the *Hide by Property* field is displayed right after it to let you set the condition for hiding.

For more information, see [Hide by Property](appendix-457f2e9.md#loio4e8bb3df433546f8a80f16e53b29e4c1).

For more information, see [Maintaining Basic Field Properties](https://help.sap.com/docs/SAP_FIORI_tools/bdf9573a206b492382cc747e731cf34b/2953503145dd428194c6dff252744ac1.html?state=DRAFT&version=DEV&q=label#maintaining-basic-field-properties).

