<!-- loio457f2e9699b5437fb09d56311055a4a0 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Appendix

<a name="loiof2b7486cb4644441979d818802b79940"/>

<!-- loiof2b7486cb4644441979d818802b79940 -->

## Criticality Representation

When *Criticality* property is defined for the basic table column or section field, the *Criticality Representation* property appears in the properties pane right after it. If you want to use the default representation defined by Fiori elements, you can leave this field set to *None*. Otherwise, you can explicitly define whether to indicate the criticality by an icon in addition to the semantic coloring. For this, choose one of the following options:

-   **With Icon** – displays the icon in addition to the semantic coloring, independent on the default representation defined by Fiori elements.
-   **Without Icon**

As a result, *Criticality Representation* property is added to the `UI.DataField` record and the respective column or field values are shown with or without the icon, independent on the default representation defined by Fiori elements presenting the table column or section field.

<a name="loio19d82b5d8bc940738afcb49b51a48bed"/>

<!-- loio19d82b5d8bc940738afcb49b51a48bed -->

## Criticality

You can display the values of the section fields or basic table columns with semantic coloring and optionally with criticality icons. For example, you can choose to display the *Travel Status* value in red if the trip is cancelled and green if it is confirmed.

As a prerequisite, your service should contain the property representing the status criticality information. If this prerequisite is fulfilled, do the following:

-   In outline, choose the table column or field you want to show with the semantic information.
-   In the Properties pane, choose the property representing the status criticality information in the *Criticality* field.

![](images/Criticallity_ac93cba.png)

As a result, *Criticality* property is added to the `UI.DataField` record and the respective column or field values are shown in semantic colors. In addition, the criticality icon may appear, that depends on the default behavior of Fiori elements template. You may override this default by explicitly defining the criticality representation.

<a name="loio53c6d1a41ee041e7a01918f14b4925e6"/>

<!-- loio53c6d1a41ee041e7a01918f14b4925e6 -->

## Description

In addition to the section label, some header section types, such as progress or micro chart, let you set the description of the content. To define the description:

1.  Open the *Page Editor*, choose the Header Section.
2.  In the Properties Pane, enter the text providing additional information for your content in the Description property.

> ### Note:  
> Similar to section label, description text can be prepared for translation. For more information see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md).

<a name="loio344568c1e4014621905d78857cf66401"/>

<!-- loio344568c1e4014621905d78857cf66401 -->

## Display as Image

If the table column or section field is built on a string property and contains a link to the image, you can set it so that it displays as an image in your application at runtime. To do so, switch on the property *Display as Image*. This applies `@UI.IsImageURL: true` to the property used for that column or field.

> ### Note:  
> -   All fields and columns in your project built on this property use the same rendering. Deleting a column or field does not remove the annotation, as this could impact other instances of the field at runtime.
> 
> -   If the property is annotated with `@UI.IsImageURL: true` in the service or in the local annotation file of the lower layer, the setting cannot be changed in the Page Editor.
> 
> -   Table columns and section fields annotated with `@Core.MediaType` along with `@Core.IsURL` are also displayed as images at runtime. However, as these annotations are applicable on the service level, they cannot be maintained using the Page Editor, and so *Display as Image* is displayed in read-only mode for such fields and columns.

<a name="loiof7ad71792a0044d6b6172f078827bdc0"/>

<!-- loiof7ad71792a0044d6b6172f078827bdc0 -->

## Hidden

Defines if the UI element is hidden in the application UI. Once you have activated the *Hidden* feature with the toggle button, the *Hide by Property* field is displayed right after it to let you set the condition for hiding.

<a name="loio4e8bb3df433546f8a80f16e53b29e4c1"/>

<!-- loio4e8bb3df433546f8a80f16e53b29e4c1 -->

## Hide by Property

In this property, you can define the condition for hiding the UI element. For this, choose one of the suggested boolean properties from the dropdown list. If the chosen property evaluates to true for the specific context, the element will be hidden, otherwise it will be displayed.

> ### Note:  
> The exact impact of hiding an element in the application UI depends on the UI element specifics. For more information, see [Hiding Features Using the UI.Hidden Annotation](https://sapui5.hana.ondemand.com/#/topic/ca00ee45fe344a73998f482cb2e669bb).

<a name="loio8ad2438ea4ed4a52ab530ff104530f98"/>

<!-- loio8ad2438ea4ed4a52ab530ff104530f98 -->

## Measures and Currencies

You can display the numeric values of the section fields or basic table columns together with measures or currencies represented by these values. For example, you can display prices along with the currencies and product dimensions, such as width or weight, with the measure unit. For this, as a prerequisite, do the following:

-   In outline, choose the table column or field you want to show with the semantic information.
-   In the Properties pane, choose one of the following options in the *Measures and Currencies* field:
    -   **Currency Unit**
    -   **Measure Unit**

-   In the pop-up, define how the unit should be represented by choosing one of the following options and clicking *Apply*:
    -   **Path** – if you want to define the unit as the property of associated entity. In this case, choose the property representing measure or currency units.
    -   **String**– if you want to define the unit as plain text, such as %. the property of associated entity. In this case, enter the text for the unit to be displayed along with the value


As a result, `Measures.ISOCurrency` annotation is applied to the field or column value referencing the property or string you chose and the respective column or field values are shown with the respective currency or measure unit.

You can change the selected measure or currency in the properties pane at any time by choosing the values in the newly appeared *Type* and *Unit* fields. You can prevent displaying the unit with your column/field value by setting the *Measures and Currencies* value to *None*.

![](images/Measure_and_Currencies_3bd7c70.png)

<a name="loiod44832d99bdf4f73ba14cdbb16dc9301"/>

<!-- loiod44832d99bdf4f73ba14cdbb16dc9301 -->

## Label Maintenance

The `Form/Table/Identification/Chart` section labels are translatable and readable elements which are rendered in the SAP Fiori apps. When the user creates a supported section, the label inputted by the user is assigned to the `Label` property of the `ReferenceFacet` record in the `Facet` annotation. During deletion of the section, the `ReferenceFacet` record is deleted which eventually deletes the `Label` in it.

> ### Note:  
> All the labels translatable and can maintained through project i18n files. For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md).



<a name="loiod44832d99bdf4f73ba14cdbb16dc9301__section_fm3_c35_j5b"/>

## Fields

-   The `Fields` labels can be maintained with annotations, such as `Common.Label` and `@title`.
-   The `Fields` sublabel can be maintained with type information of the entity property such as `name: String(50)`.
-   The navigation to the source code leads to the respective `DataField` record.
-   In case, these annotations are not present for the entity property, the `Label` property of the `DataField` is generated with the same value as the `Value` property.
-   The application does not generate the label annotations directly on the properties.
-   If you attempt to change the value of the Label provided by annotation, the annotation value is not updated. Rather the `Label` property of `DataField` is generated or updated.
-   During deletion of the field, annotations mentioned above are not deleted, only labels which are directly maintained in record are deleted as record is fully completely removed. For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md) for more information.



<a name="loiod44832d99bdf4f73ba14cdbb16dc9301__section_e3g_3l5_j5b"/>

## Columns

The `Column` labels can be maintained with annotations, such as `Common.Label` and `@title`. The `Basic Column`sublabel can be maintained with type information of the entity property such as `name: String(50)`. The navigation to the source code leads to the respective `DataField`record. The other column types such as `Rating Column`, `Progress Column` sublabel can be maintained with column type information e.g. `Type: Rating` or `Type: Progress`. In case the annotations are not maintained, the label would be empty and the user can add label through the property panel and the Label property for DataField is generated. During deletion of column, the label maintained in record gets deleted as the record is completely removed.



<a name="loiod44832d99bdf4f73ba14cdbb16dc9301__section_ysw_3l5_j5b"/>

## Actions

`Actions` has also editable labels.

-   During creation of action, we use the the last segment of actions to create the label. For example, `Trippin.Container/GetNearestAirport` the `Label` will have `GetNearestAirport` as the value assigned to it.
-   This Label would be eventually rendered as the Button Label in Fiori application. During deletion the the entire `DataFieldForAction` record is deleted, thus deleting the `Label` along with it.
-   Label based annotations are not removed during the cleanup procedure [Project Cleanup](project-cleanup-2640899.md).

<a name="loio5d1cc16e80ce48de8a47f2835a42cc47"/>

<!-- loio5d1cc16e80ce48de8a47f2835a42cc47 -->

## Text

Fields and basic table columns representing IDs or codes often need to be displayed along with the descriptive text which conveys the meaning in a human-readable way. For example, status codes: `O`, `A`, and `C` aree meaningless for the user and should be accompanied or even replaced by the descriptive text, such as Open, Accepted, Cancelled.

To add such descriptive texts, select the property representing the descriptive text in the *Text* property. Then, the `Common.Text` annotation will be applied to the property representing field/column value.

<a name="loioecd5568919bf43c5a04dd6b5e8e173f6"/>

<!-- loioecd5568919bf43c5a04dd6b5e8e173f6 -->

## Text Arrangement

When *Text* is defined, the `Text Arrangement` property appears in the properties pane right after it. If you want to use the default arrangement of Fiori elements, you can leave this field set to *None*. Otherwise, you can define how this text is displayed to the field or column value.

> ### Note:  
> The option *None* is not available if `UI.TextArrangement` or `Common.TextArrangement` is already defined on a lower layer, such as in the service.

Also, you can set the text arrangement explicitly, as follows:

-   To display both, the field/column value and text, select the *Text First* or *Text Last* values.
-   To substitute the field/column value with the text, select *Text Only*.
-   To conceal the property defined as a text in the value help, select *ID Only*.

As a result, the `UI.TextArrangement` annotation is applied to the `Common.Text` annotation defined for the text property.

<a name="loio64af370703b94edb9b4068fda3e2a613"/>

<!-- loio64af370703b94edb9b4068fda3e2a613 -->

## Tooltip

You can set tooltips for some table columns and header section types, in particular:

-   Progress Columns in *List Report* and *Object Page* tables.
-   Rating Columns in *List Report* and*Object Page* tables.
-   Progress Header Sections in *Object Page*.
-   Rating Header Sections in *Object Page*.
-   Data Point Header sections in *Object Page*.

This tooltip can be set as a fixed text or as a dynamic text coming from the service property.

To set the tooltip:

1.  Open the *Page Editor*, choose the Header Section or Column of type Supporting tooltips.
2.  In the Properties Pane, choose select the desired source of the tooltip.
    -   **String**: lets you enter the fixed translatable text.
    -   **Property**: provides a list of string service properties to choose from.

3.  Enter the tooltip text or choose the desired property based on the option you selected.

> ### Note:  
> Tooltip defined as text string can be prepared for translation. For more information, see [Internationalization \(i18n\)](internationalization-i18n-eb427f2.md).

<a name="loio43ced2fc24ac473e82ccaeb20b5f1f3f"/>

<!-- loio43ced2fc24ac473e82ccaeb20b5f1f3f -->

## Text and Text Arrangement for Fields Configured with ValueHelp

If the field display type is configured the same way as `Value Help`, you can configure the field value the same way as the `Value Help` value.

To do so, select the same property as *Text* for the field and *Value Description Property* for `Value Help`. Also, choose the same options for the text arrangement.

-   **Example 1**:

    The selected value in the *Type* filter field is consistent with the `Value Help` list values.

    ![](images/example_d6376cf.jpg)

    This is assured by the same values selected in *Text/Value Description Property* and *Text Arrangement* for the filter field and its value help. The `typedescription` property is used as *Text/Value Description Property* and *Text Only* as *Text Arrangement*.

    **Filter Field properties**:

    ![](images/Filter_Field_properties_a32bce5.jpg)

    **`Value Help` properties**:

    ![](images/Value_Help_properties_cf241c6.jpg)

-   **Example 2**:

    The selected value in the filter field is not consistent with the value help list values.

    ![](images/example_1_0556254.jpg)

    The *Text/Value Description Property* and *Text Arrangement* are configured differently on the field and value help. The `typedescription` property is used as *Value Description Property* and `Text Only` as *Text Arrangement* for the value help, while *Text* and *Text Arrangement* are not defined on the filter field itself because it is set to *None*.

    **Filter Field properties**:

    ![](images/Filter_Field_Properties_Example_2_5778877.jpg)

    **Value Help Properties**:

    ![](images/Value_Help_Properties_Example_2_dbcc00a.jpg)


The ![](images/Take_Over_Button_6452fbf.jpg) button is provided by the *Page Editor* to simplify the text/text arrangement synchronization. It appears next to the *Text* field once the *Value Description Property* is defined in the `Value Help`. When you click it, the value defined in the `Value Help` is set as *Text* for the field.

Similarly, it appears next to the *Value Description Property* field in the `Value Help`, once *Text* is defined for the field. When you click it, the value defined for the field *Text* is set for the *Value Description Property* .

> ### Note:  
> The ![](images/Take_Over_Button_6452fbf.jpg) button doesn’t appear if both properties are set in the same way.

If the values of *Value Description Property* and *Text* field are synchronized, *Text Arrangement* values are checked. If they don’t match, the ![](images/Take_Over_Button_6452fbf.jpg) button appears next to the *Text Arrangement* allowing you to synchronize one value with another.

As a result, the values in the `Common.Text` annotations applied to the field value and source value of the value help point to the same property and `UI.TextArrangement` have the same enum value.

-   *Text* and *Text Arrangement* on the filed value:

    ```
     annotate service.CapexType with {
        type @Common.Text : {
            $value : typedescription,
            ![@UI.TextArrangement] : #TextOnly,
        }
    };
    
    ```

-   *Text* and *Text Arrangement* on the source value of the value help:

    ```
    annotate service.Capex with {
        type @Common.Text : {
            $value : type.typedescription,
            ![@UI.TextArrangement] : #TextOnly,
        }
    };
    
    ```


<a name="loio90e03983431d4bfd927b51593a937955"/>

<!-- loio90e03983431d4bfd927b51593a937955 -->

## Semantic Object Name

Fields and basic table columns sometimes need to serve as links for navigation to other applications in the launchpad. Once the `manifest.json` file of the target application is configured for the inbound navigation and respective configuration is set in the launchpad, enter the semantic object name as defined in the inbound navigation of the target application.

<a name="loio7726cb0d97194461973e3ec176c8a888"/>

<!-- loio7726cb0d97194461973e3ec176c8a888 -->

## Semantic Object Property Mapping

When [Semantic Object Name](appendix-457f2e9.md#loio90e03983431d4bfd927b51593a937955) is defined, the Semantic Object Property Mapping property is enabled in the properties pane. If the semantic object property in the target application is different from the current one, provide the name of semantic object property in the target application for the correct mapping.

<a name="loio3f4dde1260b24ecdae6b5c516b4790d3"/>

<!-- loio3f4dde1260b24ecdae6b5c516b4790d3 -->

## ValueHelp

You can configure the default value help for the section fields, table columns, and filter fields unless they arere represented by properties of type Boolean or defined as read-only \(directly or via the parent entity\). To do so, you need to set the *Display Type* property to *Value help*.

To enable the value help, your service should contain the entity set representing the list of suitable values. For example, if you want to define the value help for the CapexType field, your service should have an entity set, such as CapexType containing at least one property representing available CAPEX categories.

```
entity CapexType : managed {
    key type            : String;
        typedescription : String;
}


```

When the *Value help* option is selected, the dialog window *Define Value Help Properties* appears where you provide the data source parameters for possible values:

-   **Label**

    Text displayed in the value help dialog if more than one value help is defined for the property.

-   **Value Source Entity** - Entity set representing the list of field values.

    If you work in the CAP project and the field value is defined as an association, the associated entity is suggested automatically. For example, if you configure the Value Help for the Type field defined as an association to the CapexType, Capex type will be added automatically as a value here.

    ```
    entity CapexBase : managed {
            type                : Association to CapexType;
    }
    
    ```

-   **Value Source Property** - Property to be used as an input field.

    If you work in the CAP project and the field value is defined as an association, the first key property of the associated entity is automatically suggested.

-   **Value Description Property** - Property to be used for displaying the additional text along with or instead of the input value.

    This property is usually defined if an input value *Value Source Property* represents a code or ID, and serves for explaining the meaning of that code/ID. For example, if *Value Source Property* is set to the type field representing some CapexType code, we recommend that you choose in *Value Description Property* representing the human-readable description of the Capex type.

    > ### Note:  
    > *Value Description Property* and *Text Arrangement* are similar to *Text* and *Text Arrangement* properties of Filter fields, Form section fields, and basic table columns. They result in the same annotations and are applied to the property selected as *Value Source Property*. If you expect the *Text* and *Text Arrangement* defined for the field to be the same as in the value help, click *Take Over* to apply the respective values.

-   **Text Arrangement** - Defines how the *Value Description Property* is displayed with regards to the *Value Source Property*.

    You can display them together by selecting the *Text First* or *Text Last* values or substitute the code/ID represented in *Value Source Property* with the descriptive value by selecting *Text Only*.

    > ### Note:  
    > If you select *ID only*, *Value Description Property* isn’t displayed in the value help.

-   *Display as Dropdown* checkbox - Defines if the field is displayed as a combo-box or a standard value help dialog.

    > ### Note:  
    > Check SAP Fiori guidelines to decide which option to use.

-   *Result List*

    You can let your user differentiate the available options by configuring the *Result List* table. For example, it could contain instructions on when the specific type applies and the processing rules, if any.

    To add table columns to the *Result List* table, choose the *Add Column* button and select a property for it.

    If needed, you can set the dependent filtering. For this, you choose the dependency direction in the *Dependency* column, and the respective local property in the *Local Value* column:

    -   *None:* the selected property is represented in `Common.ValueList` annotation as `ValueListParameterDisplayOnly`. At runtime, the selected value doesn't affect other fields or columns based on the same property. The *Local Value* column is not applicable in this case.

    -   *In:* the selected property is represented in `Common.ValueList` annotation as `ValueListParameterIn`. At runtime, the selected value filters the available options in other fields or columns based on the same property. When this dependency is selected, you must choose the corresponding property from the main entity in the *Local Value* column.

    -   *Out:* the selected property is represented in `Common.ValueList` annotation as `ValueListParameterOut`. The selected value will be automatically set in other fields or columns in runtime based on the same property. When this dependency is selected, you must choose the corresponding property from the main entity in the *Local Value* column.

    -   *InOut:* the selected property is represented in `Common.ValueList` annotation as `ValueListParameterInOut`. At runtime, the selected value gets both automatically set and filters the available options in other fields or columns based on the same property. When this dependency is selected, you must choose the corresponding property from the main entity in the *Local Value* column.


-   *Sort Order*

    You can define how the *Result List* is sorted by default. For example, you can choose by which property \(column\) is sorted and in which direction. You can set the sorting by multiple columns in the pre-defined order.

    > ### Note:  
    > Sorting by properties that are not part of the *Result List* is not possible. Sorting by properties of associated entities is not possible.

    To set the default sorting:

    -   Click *Add Sort Property*.

    -   Choose the property to sort by first. If needed, change the default sorting direction.

    -   Repeat to sort by additional properties \(columns\).

        You can change the sequence of properties to sort by with drag-and-drop or by clicking the <span class="SAP-icons-V5"></span> \(*Sort*\) icon in the *Sort Order* table row. You can delete the sort property by clicking the :wastebasket: \(*Delete*\) icon in the *Sort Order* table row.



Select the required value and click *Apply*.

When the configuration is done, the following annotations are generated and updated on the application layer:

-   `UI.MultiLineText`
-   `Common.ValueList`
-   `Common.ValueListWithFixedValues`
-   `Common.Text`
-   `UI.PresentationVariant` with auto-generated qualifier.

    `UI.PresentationVariant` is referenced via its qualifier in the `PresentationVariantQualifier` property of the `Common.ValueList` annotation.


These annotations map to the *Value Help* properties as follows:

![](images/Value_help_screenshot_adf0b9c.png)

> ### Note:  
> To edit previously selected properties, click *Edit properties for Value Help*.

> ### Note:  
> It is possible that several value help variants are manually defined for your application in addition to the default one. You cannot read or update such additional value helps with the *Page Editor*, but you can reecognize that they are already defined by an information message in the value help dialog. Value help variants listed in `@Common.ValueListRelevantQualifiers` are not supported.

