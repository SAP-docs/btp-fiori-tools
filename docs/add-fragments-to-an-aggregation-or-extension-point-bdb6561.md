<!-- loiobdb6561e8c554b29bb6f6ebe0279e5c5 -->

# Add Fragments to an Aggregation or Extension Point

Learn how to add fragments to an aggregation or extension point using UI Adaption mode.



<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__section_ygx_xd4_2mb"/>

## Content

-   [Add Fragments to an Aggregation](add-fragments-to-an-aggregation-or-extension-point-bdb6561.md#loiobdb6561e8c554b29bb6f6ebe0279e5c5__addfragments)

-   [Add Fragments to an Extension Point](add-fragments-to-an-aggregation-or-extension-point-bdb6561.md#loiobdb6561e8c554b29bb6f6ebe0279e5c5__extensionpoint)




<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__addfragments"/>

## Add Fragments to an Aggregation



### Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and click *Preview Application*. Click *start-editor*.

    The application opens in the canvas in UI Adaptation mode.

2.  On the UI, select a control \(such as a smart filter bar or an overflow toolbar\), and from its context menu, click *Add Fragment*.

    In the dialog box that opens, the default target aggregation and last index are selected. Choose the target aggregation and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

    > ### Note:  
    > The index is disabled for `controlConfiguration` aggregation in the control Smart Filter Bar. This aggregation does not support positioning at a specific index.

    > ### Tip:  
    > You can use the quick actions in the top-right panel for the most common cases. To add a fragment, click on the action, enter a name for the fragment file, and choose *Create*. The generated file will contain dummy data, so you can immediately see the result in the preview when you press *Save and Reload* in the toolbar. You can then edit the generated file as needed for your extended app. The following quick actions for are provided for adding fragments:
    > 
    > -   Add Custom Page Action
    > -   Add Custom Table Action
    > -   Add Custom Table Column
    > -   Add Header Field
    > -   Add Custom Section

3.  To create a fragment:

    1.  Enter a name for the fragment and click *Create*.

        A `fragment.xml` file is created in the folder: *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    2.  Define the fragment. Save and close the `.xml` file. For more information, see [XML Fragments](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder: *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the `fragment.xml` file, selected target aggregation, and index.


4.  Navigate to the canvas to see the changes that you made.

    To load the added change, you need to reload the browser tab for the adaptation project editor and application preview \(if opened in a separate tab\).

    > ### Note:  
    > Add the definition of the namespace for the controls you are going to use inside of the fragment. Also, use stable and unique IDs for the controls you define.
    > 
    > Example:
    > 
    > ```
    > <core:FragmentDefinition xmlns:core='sap.ui.core' xmlns:uxap='sap.uxap'>
    >  <uxap:ObjectPageSection  id="sample.Id" title="Title"></uxap:ObjectPageSection>
    > </core:FragmentDefinition>
    > ```
    > 
    > Follow the definition rules for your controls. Each control can have its own specific rules.

    > ### Remember:  
    > You can delete the fragments that you create. Delete the change files associated to a fragment first and then delete the fragment. If you do not, you cannot add further fragments to the adaptation project.




<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__extensionpoint"/>

## Add Fragments to an Extension Point



### Prerequisites

-   You are using SAPUI5 version 1.78 or above.

-   You are using `SAP_UI` version 7.55 or above.
-   You are using a freestyle application that has extension points for basis of your adaptation project.



### Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and click *Preview Application*. Click *start-editor*.

    The application opens in the canvas in UI Adaptation mode.

2.  Expand the outline tree. You can see which element is a possible extension point. Then, select the element in the tree and you will see its parent marked and highlighted in the visual part of the editor. Right click on the highlighted element and click *Add fragment at extension point*.

    In the dialog box, the default extension point is selected. Choose the target extension point and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

3.  To create a fragment:

    1.  Enter a name for the fragment and click *Create*.

        A `fragment.xml` file is created in the folder, *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    2.  Define the fragment. Save and close the `.xml` file. For more information, see [SAPUI5 documentation](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder, *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the fragment.xml file, selected target aggregation, and index.


4.  Navigate to the canvas to see the changes that you made.

    To load the added change, you need to reload the browser tab for the adaptation project editor and application preview \(if opened in a separate tab\).

    > ### Note:  
    > Add the definition of the namespace for the controls you are going to use inside of the fragment. Also, use stable and unique IDs for the controls you define.
    > 
    > Example:
    > 
    > ```
    > <core:FragmentDefinition xmlns:core='sap.ui.core' xmlns:uxap='sap.uxap'>
    >   <uxap:ObjectPageSection  id="sample.Id" title="Title"></uxap:ObjectPageSection>
    > </core:FragmentDefinition>
    > ```
    > 
    > Follow the definition rules for your controls. Each control can have its own specific rules.
    > 
    > > ### Remember:  
    > > You can delete the fragments that you create. Delete the change files associated to a fragment first and then delete the fragment. If you do not, you cannot be able to add further fragments to the adaptation project.


