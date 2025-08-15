<!-- loio9c1e7b438d2f48038d8870c55d75770a -->

# Adapting the UI

Learn how to adapt the UI of applications using the Adaptation Editor.



<a name="loio9c1e7b438d2f48038d8870c55d75770a__section_tkz_f34_xlb"/>

## Contents

1.  [Overview](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__Overview)

2.  [Procedure](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__Procedure)

3.  [UI Editing Options](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__EditingOptions)

4.  [Embedding Content](adapting-the-ui-9c1e7b4.md#loio9c1e7b438d2f48038d8870c55d75770a__EmbeddingContent)




<a name="loio9c1e7b438d2f48038d8870c55d75770a__Overview"/>

## Overview

SAPUI5 adaptation projects use the editing capabilities of the Adaptation Editor. The Adaptation Editor is a design-time editor that provides an intuitive user interface to modify SAPUI5 adaptation project applications. For example, you can add, remove, or move fields and groups. You can also view all properties of the controls in the application and change the configurable properties.

> ### Tip:  
> The Adaptation Editor will display your project using the SAPUI5 version that was set during its generation. Alternatively, you can preview your project using a different SAPUI5 version, but you need to configure this in the project's settings before the next launch of the Adaptation Editor. To do so, follow these steps:
> 
> 1.  Open the `ui5.yaml` file located in your project root folder.
> 
> 2.  Locate the `version` property under the `ui5` node and change its value to the desired SAPUI5 version you want to use in the Adaptation Editor.
> 
> Keep in mind that changing other settings in this file will result in undesirable changes in your project's behavior. It is strongly recommended not to make such changes.

The editor has an Outline pane, a Canvas \(application preview\), and a Properties pane.

If the application page is based on an SAP Fiori elements list report or an object page floorplan, a quick actions list is displayed above the Properties pane. This quick actions list provides an easy way for you to create the most commonly used adaptation changes. The available actions depend on the page's floorplan and the SAPUI5 version. For more information, see [Quick Actions Availability Matrix](quick-actions-availability-matrix-5d3d94b.md).

The buttons on the Adaptation Editor toolbar allow you to:

-   Navigate through and preview the application using the *Navigation* mode.

-   Change the application using the *Adaptation* mode. In this mode, if you click a UI element in the Canvas, the element is selected and highlighted in the Outline pane and the other way around. You can deselect the UI element by clicking it again in the Canvas. The Properties pane displays the properties of the UI element.

-   Change the device format of the canvas to smartphone, tablet, or desktop view.

    > ### Note:  
    > If you switch between device formats, your changes are saved to the workspace.




<a name="loio9c1e7b438d2f48038d8870c55d75770a__Procedure"/>

## Procedure

1.  In your workspace, еxpand the `webapp` folder, right click the `manifest.appdescr_variant` file and choose *Open Adaptation Editor*.

    The Adaptation Editor launches in a browser window and the application loads in the editor for you to make the changes when you switch to Adaptation mode or to navigate and preview the application when you switch to Navigation mode.

    > ### Remember:  
    > Visual Studio Code \(VS Code\) needs to be kept running in order for the editor to work.

2.  If you want to change to a different view, switch to Navigation mode, navigate to the new view, and then switch back to Adaptation Mode.



<a name="loio9c1e7b438d2f48038d8870c55d75770a__EditingOptions"/>

## UI Editing Options

As mentioned in the overview section, you can modify the configurable properties of the UI elements and edit the fields or groups. Here are some specific examples of such actions:


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

1.  Hover over or select a group or a field and click *Add Field* from the context menu.

    > ### Tip:  
    > The context menu is available both in the canvas and in the outline pane of the Adaptation Editor.\*

2.  Select the fields that you want to add to the UI.

    You can also search for field labels and tooltips, or sort the fields in alphabetical order.

3.  To apply your adaptations, click *OK*.



</td>
</tr>
<tr>
<td valign="top">

**Add a new group** 

</td>
<td valign="top">

1.  Hover over or select a group or select the form it’s contained in and click *Add Group* from the context menu.

    The default group title is *New Group* but you can rename it.

2.  To apply your adaptations, press [Enter\] or select another element.



</td>
</tr>
<tr>
<td valign="top">

**Add sections to an object page** 

</td>
<td valign="top">

1.  Hover over or select a section and click *Add Section* from the context menu.

    > ### Note:  
    > If every available section is already on the object page, you cannot use this function and it’s grayed out in the context menu.

2.  Select the sections from the list of available sections that you want to add to the UI.

    You can also search for sections or sort them in alphabetical order.

3.  To apply your adaptations, click *OK*.



</td>
</tr>
<tr>
<td valign="top">

**Rename fields and groups** 

</td>
<td valign="top">

1.  Double-click a field or group. You can also hover over or select it and click *Rename Field* or *Rename Group* from the context menu.
2.  Rename the field label or group title.
3.  To apply your adaptations, press [Enter\]. To quit, press [Esc\].



</td>
</tr>
<tr>
<td valign="top">

**Drag and drop fields and groups** 

</td>
<td valign="top">

1.  Drag a field, group, or section.
2.  Drop the field, group, or section on its new location.

    A space appears where you can drop it. You can drop a field above or below any of the highlighted fields or in any group marked with a dashed box. You can drop a group or section on any of the highlighted groups or sections.




</td>
</tr>
<tr>
<td valign="top">

**Cut and paste fields and groups** 

</td>
<td valign="top">

1.  Hover over or select a field or group and click *Cut* from the context menu. The cut field or group gets highlighted. Also, the groups where you can paste the cut field or the forms where you can paste the cut group get highlighted using dashed boxes. Move fields, groups, and object page sections.
2.  To paste a cut field, hover over or select a highlighted group or a field in a highlighted group and click *Paste*. To paste a cut group, hover over or select a group in the highlighted forms and click *Paste* from the context menu.

> ### Note:  
> To remove the highlighting and exit pasting, press [Esc\].



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
3.  Click *Combine* from the context menu of one of the selected fields where you want the combined fields to be displayed.



</td>
</tr>
<tr>
<td valign="top">

**Split combined fields** 

</td>
<td valign="top">

1.  Hover over or select the combined fields.
2.  Click *Split* from the context menu.



</td>
</tr>
<tr>
<td valign="top">

**Remove fields, groups, or object page sections** 

</td>
<td valign="top">

1.  Hover over or select the field, group, or section that you want to remove from the UI.
2.  Click *Remove Field*, *Remove Group*, or *Remove Section* from the context menu or press [DEL\].

    The fields and sections are only removed from the UI, not permanently deleted. They're still available in the list of available fields or sections, and you can add them again at any point. You cannot remove mandatory fields \(also those contained in groups\) by accident as the system will ask you to confirm.




</td>
</tr>
</table>

\*The context menu in the outline pane of the Adaptation Editor is available for projects based on the maintained SAPUI5 versions ≥1.84.



<a name="loio9c1e7b438d2f48038d8870c55d75770a__EmbeddingContent"/>

## Embedding Content

After you have made your changes, click *Save* from the toolbar above the canvas.

Embedding content is performed in the same way as the key user scenario. For more information, see [Embedding Content](https://help.sap.com/viewer/0f8b49c4dfc94bc0bda25a19aa93d5b2/latest/en-US/bfdf15154f16419fb60ce598b21fe515.html).

