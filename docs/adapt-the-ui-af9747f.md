<!-- loioaf9747fdd5e04ac38faefe535c4c6789 -->

# Adapt the UI

Make changes to the UI elements of the adaptation project.



<a name="loioaf9747fdd5e04ac38faefe535c4c6789__section_tkz_f34_xlb"/>

## Contents

1.  [Overview](adapt-the-ui-af9747f.md#loioaf9747fdd5e04ac38faefe535c4c6789__Overview)

2.  [Procedure](adapt-the-ui-af9747f.md#loioaf9747fdd5e04ac38faefe535c4c6789__Procedure)

3.  [UI Editing Options](adapt-the-ui-af9747f.md#loioaf9747fdd5e04ac38faefe535c4c6789__EditingOptions)

4.  [Embedding Content](adapt-the-ui-af9747f.md#loioaf9747fdd5e04ac38faefe535c4c6789__EmbeddingContent)

5.  [Preview in a Separate Browser Tab](adapt-the-ui-af9747f.md#loioaf9747fdd5e04ac38faefe535c4c6789__PreviewSepertaeTab)




<a name="loioaf9747fdd5e04ac38faefe535c4c6789__Overview"/>

## Overview

SAPUI5 adaptation project uses the editing capabilities of the SAPUI5 Visual Editor tool. The SAPUI5 Visual Editor is a design-time editor that provides an intuitive user interface to modify SAPUI5 adaptation project applications. For example, you can add, remove, or move fields and groups. You can also view all properties of the controls in the application and change the configurable properties.

If you have created your project with Safe Mode switched on, you will not be able to do some of the actions described in this section. More specifically you will not be able to change properties, add fragments, or add controller extensions. If you think you want to turn Safe Mode off, so you can use these features, you can do this by selecting the switch named *Safe Mode* in the Visual Editor. Be aware that if you switch it off once, it is not possible to switch it on again.

> ### Tip:  
> The SAPUI5 Visual Editor will show you your project using the SAPUI5 version that you have set during its generation. If you want, you can preview your project using another SAPUI5 version, but you need to set it in the project\`s settings prior the next launch of the SAPUI5 Visual Editor. It can be easily done following these steps:
> 
> 1.  Open the `ui5.yaml` file placed in the root of your project.
> 
> 2.  Find the `framework/version` parameter and change their value to point to the desired SAPUI5 version.
> 3.  Find the `ui5/version` property, and change its value to the same desired SAPUI5 version.
> 4.  Find the `ui5/url` property and change its value to point to the URL for the same desired SAPUI5 version.
> 
> Have in mind that changing other settings in this file will result in undesirable changes in the behavior of your project, and it is strongly advised not to make such changes.

The editor has an Outline pane, a Canvas \(application preview\), and a Properties pane.

The buttons on the SAPUI5 Visual Editor toolbar allow you to:

-   Navigate through and preview the application using the *Preview* mode.

-   Change the application using the *Edit* mode. In this mode, if you click a UI element in the Canvas, the element is selected and highlighted in the Outline pane and vice versa. You can deselect the UI element by clicking it again in the Canvas. The Properties pane displays the properties of the UI element.

-   Change the device format of the canvas to smartphone, tablet, or desktop view.

    > ### Note:  
    > If you switch between device formats, your changes are saved to the workspace.

-   Expand and collapse the panes to the right and left of the canvas.




<a name="loioaf9747fdd5e04ac38faefe535c4c6789__Procedure"/>

## Procedure

1.  In your workspace, еxpand the `webapp` folder and right click the `manifest.appdescr_variant` file and choose *Open SAPUI5 Visual Editor*. SAPUI5 Visual Editor launches and the application loads in the editor for you to make the changes when you switch to Edit mode from Preview mode.
2.  Navigate to the page containing the UI element you want to change.
3.  From the editor header, select *Edit*.



<a name="loioaf9747fdd5e04ac38faefe535c4c6789__EditingOptions"/>

## UI Editing Options


<table>
<tr>
<td valign="top">

**Change properties** 

</td>
<td valign="top">

1.  Select the UI element you want to change.
2.  Change the element's properties as needed.

> ### Note:  
> Not all properties can be changed.



</td>
</tr>
<tr>
<td valign="top">

**Add new fields** 

</td>
<td valign="top">

1.  Hover over or select a group or a field and choose *Add Field* from the context menu.
2.  Select the fields from the list of available fields that you want to add to the UI.

    You can also search for field labels and tooltips, or sort the fields in alphabetical order.

3.  To apply your adaptations, choose *OK*.



</td>
</tr>
<tr>
<td valign="top">

**Add a new group** 

</td>
<td valign="top">

1.  Hover over or select a group or select the form it’s contained in and choose *Add Group* from the context menu.

    The default group title is *New Group*, and you can rename it to whatever you want.

2.  To apply your adaptations, press [ENTER\] or select another element.



</td>
</tr>
<tr>
<td valign="top">

**Add sections to an object page** 

</td>
<td valign="top">

1.  Hover over or select a section and choose *Add Section* from the context menu.

    > ### Note:  
    > If all available sections are already on the object page, you cannot use this function and it’s grayed out in the context menu.

2.  Select the sections from the list of available sections that you want to add to the UI.

    You can also search for sections or sort them in alphabetical order.

3.  To apply your adaptations, choose *OK*.



</td>
</tr>
<tr>
<td valign="top">

**Rename fields and groups** 

</td>
<td valign="top">

1.  Double-click a field or group. You can also hover over or select it and choose *Rename Field* or *Rename Group* from the context menu.
2.  Rename the field label or group title.
3.  To apply your adaptations, press [ENTER\]; to quit, press [ESC\].



</td>
</tr>
<tr>
<td valign="top">

**Drag and drop fields and groups** 

</td>
<td valign="top">

1.  Drag a field, group, or section.
2.  Drop the field, group, or section on its new location.

    A space appears where you can drop it. You can drop a field above or below any of the highlighted fields or in any group marked with a dashed box; you can drop a group or section on any of the highlighted groups or sections.




</td>
</tr>
<tr>
<td valign="top">

**Cut and paste fields and groups** 

</td>
<td valign="top">

1.  Hover over or select a field or group and choose *Cut* from the context menu. The cut field or group gets highlighted. Also, the groups where you can paste the cut field or the forms where you can paste the cut group get highlighted using dashed boxes. Move fields, groups, and object page sections.
2.  To paste a cut field, hover over or select a highlighted group or a field in a highlighted group and choose *Paste*. To paste a cut group, hover over or select a group in the highlighted forms and choose *Paste* from the context menu.

> ### Note:  
> To remove the highlighting and exit pasting, press [ESC\].



</td>
</tr>
<tr>
<td valign="top">

**Combine fields** 

</td>
<td valign="top">

You can combine up to three fields so that they’re displayed in a single line.

1.  Select a field.
2.  Press and hold [CTRL\]. Move fields, groups, and object page while selecting the other fields you want to combine with this field.
3.  Choose *Combine* from the context menu of one of the selected fields where you want the combined fields to be displayed.



</td>
</tr>
<tr>
<td valign="top">

**Split combined fields** 

</td>
<td valign="top">

1.  Hover over or select the combined fields.
2.  Choose *Split* from the context menu.



</td>
</tr>
<tr>
<td valign="top">

**Remove fields, groups, or object page sections** 

</td>
<td valign="top">

1.  Hover over or select the field, group, or section that you want to remove from the UI.
2.  Choose *Remove Field*, *Remove Group*, or *Remove Section* from the context menu or press [DEL\].

    The fields and sections are only removed from the UI, not permanently deleted. They're still available in the list of available fields or sections, and you can add them again at any point. You cannot remove mandatory fields \(also those contained in groups\) by accident as the system will ask you to confirm.




</td>
</tr>
</table>



<a name="loioaf9747fdd5e04ac38faefe535c4c6789__EmbeddingContent"/>

## Embedding Content

Embedding content is done the same way, as in the key user scenario. You can follow the procedure described in [Embedding Content](https://help.sap.com/viewer/0f8b49c4dfc94bc0bda25a19aa93d5b2/latest/en-US/bfdf15154f16419fb60ce598b21fe515.html).



<a name="loioaf9747fdd5e04ac38faefe535c4c6789__PreviewSepertaeTab"/>

## Preview in a Separate Browser Tab

See [Preview the Adaptation Project](preview-the-adaptation-project-64cc15b.md).

