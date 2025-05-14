<!-- loiob78b3023e27b4078bab94189937fb550 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Chart Column

A chart column can be added to a table that is part of a *List Report* or in an *Object Page* section.

![](images/Chart_Column_b8ccb9a.png)

Depending on the desired chart type, you need to choose values for the mandatory properties.



<a name="loiob78b3023e27b4078bab94189937fb550__section_rnc_z5y_35b"/>

## Adding a Chart Column

To add a chart column to a table to a section, perform the following steps:

1.  Click *Add Chart Column* when clicking the :heavy_plus_sign: \(*Add*\) icon in the Columns node in the *Page Editor* .

    > ### Note:  
    > The *Add Chart Column* option is disabled if the table entity does not have any numeric properties.

2.  Chose a *Chart Type* using the tree control.

    > ### Note:  
    > Depending on the selected chart type, fill in additional properties as described below.

3.  Click *Add*. Depending on the desired chart type, you need to choose values for the mandatory properties.
    -   When the chart column is added, a new `UI.Chart` and `UI.DataPoint` annotation is created.


Column properties can be configured in the *Property Panel*.

For information on defining and editing the properties, see [Column Properties](table-columns-a80d603.md#loioa80d603f85164482b192eeeb2df535a2__columnproperties) and [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0).



### Chart type: Area

-   **Value Source**: property to represent the chart data.
-   **Measure**: property representing a value in the chart.
-   **Dimension**: dimension to represent the x-axis of the chart by default..



### Chart type: Bullet

-   **Value**: numeric property to represent the chart data.
-   **Maximum Value \(Path\)**: fixed number to represent the maximum possible value in the chart.

    > ### Note:  
    > You can set the Maximum Value to the numeric property in the Properties pane once you add the chart column.




### Chart type: Column

-   **Value Source**: property to represent the chart data.
-   **Measure**: property representing a value in the chart.
-   **Dimension**: dimension to represent the x-axis of the chart by default..



### Chart type: Line

-   **Value Source**: property to represent the chart data.
-   **Measure**: property representing a value in the chart.
-   **Dimension**: dimension to represent the x-axis of the chart by default..



### Chart type: Radial

-   **Value**: numeric property to represent the chart data.
-   **Target Value \(Path\)**: numeric property to represent the maximum possible value in the chart.

When a chart column is added, a new `UI.Chart` and `UI.DataPoint` annotation is created.

> ### Note:  
> The generated chart is based on the minimum required properties entered when adding the chart column. You can configure it further in the *Property Panel* by defining additional properties for the selected chart type, such as criticality, thresholds, etc.



<a name="loiob78b3023e27b4078bab94189937fb550__section_amv_mry_35b"/>

## Moving Chart Column

To move a column within a table, use one of the following options:

-   **Drag-and-drop**

    Hover over the table column outline, press and hold the mouse button while moving the mouse pointer to the different position within the table. Release the mouse button at the desired position. Eligible positions are highlighted in green.

    With drag-and-drop, you can move multiple columns at once by pressing [CTRL\] + [\+\]  .

-   **Arrow buttons**

    Press the <span class="SAP-icons-V5"></span>\(*Move Up*\) or <span class="SAP-icons-V5"></span> \(*Move Down*\) button next to the column name. This option only moves one column at a time.




<a name="loiob78b3023e27b4078bab94189937fb550__section_gg1_psy_35b"/>

## Deleting Chart Column

To delete a column in the application, perform the following steps:

1.  Navigate to a column.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.



<a name="loiob78b3023e27b4078bab94189937fb550__section_fvv_mb5_s2c"/>

## Maintaining Chart Column Properties

In addition to the column properties available for all column types, you can define the following properties specific to the chart column:

-   Maximum Value Type
    -   Choose the expression type for the maximum possible value in the chart. It could be a decimal number or a property of type decimal.

-   Maximum Value
    -   Choose a decimal number representing the maximum possible value in the chart.

-   Minimum Value Type
    -   Choose the expression type for the starting value of the chart. It could be a decimal number or a property of type decimal.

-   Minimum Value
    -   Choose a decimal number representing the starting value for the chart.

-   Forecast Value
    -   Choose a property representing the expected value.

-   Target Value
    -   Choose a property representing the target value.

-   Measures
    -   Add properties representing values for additional lines.

-   Criticality Source
    -   Choose how the chart color should be calculated. Choose Property if criticality calculation is performed in the back end and exposed as a service entity element. Choose Calculation to define the criticality calculation parameters, such as improvement direction and deviation ranges. Note: For some chart types, only one option is possible. For example, the criticality can be set either only as a property or only as calculation.


