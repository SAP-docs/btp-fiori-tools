<!-- loioa80d603f85164482b192eeeb2df535a2 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Table Columns

You can add columns of different types to the [Table](table-aaff7b1.md) or a [Table Section](table-section-fc59378.md) in the *Object Page*.

To add a table column, click the :heavy_plus_sign: \(*Add*\) icon in the *Columns* node and select the desired column type. Then, enter the requested information and click *Add*.

Once the table columns are added, you can move them within the table, delete, or define additional properties for them in the *Property Panel*. Some properties, such as *Label* and *Importance* can be defined for all table columns. Other properties are specific to the column type. You can see a column type in the *Property Panel* within the column header. For basic columns, the value type, such as **String** or **Decimal** is displayed. For others, its visualization, such as **Chart** or **Rating**.

The following column types are supported:

-   [Basic Columns](basic-columns-5f8c75b.md)
-   [Rating Column](rating-column-b2ba7b4.md)
-   [Progress Column](progress-column-0039256.md)
-   [Chart Column](chart-column-b78b302.md)
-   [Table Actions](table-actions-da1931b.md)
-   [Contact Column](contact-column-dc5931d.md)
-   [External Navigation Column](table-actions-da1931b.md)

Once the table columns are added, you can move them within the table, delete, or define additional properties for them in the *Property Panel*.



<a name="loioa80d603f85164482b192eeeb2df535a2__columnproperties"/>

## Maintaining Column Properties

Some column properties, such as *Label* and *Importance* can be defined for all table columns. Other properties are specific to the column type. You can find the column type in the *Property Panel* within the column header. For basic columns, the value type, such as *String* or *Decimal* is displayed. For others, its visualization, such as *Chart* or *Rating*.

The following properties can be configured for all columns in the *Property Panel*. The remaining properties depend on the column type such as *Chart* or *Rating* and value type such as *String*, *Date*, *Decimal* you select. For more information, see [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0).



<a name="loioa80d603f85164482b192eeeb2df535a2__section_mwf_b1h_2sb"/>

## Label

When a column is added to a table, the *Page Editor* checks for the `Common.Label` and `@title` annotations on the property used as the column value.

> ### Note:  
> `@title` annotations are only relevant for CAP projects.

-   If these annotations are provided, the `UI.DataField` record is generated without the *Label* property. The value of the `Common.Label` or `@title` property is used as the column title and displayed in the *Label* field for the column.

    > ### Note:  
    > If you change this value in the *Property Panel*, the `Common.Label` or `@title` annotations are not affected to avoid unexpected changes in other parts of the application. Instead, a *Label* property with a new value is generated in the respective `UI.DataField` record so the change is specific to the column title of the modified table.

-   If these annotations are not yet provided, the `UI.DataField` record is added with the auto-generated label. You can then change this label for the given context in the *Property Panel*.

When a column is deleted, the `Common.Label` or `@title` annotations are not removed. Only the labels that are directly maintained in a record are deleted because the record is completely removed.



<a name="loioa80d603f85164482b192eeeb2df535a2__section_up3_szg_2sb"/>

## Importance

When you add a column to the table, the importance is set to *None*. This value means that no importance is specified for the current column. You can change the importance value for table columns to indicate which of these fields should be displayed on the small-screen devices.

If the column importance value is defined in the `UI.LineItem` residing in a lower layer \(base layer\), the corresponding value is displayed in the dropdown menu with a suffix \(base layer\). Example: High \(base layer\).

If the importance value is changed to *None*, the `UI.Importance` annotation is deleted from the local annotation file.



<a name="loioa80d603f85164482b192eeeb2df535a2__section_egg_grw_m2c"/>

## Hidden

The *Hidden* property defines if a column should be hidden in the application UI. Once you have activated the *Hidden* feature with the toggle button, you can choose the boolean property as a hiding condition in the *Hide by Property* field.

