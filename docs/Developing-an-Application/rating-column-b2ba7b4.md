<!-- loiob2ba7b47f2be4c1cb5fcfaf2df25c19a -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Rating Column

A rating column can be added to a list report table or an object page section.



<a name="loiob2ba7b47f2be4c1cb5fcfaf2df25c19a__section_rnc_z5y_35b"/>

## Adding a Rating Column

To add a rating column to a table to a section, perform the following steps:

1.  Click *Add Rating Columns* when clicking the :heavy_plus_sign: \(*Add*\) icon in the Columns node in the *Page Editor*.
2.  Select *Columns* using the tree control.
3.  Click *Add* and a new `UI.DataPoint` annotation is created with the following values:
    -   `Value` property is set to the property chosen by the user.
    -   `TargetValue` property is set to 5.
    -   `Visualization` property is set to enum value **Rating**.


The rating column has the following additional properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Importance](appendix-457f2e9.md#loio7fe32a215209419da6d6c19da0f69ccb)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Target Value](appendix-457f2e9.md#loioa9654b0fd63443d9b2727d1a497f84b6)
-   [Tooltip Source](appendix-457f2e9.md#loiof0bc466aae5b42e697c89506026050af)



<a name="loiob2ba7b47f2be4c1cb5fcfaf2df25c19a__section_zpp_qry_35b"/>

## Moving Rating Column

To move a column within a table, use one of the following options:

-   **Drag and Drop**

    Hover over the table column outline, press and hold the mouse button while moving the mouse pointer to the different position within the table. Release the mouse button at the desired position. Eligible positions are highlighted in green.

    With drag and drop, you can move multiple columns at once by pressing [CTRL\] + [\+\]  .

-   **Arrow Icons**

    Click the <span class="SAP-icons-V5"></span>\(*Move Up*\) or <span class="SAP-icons-V5"></span> \(*Move Down*\) icon next to the column name. This option only moves one column at a time.




<a name="loiob2ba7b47f2be4c1cb5fcfaf2df25c19a__section_mvt_5sy_35b"/>

## Deleting Rating Column

1.  Navigate to a column.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

