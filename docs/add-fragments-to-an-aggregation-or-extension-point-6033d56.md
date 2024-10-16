<!-- loio6033d5678a3e4416abf022624dcd5043 -->

# Add Fragments to an Aggregation or Extension Point

You have the possibility to add fragments to an aggregation of your choice, or to an extension point.



<a name="loio6033d5678a3e4416abf022624dcd5043__section_ygx_xd4_2mb"/>

## Content

-   [Add Fragments to an Aggregation](add-fragments-to-an-aggregation-or-extension-point-6033d56.md#loio6033d5678a3e4416abf022624dcd5043__addfragments)

-   [Add Fragments to an Extension Point](add-fragments-to-an-aggregation-or-extension-point-6033d56.md#loio6033d5678a3e4416abf022624dcd5043__extensionpoint)




<a name="loio6033d5678a3e4416abf022624dcd5043__addfragments"/>

## Add Fragments to an Aggregation



### Procedure

1.  In your workspace, from the project context menu, choose *SAPUI5 Visual Editor*.

    The application opens in the canvas in preview mode.

2.  From the editor header, choose *Edit*.

3.  On the UI, select a control \(such as a smart-filter bar or an overflow toolbar\), and from its context menu, choose *Add Fragment*.

    In the dialog box that opens, the default target aggregation and last index are selected. A list displays the fragments available for the selected target aggregation. You can also create fragments. Choose the target aggregation and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

    > ### Note:  
    > The index is disabled for **controlConfiguration** aggregation in the control Smart Filter Bar. This aggregation currently does not support positioning at a specific index.

4.  To create a fragment:

    1.  Choose *Create New*.

        The default target aggregation is the one you selected in the previous step.

    2.  Enter a name for the fragment and choose *Create*.

        A fragment.xml file is created in the folder: *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    3.  Define the fragment. Save and close the .xml file. For more information, see [SAPUI5 documentation](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder: *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the fragment.xml file, selected target aggregation, and index.


5.  To choose an existing fragment from the list:

    1.  Select a fragment from the list and choose *Add*.

    2.  Double click the `fragment.xml` file from the workspace to open it in the editor.

    3.  Edit the code to modify the properties of the fragment. Save and close the `.xml` file.


6.  Navigate to the canvas to see the changes that you made.

    After adding fragments, you'll be prompted to reload the SAPUI5 Visual Editor to see your changes.

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




<a name="loio6033d5678a3e4416abf022624dcd5043__extensionpoint"/>

## Add Fragments to an Extension Point



### Prerequisites

-   You are using freestyle SAPUI5 application that has extension points for basis of your adaptation project.



### Procedure

1.  In your workspace, from the project context menu, choose *SAPUI5 Visual Editor*.

    The application opens in the canvas in preview mode.

2.  From the editor header, choose *Edit*.

3.  If you expand the outline tree you will be able to see which element is a possible extension point. Then you can select the element in the tree and you will see its parent marked and highlighted in the visual part of the editor. You can then right click on that highlighted element and choose *Add fragment at extension point*.

    In the dialog box that opens, the default extension point is selected. A list displays the fragments available for the selected extension point. You can also create fragments. Choose the target extension point and the index from the list where you want to add the fragment. You cannot reuse the same fragment multiple times.

4.  To create a fragment:

    1.  Choose *Create New*.

        The default extension point is the one you selected in the previous step.

    2.  Enter a name for the fragment and choose *Create*.

        A fragment.xml file is created in the folder, *Your project name* \> *webapp* \> *changes* \> *fragments* and opens in the editor.

    3.  Define the fragment. Save and close the `.xml` file. For more information, see [SAPUI5 documentation](https://sapui5.hana.ondemand.com/#/topic/2c677b574ea2486a8d5f5414d15e21c5).

        An associated `addXML.change` file is created for every fragment in the folder, *Your project name* \> *webapp* \> *changes*. This change file contains the reference to the fragment.xml file, selected target aggregation, and index.


5.  To choose an existing fragment from the list:

    1.  Select a fragment from the list and choose *Add*.

    2.  Double click the `fragment.xml` file from the workspace to open it in the editor.

    3.  Edit the code to modify the properties of the fragment. Save and close the `.xml` file.


6.  Navigate to the canvas to see the changes that you made.

    After adding fragments, you'll be prompted to reload the SAPUI5 Visual Editor to see your changes.

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


