<!-- loio0039256581704bf3a8a586d406875c90 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Progress Column

A progress indicator column can be added to a list report table or an object page section.



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


The progress column has the following additional properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Importance](appendix-457f2e9.md#loio7fe32a215209419da6d6c19da0f69ccb)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Target Type](appendix-457f2e9.md#loio678bf9265c664134a075b59fd193c64e)
-   [Target](appendix-457f2e9.md#loio7fba03aba4214ceab2130f16186f4ff2)
-   [Criticality for Micro Charts and Progress Indicators](appendix-457f2e9.md#loio19d82b5d8bc940738afcb49b51a48bed__section_xdw_kkj_kfc)
-   [Tooltip Source](appendix-457f2e9.md#loiof0bc466aae5b42e697c89506026050af)



<a name="loio0039256581704bf3a8a586d406875c90__section_tts_fsy_35b"/>

## Moving Progress Column

To move a column within a table, use one of the following options:

-   **Drag and Drop**

    Hover over the table column outline, press and hold the mouse button while moving the mouse pointer to the different position within the table. Release the mouse button at the desired position. Eligible positions are highlighted in green.

    With drag and drop, you can move multiple columns at once by pressing [CTRL\] + [\+\]  .

-   **Arrow Icons**

    Click the <span class="SAP-icons-V5"></span>\(*Move Up*\) or <span class="SAP-icons-V5"></span> \(*Move Down*\) icon next to the column name. This option only moves one column at a time.




<a name="loio0039256581704bf3a8a586d406875c90__section_ld3_ysy_35b"/>

## Deleting Progress Column

To delete a column, perform the following steps:

1.  Navigate to a column.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

