<!-- loio4d7e85110e53425a94f72fddbc5c2a30 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Analytical Chart Actions

You can place analytical chart actions in a toolbar in an analytical chart.

With the *Page Editor*, you can configure the actions to be performed within the application as well as external navigation actions to navigate to a different application target which is configured in SAP Fiori launchpad. The actions to be performed within the application are based on the records of type `UI.DataFieldForAction`, which reference unbound actions, and the actions for navigation to the different application which are based on `UI.DataFieldForIntentBasedNavigation`. You can also define action menus.

This feature is supported in SAP Fiori elements for OData V4 applications with SAPUI5 version 1.136 and higher.

> ### Note:  
> To enable cross-application navigation, the appropriate configuration must be set in SAP Fiori launchpad and in the `manifest.json` file of the target application.
> 
> For more information about adding custom actions, see [Adding Custom Action](maintaining-extension-based-elements-02172d2.md#loio76374b198e514b39a96176094bb8aa1b).



<a name="loio4d7e85110e53425a94f72fddbc5c2a30__section_nhp_11m_zrb"/>

## Adding Actions

You can only add annotation-based chart actions if there is an available unbound action or function defined in the service. Bound actions are not supported.

You can only add external navigation actions if you know the semantic object name and action as defined in the target application.

To add an action, proceed as follows:

1.  Click the :heavy_plus_sign: \(*Add*\) icon in the *Actions* node which is inside *Chart* \> *Chart Toolbar*.
2.  Select the type of action you want to add.
3.  Provide the following information depending on the type of action:
    -   *Add Actions*: Select the *Actions* you want to add.

    -   *Add External Navigation*: Provide a *Semantic Object Name* and *Semantic Action Name*.


4.  Click *Add*.

Your action has been added to the chart toolbar.



<a name="loio4d7e85110e53425a94f72fddbc5c2a30__section_ptv_psy_pfc"/>

## Adding Action Menus

To add an action menu, proceed as follows:

1.  Click the :heavy_plus_sign: \(*Add*\) icon in the *Actions* node which is inside *Chart* \> *Chart Toolbar*.
2.  Click *Add Action Menu*.
3.  Provide a *Label* for your action menu.
4.  Select the *Source* for your action menu.
5.  Select the *Actions* you want to include in your action menu.

    > ### Note:  
    > An action cannot be added if it already exists outside of an action menu or as part of an action menu.

6.  *Manifest*: If *Manifest* is selected as the *Source*, you can also create a new custom action to add to your action menu.
7.  Click *Add*.

Your action menu has been added to the chart toolbar.



<a name="loio4d7e85110e53425a94f72fddbc5c2a30__section_yrp_b1m_zrb"/>

## Maintaining Action and Action Menu Properties

Actions and action menus support the following properties:

-   [Label](appendix-457f2e9.md#loiod44832d99bdf4f73ba14cdbb16dc9301)
-   [Hidden](appendix-457f2e9.md#loiof7ad71792a0044d6b6172f078827bdc0)
-   [Hide by Property](appendix-457f2e9.md#loio4e8bb3df433546f8a80f16e53b29e4c1)



<a name="loio4d7e85110e53425a94f72fddbc5c2a30__section_sy4_btn_qxb"/>

## Deleting Actions and Action Menus

You can delete actions and action menus by clicking the :wastebasket: \(*Delete*\) icon.

