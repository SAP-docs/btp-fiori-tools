<!-- loio3bf8025da58d49b0a03713a84cf347c0 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Chart Section

Chart section can be added either on the section node or inside the group on the subsection node.



<a name="loio3bf8025da58d49b0a03713a84cf347c0__section_m2x_tjt_g5b"/>

## Adding Chart Section

To add a chart section, perform the following steps:

1.  Click the *Object/Form Entry Page* to open the *Page Editor*.
2.  Navigate to the section node in the outline and click the :heavy_plus_sign: \(*Add*\) icon.

    A drop-down menu displaying currently supported section types is displayed.

3.  Select *Add Chart Section* from the drop-down list.

    A pop-up window with following attributes:

    -   *Label*
    -   *Entity*
    -   *Type*
    -   *Dimension*
    -   *Measure*

    A measure can be specified by selecting one of the following:

    -   Use existing measure
    -   Create new measure

    If you choose to use existing measure, select one of the available measures defined with custom or transformation aggregations in the *Name* field.

    If you choose to create new measure, choose the aggregatable property and one of the supported aggregation methods . This allows you to create a new **dynamic** measure and use it in the chart.

    > ### Note:  
    > The technical name and the label are generated automatically. You can then adjust the generated label in the *Property Panel*.

4.  Click *Add*

    As a result, you can see the following changes applied:

    -   A new `UI.Chart` and a new `UI.ReferenceFacet` with an `annotationPath` pointing to the created `UI.Chart` is added to the existing `UI.Facets`.
    -   If you chose to create a new measure, `@Analytics.AggregatedProperty` is applied to the selected aggregatable property with your chosen aggregation method.
    -   If not yet available, a new `UI.Facets` annotation is created under the entity associated with that *Object Page*.
    -   If `UI.Facets` exists on an underlying layer, the annotation in the underlying layer is overridden.
    -   For CAP CDS, a using statement is added to the overridden file if not yet there.




<a name="loio3bf8025da58d49b0a03713a84cf347c0__section_nvy_xjz_g5b"/>

## Deleting Chart Section

You can delete a section that is not required to be displayed in the UI.

To delete the section in the application, perform the following steps:

1.  Navigate to the section node in the outline.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

> ### Note:  
> This action deletes the generated `UI.ReferenceFacet` from the `UI.Facets` collection.
> 
> The `UI.Chart` annotation is cleaned up during the cleanup procedure.



<a name="loio3bf8025da58d49b0a03713a84cf347c0__section_rdb_prj_35b"/>

## Maintaining Chart Section Properties

You can update the properties of the chart and define optional properties in the *Property Panel*. For the information on changing the section label, see [Change Form Section Label](form-section-4102b3d.md#loio4102b3d63d9047c881108e6f0caae15e__changeformsectionlabel).

For the information on maintaining other chart properties, see [Maintain Analytical Chart Properties](analytical-chart-9c086ec.md#loio9c086ecaace540be83b0e50101244e78__analyticalchartproperties).



### Hidden

For more information see, [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0).

