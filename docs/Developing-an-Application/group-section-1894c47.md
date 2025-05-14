<!-- loio1894c471d7aa4121964e497d5ffa3118 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Group Section

A Group section groups multiple sections together. It can contain a group of sections of any type except custom sections. The group section can’t contain fields/columns or actions. With several nested group sections, you can build a nested tree of sections.

> ### Note:  
> [Defining and Adapting Sections](https://sapui5.hana.ondemand.com/#/topic/facfea09018d4376acaceddb7e3f03b6).



<a name="loio1894c471d7aa4121964e497d5ffa3118__section_d3x_4sx_xrb"/>

## Adding Group Section or Subsections

To add a Group section or subsections, perform the following steps:

1.  Click the Object/Form Entry Page to open the *Page Editor*.
2.  Navigate to the section layer and click the :heavy_plus_sign: \(*Add*\) icon.

    As a result, a dropdown menu displaying currently supported section type appears.

3.  Select *Add Group Section* from the dropdown list.

    A new pop-up window *Add Group Section* appears with a field to provide a label for the section to be added.

4.  Enter a title in the *Label*text box and click *Add*.

    > ### Note:  
    > Internally, a new entry is added to the annotation `UI.Facets`. This entry is of the type `UI.CollectionFacet` with corresponding property Label and property Facets being set to an empty array. If `UI.Facets` does not exist yet or is not present in the changeable annotation file, managing process is the same as when adding a new Form section.

    A new Group tab appears in the application preview.




### Add Subsections

1.  Navigate to the Subsections node and click the :heavy_plus_sign: \(*Add*\) icon.
2.  Select the required section from the list, such as Form Section.

    A new pop-up window *Add Form Section* appears with a field to provide a label for the section to be added.

3.  Enter a title in the *Label* text box and click *Add*.

> ### Note:  
> In the new Form section, you can perform the same actions as in the classic [Form Section](form-section-4102b3d.md), such as adding, editing, moving, and deleting fields.

Label properties can be prepared for translation. For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md). In addition, see [Edit in Source Code](edit-in-source-code-7d8e942.md) feature to navigate to code fragments in the annotation file.



<a name="loio1894c471d7aa4121964e497d5ffa3118__section_udp_pxx_xrb"/>

## Moving Sections

Sections in the Group section can be moved as follows:

-   Within a Group section.
-   Between different Group sections.
-   To the top level and back.

By using the drag-and-drop functionality, drag the required section to a different position.

For more information, see [Move Basic Fields](basic-fields-2953503.md#loio2953503145dd428194c6dff252744ac1__movebasicfields).



<a name="loio1894c471d7aa4121964e497d5ffa3118__section_cwh_qxx_xrb"/>

## Deleting Group Section or Subsection

To delete the section in the application, perform the following steps:

1.  Navigate to the section layer.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> During deletion of the group section, the respective `UI.CollectionFacet` record is deleted from the `UI.Facets` annotation along with all its content.

> ### Note:  
> To clean up the unreferenced annotations for the deleted section content, you need to run the cleanup procedure that deletes the unreferenced annotation.



<a name="loio1894c471d7aa4121964e497d5ffa3118__section_yn2_2qb_zrb"/>

## Maintaining Group Section Properties



### Label

To change the section label, perform the following steps:

1.  Select the required section and navigate to the properties pane area.
2.  Enter a new name in the *Label* text box. This field defines the text to be displayed at a section label.

    As a result, the section is renamed both in the *Page Editor* and in the application preview.


See [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) for more information.

> ### Note:  
> See [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for translation if not yet there.



### Hidden

See, [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)

