<!-- loio0b8428645243486680ffa22c0b541039 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Filter Fields



Filters are located in the filter bar and can be represented by regular filters also known as compact filters and visual filters. Compact filters are represented in runtime as filter fields with value help, whereas visual filters are represented as charts with selectable elements. Visual filters are only available if your service is enabled for analytics.

> ### Note:  
> If you work with a CAP \(Node.js\) project, some of the analytical features depend on the used OData parser. For more information, see [Release notes CAP](https://cap.cloud.sap/docs/releases/oct22?q=odata_new_parser#alp-sflight).



<a name="loio0b8428645243486680ffa22c0b541039__addingfilterfields"/>

## Adding Filter Fields

In the filter area, the user can add or remove *Filter Fields*. The *Filter Fields* are used to filter table entries in list report.

To add a *Filter Fields*, perform the following steps:

1.  Navigate to *Page Map* \> *List Report* to open a list report project.
2.  Click the :pencil2: \(*Configure Page*\) icon.

    Then, the *Filter Bar* appears.

3.  Navigate your pointer over *Filter Bar* \> *Filter Fields* or *Filter Bar* \> *Compact Filters*
4.  Click [\+\] to add a filter field.

    > ### Note:  
    > If your service is enabled for analytics but there are no visual filters in your *List Report*, choose *Add Compact Filters*.

    A new *Add Filter Fields* pop-up window with a list of available filter fields appears.

    > ### Note:  
    > Properties annotated with `UI.Hidden`, `UI.HiddenFilter`, or set as `NonFilterableProperties` within `Capabilities.FilterRestrictions` are not available for selection, as they cannot be used for filtering.

5.  Search for or select the properties to be used as filters.
6.  Choose *Add*.

While adding new *Filter Fields* the following logic applies:

-   `UI.SelectionFields` annotation is generated or updated in local annotation file.



<a name="loio0b8428645243486680ffa22c0b541039__section_h5r_vkh_hwb"/>

## Adding Visual Filters

If your service is enabled for analytics, you can define visual filters represented as bar charts in runtime. To add *Visual Filters*, perform the following steps:

1.  Navigate to *Page Map* \> *List Report* to open a list report project.
2.  Click the :pencil2: \(*Configure Page*\) icon.
3.  Navigate your pointer *Filter Bar* \> *Filter Fields* or *Filter Bar* \> *Visual Filters*.
4.  Click [\+\] to add a filter field.

    > ### Note:  
    > If your service is enabled for analytics but there are no visual filters in your *List Report*, choose *Add Visual Filters*.

    A new *Add Visual Filter* pop-up window appears.

5.  Search for or select the properties to be used as filters.

    > ### Note:  
    > Properties annotated with `UI.Hidden`, `UI.HiddenFilter`, or set as `NonFilterableProperties` within `Capabilities.FilterRestrictions` are not available for selection, as they cannot be used for filtering.
    > 
    > If you select a time-based filter field, that is, a service property of type `Edm.Date`, `Edm.Time`, `Edm.DateTime`, or `Edm.DateTimeOffset`, you can choose the chart type bar or line. You can only use a bar chart to represent your visual filter for all other types.

6.  Choose the entity that contains the appropriate filter values. Only analytically enabled entities are available for selection.
7.  Choose the property representing the filter values. It's used as a dimension in the chart representing the visual filter. Only groupable properties are available for this selection.
8.  Choose the measure for the chart representing the visual filter. You can use an existing measure, if available, or create a new one.

    > ### Note:  
    > A new measure can be created based on the aggregated property of the selected value source and supported aggregation method as long as there's no existing measure based on the same combination. Creating new measures based on properties with custom aggregations aren't supported.

    -   If you choose to use an existing measure, select one of the available measures defined with custom or transformation aggregations in the *Name* field.
    -   If you choose to create new measure, choose the aggregatable property and one of the supported aggregation methods.

9.  Select *Add*.

    A new visual filter is added with the basic properties. You can maintain additional properties of your visual filters in the *Property Panel*. A new compact filter is added for the same property if not yet defined to follow the best practices.


> ### Note:  
> Adding a visual filter updates the local annotation file and app descriptor file of your application.

The following annotations are generated in the local annotation file:

-   `UI.Chart` based on the selected measure and dimension.
-   `UI.PresentationVariant` referencing this chart.
-   `Common.ValueList` referencing the presentation variant via its qualifier.
-   `UI.SelectionFields` referencing the filter field if not yet defined.

The `manifest.json` is updated with the control configuration for the `com.sap.vocabularies.UI.v1.SelectionFields` referencing the selected filter field along with the generated `Common.ValueList` annotation.



<a name="loio0b8428645243486680ffa22c0b541039__movingfilterfields"/>

## Moving Filter Fields

To move a field within the list of the *Filter Fields* or *Compact Filters*, you can perform one of the following options:

-   Drag and drop *Filter Fields* to the desired location.
-   Press the [↑\][↓\] buttons on the UI using your mouse.
-   Use your keyboard to set the focus on the [↑\][↓\] buttons on UI and hit [Enter\].

The sequence of the property paths in `UI.SelectionFields` is adjusted, which changes the sequence of the filters in the application preview.

You can't change the sequence of the visual filters directly, as it depends on the sequence of the compact filters defined in `UI.SelectionFields`. To change the sequence of the visual filters, make sure you've defined the compact filter for the same property and then move it as described above. This changes the sequence of the property paths in `UI.SelectionFields` and the sequence of the visual filter is adjusted accordingly.



<a name="loio0b8428645243486680ffa22c0b541039__section_r1d_d1x_k5b"/>

## Deleting Filter Fields

To delete a field within the list of the *Filter Fields*, perform the following steps:

1.  Select a required filter field.
2.  Click the :wastebasket: \(*Delete*\) icon to delete it.

> ### Note:  
> The `Common.Label` annotation isn’t deleted along with the filter field, as it can also be used elsewhere in the application.

> ### Note:  
> When deleting a visual filter, only the respective configuration in `manifest.json` is removed. To remove the respective annotations from the local file, use the cleanup button.



<a name="loio0b8428645243486680ffa22c0b541039__section_ag2_xmd_s5b"/>

## Maintaining Filter Fields Properties

The following *Filter Fields* and *Compact Filter* properties are editable:

-   [Label Maintenance](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301) 
-   [Text](appendix-457f2e9.md#loio5d1cc16e80ce48de8a47f2835a42cc47)
-   [Text Arrangement](appendix-457f2e9.md#loioecd5568919bf43c5a04dd6b5e8e173f6)
-   Display Type

For more information, see [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0).



### Label

To change the label, perform the following steps:

1.  Click on the *Filter Fields* in the outline to display its properties in the properties pane.
2.  In the *Label* field, add the new text.

Removing the label text doesn't delete any `@title` and `@Common.Label` annotations defined for that property in the upper and lower layers.

> ### Note:  
> Changing the filter label has a global effect and influences all occurrences of that field in the application - unless it’s overridden there.

The following *Visual Filter* properties are editable:

-   [Measure Label](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__measure)
-   [Dimension Label](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__measure)
-   [Dimension Text](appendix-457f2e9.md#loio5d1cc16e80ce48de8a47f2835a42cc47)
-   [Dimension Text Arrangement](appendix-457f2e9.md#loio43ced2fc24ac473e82ccaeb20b5f1f3f)
-   [Measures and Currencies](appendix-457f2e9.md#loio8ad2438ea4ed4a52ab530ff104530f98)
-   [Scale Factor](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__ScaleFactor)
-   [Number of Fractional Digits](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__Number) 
-   [Sort Order](filter-fields-0b84286.md#loio0b8428645243486680ffa22c0b541039__SortOrder) 

For more information about editing measures and currencies, see [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0).

> ### Note:  
> Measure and dimension labels as well as a scale factor and Unit of Measure or currency impact the display of the visual filter title in the following order: *Measure Label* by *Dimension Label* in *Scale factor* *Measure or Currency Unit* .

> ### Note:  
> Text values for *Dimensions* should be from the same entity as the dimension.



### Measure and Dimension Labels

To change the label, perform the following steps:

1.  Choose the *Filter* in the outline to display its properties in the *Property Panel*.
2.  In the *Measures* or *Dimensions* table, change the value in the *Label* field.

If you don't define a label, the property name for the respective measure and dimension is displayed in the visual filter title.

> ### Note:  
> Changing the dimension label as well as a label of custom aggregated measure updates the `Common.Label` or `@title` annotation applied to the property used as measure or dimension. Changing the label for the measure built with transformation aggregation, updates the `Common.Label` annotation applied to `Analytics.AggregatedProperty`.



### Scale Factor

By default, the scale factor for the visual filter measure data is calculated automatically based on the data. However, you can explicitly set the desired scale factor by choosing one of the values provided in the drop-down box. If you want to use the calculated scaling factor, choose *None*.

> ### Note:  
> The scaling factor is defined in the `UI.DataPoint` annotation referenced in the `UI.Chart` annotation of the visual filter.



### Number of Fractional Digits

If the measure data in your visual filter is numeric, you can choose how many decimal places to display for it. By default no decimals are displayed, but you can set it to 1 or 2. For a currency-based measure, the number of decimal places as specified here is only considered if the scale factor is defined. Otherwise, the number of decimal places is based on the currency.



### Sort Order

You can sort the measure data in the visual filters represented by the bar chart as follows:

1.  Choose the *Add Sort Property* button. The property used for the chart measure is set as the sort property in ascending order.
2.  Choose *Descending* in the direction field to sort the measure data in descending order.

> ### Note:  
> You can't sort the chart data in the visual filters represented by the bar chart by a different property.

> ### Note:  
> You can’t sort the chart data in visual filters based on the line chart.



### Fixed Values

You can limit the data displayed in the visual filter by defining one or more filters. To do so, proceed as follows:

1.  Choose the *Add Filters* button. By default, the property used as the dimension is suggested. You can accept it or change it to any other numeric, string, or Boolean property of the visual filter entity.

2.  Define filter properties:

    -   Include/Exclude

    -   Comparison Operator

    -   Value



> ### Note:  
> By default, the *Value* is set to an empty string. If your data does not contain the empty string values, the filter shows no data until you update the *Value* field with the existing values. If you choose the operator *Between* or *Not Between* requiring two values, you must define *Low Value* and *High Value* instead of *Value* to set the lower and upper limit.

The numbers in the bar chart get updated to match the filter criteria. The list of bars in the bar chart gets limited to those matching the filters based on the dimension property.

You can repeat the steps above to add additional filters. You can then also move the individual filters up and down to change the sequence in which the filters are applied by using drag and drop or by clicking the move up/move down arrows. You can delete individual filters by using the :wastebasket: \(*Delete*\) icon.

