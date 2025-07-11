<!-- loioa05d7fc1bbbf42a0ade9fb50f6b58b56 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Header

<a name="loioe26d602fe170401abb23d963bda7dd92"/>

<!-- loioe26d602fe170401abb23d963bda7dd92 -->

## Header Properties



The following annotation-based properties can be defined on the header node of an object page:

-   [Type Name](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__TypeName)
-   [Type Name Plural](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__TypeName)
-   [Title](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__Title)
-   Description
-   [Image](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__Image)
-   [Initials](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__Initials)
-   [Icon URL](header-a05d7fc.md#loioe26d602fe170401abb23d963bda7dd92__URL)

All properties are based on the `@UI.HeaderInfo` annotation.

If `@UI.HeaderInfo` does not exist, it is created as soon as one of the properties above gets a value.

If `@UI.HeaderInfo` annotation is defined in the lower layer, such as service, the values of these properties are marked with the "\(base layer\)" suffix indicating the value origin. Once a property value has been changed, the complete annotation is copied to the local annotation file and \(base layer\) suffix is no longer displayed to indicate it.



### Type Name/Type Name Plural

`Type Name` and `Type Name Plural` are string properties describing the main object of the page. `Type Name` is displayed on the very top of the object page. `Type Name Plural` represents a plural form of the object name and is displayed as a table header on the previous page. These properties are mandatory so they are set to the empty string if they are not defined. These properties support internationalization. For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md).



### Title

Title is a property representing the main object of the page. It is displayed in the page header area. You can choose one of the direct properties of the page entity provided in the dropdown. If you set it to *None*, the title in the header of the object page is not display ed. The default text will be displayed instead. Always define the *Title* if the *Visible* property of the page header is set to `true`.

> ### Note:  
> The *None* option is not available if the *Title* is defined in a lower layer such as service.



### Image

-   Adds the `ImageUrl` property with the selected property as a value to the `UI.HeaderInfo`.
-   The value is a path pointing to string properties of the entity or of a 1 to 1 associated entity.
-   To remove the `ImageUrl` property, you can select the *None* option.

For more information on images, see: [Using Images, Initials, and Icons](https://sapui5.hana.ondemand.com/sdk/#/topic/5760b638ea274d7aab59e4e434899528.html).



### Initials

-   Adds the `Initials` property with the selected property as a value to the `UI.HeaderInfo`.
-   The value is a path pointing to string properties of the entity or of a to one associated entity.
-   To remove the `Initials` property, you can select the *None* option.



### Icon URL

-   Adds the `TypeImageUrl` property with the SAP icon text as a value to the `UI.HeaderInfo`.

    > ### Example:  
    > `sap-icon://accept`

-   The value is a string pointing to a SAP Icon such as from the Icon Explorer.

<a name="loioed6ebe654f8d4aacb472c691eb11e5e3"/>

<!-- loioed6ebe654f8d4aacb472c691eb11e5e3 -->

## Header Actions



Header actions are displayed in the object page header as buttons. You can maintain the following kinds of header actions in the *Page Editor*:



### Standard Actions

The SAP Fiori elements framework provides standard generic actions, such as *Edit* and *Delete*, by default for object pages in all applications if certain criteria are met. If these standard actions are provided, you can hide them in your application UI by activating the *Hidden* property.

Once you have activated the *Hidden* property using the toggle button, the *Hide by Property* field is displayed below. You can set the condition for dynamic hiding by selecting one of the suggested Boolean properties from the dropdown list. If the selected property evaluates to `true` at runtime, the button will be hidden; otherwise it will be displayed. You can select *None* to revert back to static hiding.

> ### Note:  
> When you hide the *Edit* button, the `UI.UpdateHidden` annotation is applied to the entity set of the respective object page. When you hide the *Delete* button, the `UI.DeleteHidden` annotation is applied.



### Annotation-Based Actions

These actions are based on the following records of the `UI.Identification` annotation, applied to the main entity of the page:

-   `UI.DataFieldForAction` with the `Determining` property set to `false` or not defined. These actions are performed within the application.
-   `UI.DataFieldForIntentBasedNavigation` actions are used for external navigation from the current application to a different \(target\) application, configured in SAP Fiori launchpad.

You can add, delete, and maintain the header actions in the same way as described in [Table Actions](table-actions-da1931b.md).

You can also add action menus to the object page header. They are based on records of type `UI.DataFieldForActionGroups` contained in a `UI.Identification` annotation that does not have a qualifier and targets the root entity of the object page.

The record `UI.DataFieldForActionGroups` has an `Actions` property which is a collection of standard action records of type `UI.DataFieldForAction` representing the action menu items. Note: When using the *Page Editor*, you can only configure action menus using annotations.

> ### Note:  
> The *Importance* and *Requires Context* properties are not relevant for the header actions.
> 
> The *Criticality* property impacts the sequence of the actions in the *Object Page* header. After you change its value from *None* to *Positive* or *Negative* \(or the other way around\), the sequence of the action nodes in the *Page Editor* outline view is automatically updated.
> 
> You cannot set the criticality for actions in an action menu. You also cannot move actions with criticality to action menus.

You can move header actions and action menus to form sections based on the same entity, as long as these actions are not semantically highlighted. You can move the actions based on the `UI.DataFieldForAction` to the footer.



### Custom Actions

Custom actions are based on application extensions. For more information, see [Adding Custom Action](maintaining-extension-based-elements-02172d2.md#loio76374b198e514b39a96176094bb8aa1b).

<a name="loio8a127fc36f5640abaab0056e632fe630"/>

<!-- loio8a127fc36f5640abaab0056e632fe630 -->

## Header Section



Header sections show the key information of the object page entity and are displayed in the header area. The visualization of this information depends on the section type.



<a name="loio8a127fc36f5640abaab0056e632fe630__header_section"/>

## Adding Header Section

To add a header section, perform the following steps:

1.  Open the *Page Editor* for an object page.
2.  Click the :heavy_plus_sign: \(*Add*\) icon next to *Header Sections*.
3.  Choose the desired section type.![Object Page Header Section](images/Fiori_tools_Object_Page_Header_Section_329d536.png)
4.  Provide the requested information. Depending on the section type you selected, different fields are needed:
    -   Form Section - Label
    -   Data Point Section - Value Source Property
    -   Progress Section - Value Source Property
    -   Rating Section - Value Source Property
    -   Micro Chart Section - Chart Type. You are prompted for more information depending on the selected chart type, same as for Chart Column.


Once the header section is generated, you can add and maintain its properties in the *Property Panel*.



### Form Section

The form header section displays a group of fields under the common label. Fields are not automatically added after you create a form header section. Add the fields you need using the :heavy_plus_sign: \(*Add*\) icon in the *Fields* node.

For more information, see [Form Section](form-section-4102b3d.md).



### Progress Section

The progress header section visualizes the numeric value you chose as an indicator of a progress towards a certain target. You can modify the generated label and a default target as well as define a description for your progress indicator, apply the semantic coloring based on the value criticality and provide a tooltip.

The target is the progress indicator that is generated based on the value you entered and the default target \(goal\) of 100. You can then modify the target by setting it to a different numeric constant or choose a numeric service property that represents a target. First, choose the target value type and then the desired number or property.

The progress header section contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Target Type](appendix-457f2e9.md#loio678bf9265c664134a075b59fd193c64e)
-   [Target](appendix-457f2e9.md#loio7fba03aba4214ceab2130f16186f4ff2)
-   [Criticality for Micro Charts and Progress Indicators](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed__section_xdw_kkj_kfc)
-   [Tooltip Source](appendix-457f2e9.md#loiof0bc466aae5b42e697c89506026050af)



### Data Point Section

The data point header section is used to display the single point of the key data. It is typically a number but can also be textual. For example, a status value. It is generated with a minimum property based on the value you entered. You can then enhance it in the *Properties Panel* with additional features, such as semantic coloring based on criticality. You can also add a tooltip describing the value. If your data point represents a numeric value, you can additionally define the measure or currency if this has not been defined in the base level.

The data point header section contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Criticality](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed)
-   [Measures and Currencies](appendix-457f2e9.md#loio8ad2438ea4ed4a52ab530ff104530f98)
-   [Tooltip Source](appendix-457f2e9.md#loiof0bc466aae5b42e697c89506026050af)



### Rating Section

The rating header section displays the numeric value you chose with the corresponding number of stars out of the certain maximum \(target\). It is generated based on the value you entered and default target value of 5. You can then modify the generated label and set the target to any other integer number in the *Properties Panel* as well as enter a description and a tooltip.

The rating header section contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Target](appendix-457f2e9.md#loio7fba03aba4214ceab2130f16186f4ff2)
-   [Tooltip Source](appendix-457f2e9.md#loiof0bc466aae5b42e697c89506026050af)



### Micro Chart Section

The *Micro Chart* header section allows you to visualize the numeric properties of your service as micro charts of different types. Micro charts are generated based on the minimum required information you entered and some assumed defaults. You can modify some of the generated chart properties as well as define optional ones in the *Properties Panel*.

Required and optional properties you can configure depend on the selected chart type.

> ### Note:  
> You cannot change the type or main value \(measure\) of the micro chart. If you need to modify one of these properties, add a new micro chart section and delete an existing one instead.

**Area Micro Chart**

An area micro chart is a trend chart. It provides information for actual and target values for a specific time range as well as criticality for the values at the specific time points. When adding this chart, you must choose a 1:n associated entity as a Value Source entity and then its properties to serve as the measures and dimensions of the chart.

The area micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Dimension](appendix-457f2e9.md#loio6514184c6c21405cab30fd41e9102897)
-   [Target Value](appendix-457f2e9.md#loioa9654b0fd63443d9b2727d1a497f84b6)
-   [Criticality Source](appendix-457f2e9.md#loioa94b995dd1dd4ee5b68dde0882a3ab29)
-   [Presentation Variant: Annotation](header-a05d7fc.md#loioa05d7fc1bbbf42a0ade9fb50f6b58b56__section_o2g_rlm_32c)

**Bullet Micro Chart**

The bullet micro chart visualizes the numeric value on a given scale. You can display the main value and additional values, such as target or forecast on the same scale. You can also set a description for your chart and apply the semantic coloring based on the value criticality.

The bullet micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Target Value](appendix-457f2e9.md#loioa9654b0fd63443d9b2727d1a497f84b6)
-   [Maximum Value Type](appendix-457f2e9.md#loio27fdaca358bb419f95290eebc86ed7da)
-   [Maximum Value](appendix-457f2e9.md#loiofb3939d43c884bf5b458657ef3f6f3be)
-   [Minimum Value Type](appendix-457f2e9.md#loiob3ecb1ff7aca434882b58f83176e8cb4)
-   [Minimum Value](appendix-457f2e9.md#loiobcca4bede254425d88e3fe13180194ed)
-   [Forecast Value](appendix-457f2e9.md#loio0cb6999ed1004cccbeb06fee763eb8bb)
-   [Criticality Source](appendix-457f2e9.md#loioa94b995dd1dd4ee5b68dde0882a3ab29)

**Column Micro Chart**

A column micro chart uses vertical bars to compare multiple values over time or across categories. One axis of the chart shows the categories being compared, the other axis represents a value. The chart dimensions and measures must come from a 1:n navigation entity. When adding this chart, you must choose a 1:n associated entity as a Value Source entity and then its properties to serve as the measures and dimensions of the chart.

The column micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Dimension](appendix-457f2e9.md#loio6514184c6c21405cab30fd41e9102897)
-   [Criticality Source](appendix-457f2e9.md#loioa94b995dd1dd4ee5b68dde0882a3ab29)
-   [Presentation Variant: Annotation](header-a05d7fc.md#loioa05d7fc1bbbf42a0ade9fb50f6b58b56__section_o2g_rlm_32c)

**Line Micro Chart**

A line micro chart displays information as a series of data points connected by a line. The chart dimensions and measures must come from a 1:n navigation entity. When adding this chart, you must choose a 1:n associated entity as a Value Source entity and then its properties to serve as the measures and dimensions of the chart.

The line micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Measures](appendix-457f2e9.md#loiof7225b8412704a6cb8a7b45fda3f56fe)
-   [Dimension](appendix-457f2e9.md#loio6514184c6c21405cab30fd41e9102897)
-   [Presentation Variant: Annotation](header-a05d7fc.md#loioa05d7fc1bbbf42a0ade9fb50f6b58b56__section_o2g_rlm_32c)

**Radial Micro Chart**

The radial micro chart displays the numeric value compared with the target. You choose both of these values when generating the radial micro chart. Then, you can choose a different numeric service property to be used as a target in the *Properties Panel*, as well as set a description for your chart and apply the semantic coloring based on the value criticality.

The radial micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Target Value](appendix-457f2e9.md#loioa9654b0fd63443d9b2727d1a497f84b6)
-   [Criticality Source](appendix-457f2e9.md#loioa94b995dd1dd4ee5b68dde0882a3ab29)<sub></sub>

**Comparison Micro Chart**

The comparison micro chart displays up to three values as bar charts with the common value range for comparing the values. The chart dimensions and measures must come from a 1:n navigation entity. When adding this chart, you must choose a 1:n associated entity as a *Value Source* entity and then its properties to serve as the measures and dimensions of the chart.

The comparison micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Dimension](appendix-457f2e9.md#loio6514184c6c21405cab30fd41e9102897)
-   [Criticality for Micro Charts and Progress Indicators](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed__section_xdw_kkj_kfc)
-   [Presentation Variant: Annotation](header-a05d7fc.md#loioa05d7fc1bbbf42a0ade9fb50f6b58b56__section_o2g_rlm_32c)

**Harvey Micro Chart**

The harvey micro chart, also known as harvey ball, displays a single value against a total expressed using the maximum value. The values for the chart must come from the same entity or a 1:1 navigation entity.

The harvey micro chart contains the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Description](appendix-457f2e9.md#loio53c6d1a41ee041e7a01918f14b4925e6)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Maximum Value](appendix-457f2e9.md#loiofb3939d43c884bf5b458657ef3f6f3be)
-   [Criticality for Micro Charts and Progress Indicators](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed__section_xdw_kkj_kfc)



<a name="loio8a127fc36f5640abaab0056e632fe630__section_w12_yrj_bsb"/>

## Moving Header Section

You can change the order of sections in the application header. Drag and drop the required section to a different position within the *Header Sections* node:

-   When dropped, the records in the `UI.Facets` collection are reordered.
-   When the SAP Fioriapplication is rendered, sections are displayed based on the records sequence in the `UI.HeaderFacets` annotation.

**Move multiple sections**

To move the multiple sections to another position, perform the following steps:

1.  Use the [Ctrl\] + [Click\]  combination to select more than one section.
2.  Drag the selected section to the desired position with your pointer.



<a name="loio8a127fc36f5640abaab0056e632fe630__section_rbl_mkv_t5b"/>

## Deleting Header Section

To delete a section, perform the following steps:

1.  Navigate to the section node in the outline.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* pop-up window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes the `UI.ReferenceFacet` record from `UI.Facets`.

> ### Note:  
> To remove the unreferenced `UI.FieldGroup` annotation, run the cleanup procedure to delete the unreferenced annotation.



<a name="loio8a127fc36f5640abaab0056e632fe630__section_o2g_rlm_32c"/>

## Sorting Micro Chart Data in Header Sections

Sorting chart data in micro chart header sections is set in the `Sort Order` property of the header section. This property is only visible if you have the `Presentation Variant` property defined for the micro chart header section. This requires SAPUI5 version 1.130 or higher defined as the `minUI5Version` in the `manifest.json` file. You can only sort chart data in micro charts that are area, line, column, or comparison type.



### Presentation Variant

The `Presentation Variant` property shows the `UI.PresentationVariant` annotation that defines the micro chart header section's presentation options, such as sorting. To view the sorting properties, you must set the *Presentation Variant: Annotation* to *New*.

When the *Presentation Variant: Annotation* is set, you can define one or more direct properties of the entity by which to sort the header section. Under *Presentation Variant: Sort Order*, click *Add Sort Property*. A new table row for the sort property is added with *Property* and *Direction* fields. Choose a property and direction to sort by to update the sorting logic for your micro chart in the header section.

-   You can define in which order multiple sort order properties apply by moving them up and down within the sort property.

-   You can remove the reference to the `UI.PresentationVariant` annotation generated by the *Page Editor* by setting the *Presentation Variant: Annotation* to *None*.

-   You can remove unreferenced `UI.PresentationVariant` annotations generated by the *Page Editor* from the annotation file, run the cleanup procedure. This also removes the other unreferenced `UI.PresentationVariant` annotations defined with qualifiers to keep your annotation file as clean as possible.


