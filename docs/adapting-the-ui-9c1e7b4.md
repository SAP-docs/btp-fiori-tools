<!-- loio9c1e7b438d2f48038d8870c55d75770a -->

# Adapting the UI



<a name="loio9c1e7b438d2f48038d8870c55d75770a__section_tkz_f34_xlb"/>

## Contents

1.  [Overview](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__Overview)

2.  [Procedure](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__Procedure)

3.  [UI Editing Options](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__EditingOptions)

4.  [Embedding Content](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__EmbeddingContent)




<a name="loio9c1e7b438d2f48038d8870c55d75770a__Overview"/>

## Overview

SAPUI5 adaptation project uses the editing capabilities of the Adaptation Editor \(Visual Editor\) tool. The Adaptation Editor \(Visual Editor\) is a design-time editor that provides an intuitive user interface to modify SAPUI5 adaptation project applications. For example, you can add, remove, or move fields and groups. You can also view all properties of the controls in the application and change the configurable properties.

> ### Tip:  
> The Adaptation Editor \(Visual Editor\) will show you your project using the SAPUI5 version that you have set during its generation. If you want, you can preview your project using another SAPUI5 version, but you need to set it in the project\`s settings prior the next launch of the Adaptation Editor \(Visual Editor\). It can be easily done following these steps:
> 
> 1.  Open the `ui5.yaml` file placed in the root folder of your project.
> 
> 2.  Find the `version` property under the `ui5` node, and change its value to the desired SAPUI5 version you want to use for preview in the Adaptation Editor \(Visual Editor\)
> 
> Have in mind that changing other settings in this file will result in undesirable changes in the behavior of your project, and it is strongly advised not to make such changes.

The editor has an Outline pane, a Canvas \(application preview\), and a Properties pane.

The buttons on the Adaptation Editor \(Visual Editor\) toolbar allow you to:

-   Navigate through and preview the application using the *Navigation* mode.

-   Change the application using the *UI Adaptation Mode* mode. In this mode, if you click a UI element in the Canvas, the element is selected and highlighted in the Outline pane and vice versa. You can deselect the UI element by clicking it again in the Canvas. The Properties pane displays the properties of the UI element.

-   Change the device format of the canvas to smartphone, tablet, or desktop view.

    > ### Note:  
    > If you switch between device formats, your changes are saved to the workspace.




<a name="loio9c1e7b438d2f48038d8870c55d75770a__Procedure"/>

## Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file an choose *Preview Application*. Choose *start-editor*. Adaptation Editor \(Visual Editor\) launches in a browser window and the application loads in the editor for you to make the changes when you switch to UI Navigation mode or to navigate and preview the application when you switch to Navigation mode.

    > ### Note:  
    > Have in mind that the VSCode instance needs to be kept running in order for the editor to be operable.

2.  If you want to change different view than the one that is currently loaded, switch to Navigation mode so you can navigate to it, and then switch back to UI Adaptation Mode.



<a name="loio9c1e7b438d2f48038d8870c55d75770a__EditingOptions"/>

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



<a name="loio9c1e7b438d2f48038d8870c55d75770a__EmbeddingContent"/>

## Embedding Content

After you do your changes, choose *Save* from the toolbar above the canvas.

Embedding content is done the same way, as in the key user scenario. You can follow the procedure described in [https://help.sap.com/viewer/0f8b49c4dfc94bc0bda25a19aa93d5b2/latest/en-US/bfdf15154f16419fb60ce598b21fe515.html](https://help.sap.com/viewer/0f8b49c4dfc94bc0bda25a19aa93d5b2/latest/en-US/bfdf15154f16419fb60ce598b21fe515.html).

