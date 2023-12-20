<!-- loiobdb6561e8c554b29bb6f6ebe0279e5c5 -->

# Add Fragments to an Aggregation or Extension Point



<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__section_ygx_xd4_2mb"/>

## Content

-   [Add Fragments to an Aggregation](add-fragments-to-an-aggregation-or-extension-point-bdb6561.md#loiobdb6561e8c554b29bb6f6ebe0279e5c5__addfragments)

-   [Add Fragments to an Extension Point](add-fragments-to-an-aggregation-or-extension-point-bdb6561.md#loiobdb6561e8c554b29bb6f6ebe0279e5c5__extensionpoint)




<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__addfragments"/>

## Add Fragments to an Aggregation



### Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file an choose *Preview Application*. Choose *start-editor*.

    The application opens in the canvas in UI Adaptation mode.

2.  On the UI, select a control \(such as a smart-filter bar or an overflow toolbar\), and from its context menu, choose *Add Fragment*.

    In the dialog box that opens, the default target aggregation and last index are selected. Choose the target aggregation and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

    > ### Note:  
    > The index is disabled for **controlConfiguration** aggregation in the control Smart Filter Bar. This aggregation currently does not support positioning at a specific index.

3.  To create a fragment:

    1.  Enter a name for the fragment and choose *Create*.

        A fragment.xml file is created in the folder: *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    2.  Define the fragment. Save and close the .xml file. For more information, see [SAPUI5 documentation](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder: *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the fragment.xml file, selected target aggregation, and index.


4.  Navigate to the canvas to see the changes that you made.

    In order to load the added change you need to reload the browser tab in which the adaptation project editor is opened. If you have opened Preview of the application in a separate browser tab, it also needs to be refreshed.

    > ### Note:  
    > Have in mind that you should add definition of the namespace of the controls you are going to use inside of the fragment. Also, you should use stable and unique IDs for the controls you define.
    > 
    > Example:
    > 
    > ```
    > <core:FragmentDefinition xmlns:core='sap.ui.core' xmlns:uxap='sap.uxap'>
    >  <uxap:ObjectPageSection  id="sample.Id" title="Title"></uxap:ObjectPageSection>
    > </core:FragmentDefinition>
    > ```
    > 
    > Also, each control might have its own specific rules for its definition and they should be followed in order for everything to work fine.

    > ### Remember:  
    > You can delete the fragments that you create. For a seamless experience, first delete the change files associated to a fragment and then delete the fragment. If you don't delete them, you might not be able to add further fragments to the adaptation project.




<a name="loiobdb6561e8c554b29bb6f6ebe0279e5c5__extensionpoint"/>

## Add Fragments to an Extension Point



### Prerequisites

-   You are using SAPUI5 version 1.78 or above.

-   You are using SAP\_UI version 7.55 or above.
-   You are using freestyle application that has extension points for basis of your adaptation project.



### Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the `manifest.appdescr_variant` file an choose *Preview Application*. Choose *start-editor*.

    The application opens in the canvas in UI Adaptation mode.

2.  If you expand the outline tree you will be able to see which element is a possible extension point. Then you can select the element in the tree and you will see its parent marked and highlighted in the visual part of the editor. You can then right click on that highlighted element and choose *Add fragment at extension point*.

    In the dialog box that opens, the default extension point is selected. Choose the target extension point and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

3.  To create a fragment:

    1.  Enter a name for the fragment and choose *Create*.

        A fragment.xml file is created in the folder, *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    2.  Define the fragment. Save and close the `.xml` file. For more information, see [SAPUI5 documentation](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder, *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the fragment.xml file, selected target aggregation, and index.


4.  Navigate to the canvas to see the changes that you made.

    In order to load the added change you need to reload the browser tab in which the adaptation project editor is opened. If you have opened Preview of the application in a separate browser tab, it also needs to be refreshed.

    .

    > ### Note:  
    > Have in mind that you should add definition of the namespace of the controls you are going to use inside of the fragment. Also, you should use stable and unique IDs for the controls you define.
    > 
    > Example:
    > 
    > ```
    > <core:FragmentDefinition xmlns:core='sap.ui.core' xmlns:uxap='sap.uxap'>
    >   <uxap:ObjectPageSection  id="sample.Id" title="Title"></uxap:ObjectPageSection>
    > </core:FragmentDefinition>
    > ```
    > 
    > Also, each control might have its own specific rules for its definition and they should be followed in order for everything to work fine.

    > ### Remember:  
    > You can delete the fragments that you create. For a seamless experience, first delete the change files associated to a fragment and then delete the fragment. If you don't delete them, you might not be able to add further fragments to the adaptation project.


