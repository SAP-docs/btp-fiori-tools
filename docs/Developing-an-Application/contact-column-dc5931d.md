<!-- loiodc5931d0541040ab9e6126b9108b4154 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Contact Column

Contact columns can be added to a table that is part of a *List Report* or in an *Object Page* section.

![Contact Column](images/FIORI_TOOLS_CONTACT_COLUMN_0e0431c.png)



<a name="loiodc5931d0541040ab9e6126b9108b4154__section_rl2_nmz_g5b"/>

## Adding a Contact Column

To add a contact column to a table to a section, perform the following steps:

1.  Click [Add Contact Column\] when choosing [\+\] button in Columns node in the *Page Editor* .
2.  Select *Contacts* via a tree control.
3.  Click [Add\]. A new `Communication.Contact` annotation is created with Contact Name label by default. You can change the default label in the *Property Panel*.

Column properties, can be configured in the *Property Panel*.

For information on defining and editing the properties, see [Column Properties](table-columns-a80d603.md#loioa80d603f85164482b192eeeb2df535a2__columnproperties) and [Appendix](appendix-457f2e9.md#loio457f2e9699b5437fb09d56311055a4a0).



<a name="loiodc5931d0541040ab9e6126b9108b4154__section_jpx_rfv_h5b"/>

## Moving a Contact Column

To move a column within a table, use one of the following options:

-   **Drag-and-drop**

    Hover over the table column in outline, press and hold the mouse button while moving the mouse pointer to the different position within the table. Release the mouse button at the desired position. Eligible positions are highlighted in green.

    With drag-and-drop option you can move multiple columns at once by pressing CTRL+.

-   **Arrow buttons**

    Press [Move up\] or [Move down\] buttons next to the column name. This option only moves one column at a time.




<a name="loiodc5931d0541040ab9e6126b9108b4154__section_oz3_kgv_h5b"/>

## Deleting a Contact Column

To delete a column in the application, perform the following steps:

1.  Navigate to a column.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.



<a name="loiodc5931d0541040ab9e6126b9108b4154__section_d3v_nx1_vvb"/>

## Maintaining Contact Column Properties

A contact column or field has the following properties.



### Label

`Label` has the same behavior as a regular field or column. For more information, see [Maintaining Column Properties](table-columns-a80d603.md#loioa80d603f85164482b192eeeb2df535a2__columnproperties).



### Importance

`Importance` for has the same behavior as a regular field or column. For more information, see [Maintaining Column Properties](table-columns-a80d603.md#loioa80d603f85164482b192eeeb2df535a2__columnproperties).



### Contact

The *Contact* property represents the `fn` property of `Communication.Contact`. You cannot change the property used as the *Contact Name* in the *Property Panel*. If you need to have your contact column based on a different property, delete this column and click the :heavy_plus_sign: \(*Add*\) icon to add a new contact column.



### Job Title

The *Job Title* property represents the property title of `Communication.Contact`.



### Photo

The *Photo* property represents the property photo of `Communication.Contact`.



### Role

The *Role* property represents the property role of `Communication.Contact`.



### Address

The *Address* property represents the collection property `adr` of `Communication.Contact`, which has the record type `Communication.AddressType`. You can maintain multiple addresses, each represented by a table row.

The row contains the following fields:

-   *Street* - representing property street of `Communication.AddressType`
-   *City* - representing property locality of `Communication.AddressType`
-   *State/Province* - representing property region of `Communication.AddressType`
-   *Postal Code* - representing property code of `Communication.AddressType`
-   *Country* - representing property country of `Communication.AddressType`



### Phone

The *Phone* property represents the collection property `tel` of `Communication.Contact`, which has record type `Communication.PhoneNumberType`. Users can maintain multiple phone entries, each represented by a table row.

The row contains the following fields:

-   *Phone* - representing property `uri` of `Communication.PhoneNumberType`
-   *Type* - with options `Work` \(default\), `Mobile`, `Fax`, depending on if `type` of `Communication.PhoneNumberType` contains enum value `work`, `cell` or `fax` respectively.



### Email

The *Email* Property represents the collection property `email` of `Communication.Contact`, which has record type `Communication.EmailAddressType`. Users can maintain multiple email entries, each represented by a table row.

The row contains the following field:

-   *Email* - representing property email of `Communication.EmailAddressType`

