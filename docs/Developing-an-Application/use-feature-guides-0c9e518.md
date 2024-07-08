<!-- loio0c9e518ecf704b2f80a2bed0eaca60ae -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Use Feature Guides

With guided development, you can access **how-to** guides and tutorials that explain how to implement certain functionality in an SAP Fiori elements application. You can read through the steps required to implement a feature and then use the guided development approach to make the required changes in your project.



<a name="loio0c9e518ecf704b2f80a2bed0eaca60ae__section_g4l_234_slb"/>

## Launching Guided Development

You can launch guided development in the following ways:



### Using the Command Palette

-   Open *Command Palette* \([CMD\]/[CTRL\] + [Shift\] + [P\]\).
-   Start typing *guided development*.
-   Select *Fiori: Open Guided Development* or *Fiori: Open Guided Development to the Side*.
-   Select SAP Fiori elements project from your workspace.

The *Fiori: Open Guided Development* option opens guided development in a new tab and in the selected editor region in case the editor is split into multiple regions. The *Fiori: Open Guided Development to the Side* option opens guided development to the side of the current file in another column.



### Using the Folder Context Menu

If you already have an SAP Fiori elements project in your current workspace, you can right-click its folder and select *SAP Fiori tools - Open Guided Development*. Then, guided development opens to the side of the current file in another column.

> ### Note:  
> If you don’t have any SAP Fiori elements project in your workspace, you can still open guided development by using the *Command Palette*. It’s possible to check the available guides descriptions and code samples, while interactive features are disabled in this case.



### Working with Projects

Guided development can only work with one project at a time. The name of this project is displayed on the tab header next to guided development, and this project provides all project-specific data used in the guides.

The project-specific data contains the following components:

-   The list of entities in the *Entity* list.

-   The list of data sources in the *Model* list.

-   The list of pages in the *Page* list.

-   The annotation terms that are defined in the service across all the guides.

    > ### Note:  
    > In guided development, you can add annotations from services other than the mainService.


To select or change a project, proceed as follows:

1.  Click *Select Project* on the left side of the toolbar.
2.  Select a project from the *Project* list.

    ![Select Project](images/SelectProject_9ea63e4.png)


We recommend that you refresh **guided development** in the cases given in the following table:


<table>
<tr>
<th valign="top">

When

</th>
<th valign="top">

How

</th>
</tr>
<tr>
<td valign="top">

When a new project is added to the workspace.

</td>
<td valign="top">

Click the <span class="SAP-icons-V5"></span> \(*Refresh*\) icon inside the Project list.

</td>
</tr>
<tr>
<td valign="top">

When something in the current project is changed outside guided development, such as a new page is added, or an underlying service is updated.

</td>
<td valign="top">

Click the <span class="SAP-icons-V5"></span> \(*Refresh*\) icon on the toolbar next to the Project list.

</td>
</tr>
</table>



<a name="loio0c9e518ecf704b2f80a2bed0eaca60ae__section_lc1_hwm_1rb"/>

## Accessibility

You can navigate to guided development with either a mouse or a keyboard. Keyboard navigation provides a streamlined experience, allowing users to find and use guides without needing to use their mouse. Use the arrow keys to navigate within sections, the `Tab` key to navigate to new sections and controls, `Shift + Tab` to navigate back to sections and controls, and `Enter` to make selections.

Guided development supports the use of high contrast themes.

