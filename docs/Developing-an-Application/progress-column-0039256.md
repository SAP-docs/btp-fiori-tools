<!-- loio0039256581704bf3a8a586d406875c90 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Progress Column

A progress indicator column can be added to a *List Report* table or an *Object Page* section.



<a name="loio0039256581704bf3a8a586d406875c90__section_f3l_fxy_35b"/>

## Adding a Progress Column

To add a progress column to a table to a section, perform the following steps:

1.  Click *Add Progress Column* after clicking the :heavy_plus_sign: \(*Add*\) icon in the *Columns* node in the *Page Editor* .
2.  Select *Columns* using the tree control.
3.  Click *Add* and a new `UI.DataPoint` annotation is created with the following values:

    -   `Value` property is set to the property chosen by the user.
    -   `TargetValue`property is set to 100 by default.
    -   `Visualization` property is set to enum value **Progress**.
    -   `UI.LineItem` is updated with a new`UI.DataFieldForAnnotation` containing the reference to this `UI.DataPoint` and a `Label` property generated based on the selected value.

    > ### Note:  
    > Add progress column option is disabled if the table entity and associated entities do not have any numeric properties or all of them are already used in the table.


Column properties can be configured in the *Property Panel*.

Please see [Column Properties](table-columns-a80d603.md#loioa80d603f85164482b192eeeb2df535a2__columnproperties) and [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0) for information on defining and editing the properties.



<a name="loio0039256581704bf3a8a586d406875c90__section_tts_fsy_35b"/>

## Moving Progress Column

To move a column within a table, use one of the following options:

-   **Drag-and-drop**

    Hover over the table column outline, press and hold the mouse button while moving the mouse pointer to the different position within the table. Release the mouse button at the desired position. Eligible positions are highlighted in green.

    With drag-and-drop, you can move multiple columns at once by pressing [CTRL\] + [\+\]  .

-   **Arrow buttons**

    Press the <span class="SAP-icons-V5"></span>\(*Move Up*\) or <span class="SAP-icons-V5"></span> \(*Move Down*\) button next to the column name. This option only moves one column at a time.




<a name="loio0039256581704bf3a8a586d406875c90__section_ld3_ysy_35b"/>

## Deleting Progress Column

To delete a column in the application, perform the following steps:

1.  Navigate to a column.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.



<a name="loio0039256581704bf3a8a586d406875c90__section_fyk_t15_s2c"/>

## Maintaining Progress Column Properties

In addition to the column properties available for all column types, you can define the following properties specific to the progress column:

-   Target Type
    -   Choose the expression type for the progress goal. It could be a constant number or a property of a numeric type if provided in the service.

-   Target
    -   Choose a number representing the progress goal.


