<!-- loioa80d603f85164482b192eeeb2df535a2 -->

# Table Columns

You can add columns of different types to the table [Table](table-aaff7b1.md) or a [Table Section](table-section-fc59378.md) in the *Object Page*.

To add a table column, press [\+\] in the columns node and choose the desired column type. Then enter the requested information and choose `Add`.

> ### Note:  
> The requested information depends on the selected column type.

Once the table columns are added, you can move them within the table, delete or define additional properties for them in the properties pane. Some properties, such as *Label* and *Importance* can be defined for all table columns, others are specific to the column type. You can see a column type in the properties pane within the column header. For basic columns, the value type, such as **String** or **Decimal** is displayed. For others, its visualization, such as **Chart** or **Rating**.

The following column types are supported:

-   [Basic Columns](basic-columns-5f8c75b.md)
-   [Rating Column](rating-column-b2ba7b4.md)
-   [Progress Column](progress-column-0039256.md)
-   [Chart Column](chart-column-b78b302.md)
-   [Table Actions](table-actions-da1931b.md)
-   [Contact Column](contact-column-dc5931d.md)
-   [External Navigation Column](table-actions-da1931b.md)

To add a table column, press [\+\] in the columns node and choose the desired column type. Then enter the requested information and choose [Add\].

> ### Note:  
> The requested information depends on the selected column type.

Once the table columns are added, you can move them within the table, delete or define additional properties for them in the *Property Panel*.



<a name="loioa80d603f85164482b192eeeb2df535a2__columnproperties"/>

## Maintaining Column Properties

Some column properties, such as *Label* and *Importance* can be defined for all table columns, others are specific to the column type. You can see a column type in the *Property Panel* within the column header. For basic columns, the value type, such as *String* or *Decimal* is displayed. For others, its visualization, such as *Chart* or *Rating*.

All the properties are by default accompanied with the short descriptions helping you understand and configure them. This documentation provides additional information for the relatively complex properties.

The following common properties can be configured for the columns of all types in the*Property Panel*. The remaining properties depend on the column type \(*Chart*, *Rating*, etc\) and value type \(*String*, *Date*, *Decimal*, etc\) you select in the outline. Please see [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0) for more information.



<a name="loioa80d603f85164482b192eeeb2df535a2__section_mwf_b1h_2sb"/>

## Label

When a column is added to a table, the *Page Editor* checks for the `Common.Label` and `@title` annotations on a property used as column value.

> ### Note:  
> `@title` annotation is only relevant and checked for in the CAP projects.

-   If these annotations are provided, `UI.DataField` record is generated without the **Label** property. In this case the value of `Common.Label` or `@title` property is used as a column title and displayed in the **Label** field for the column in the *Property Panel*.

    > ### Note:  
    > If you change this value in the *Property Panel*, `Common.Label` or `@title` annotations will not be affected to avoid the unexpected changes in other parts of the application. Instead the the `Label` property with a new value will be generated in the respective `UI.DataField` record and thus the change will be specific to the column title of the modified table.

-   If these annotations are not yet provided, `UI.DataField` record is added with the auto-generated label. You can then change this label for the given context in the *Property Panel*.

During deletion of the column, the annotations `Common.Label` or `@title` are not removed. Only those labels that are directly maintained in a record are deleted as the record is completely removed.



<a name="loioa80d603f85164482b192eeeb2df535a2__section_up3_szg_2sb"/>

## Importance

-   When you just add a column to the table, the importance is set to *None*. This value means that no importance is specified for the current column. You can change the importance value for table columns to indicate which of these fields should be displayed on the smaller screens such as that of smartphone or tablet.
    -   If the column importance value is defined in `UI.LineItem` residing in a lower layer \(base layer\), the corresponding value is displayed in the drop-down menu with a suffix \(base layer\). Example: High \(base layer\).
    -   If the Importance value is changed to *None*, the `UI.Importance` annotation will be deleted from the local annotation file.


> ### Note:  
> [Edit in source code\] icon is provided also when the **Importance** is set to *None*. You can use it to navigate to the `UI.DataField` record representing the table column where `UI.Importance` annotation is usually defined.

