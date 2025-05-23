<!-- loio53706e2ca58240a789ecf6a324152513 -->

# Upgrade Safe Compatibility Rules



<a name="loio53706e2ca58240a789ecf6a324152513__section_jqz_xzb_d1c"/>

## Overview

SAPUI5 flexibility ensures a modification-free extensibility approach by separating extension code from the original application life cycle. However, applications can change their UI implementation details and enhance their service implementation compatibility during the upgrade. Developing controller extensions using these rules prevents extensions breaking after upgrading the base application and reduces the effort to adapt to changes on the UI level.

> ### Note:  
> To comply with automatic upgrades, an adaptation project deployed to an SAP S/4HANA Cloud system contains a runnable snapshot of the base application containing all UI artifacts as well as a local copy of all UI annotations. Once the base application is upgraded, the snapshot ensures that the extended application is still running, and stable even in case of conflicts between extension coding and new UI implementation details. However, you still need to solve these conflicts and deploy a new version of your adaptation project to benefit from the upgraded version as well as to receive support for the base app functionality.

To check whether the base app of an adaptation project is up-to-date, see [Check Whether Your Adaptation Project Is Up-To-Date with Base App Upgrades](check-whether-your-adaptation-project-is-up-to-date-with-base-app-upgrades-c6ef105.md).



<a name="loio53706e2ca58240a789ecf6a324152513__section_pnr_q1c_d1c"/>

## Rules for Controller Extensions

-   Follow the general [Best Practices for Developers](https://ui5.sap.com/#/topic/28fcd55b04654977b63dacbee0552712).

-   Only access controls with stable IDs. Never rely on the order of controls in the aggregations or parent-child chain.
-   Always check that a control you are accessing exists and that it is of an expected control type before calling any further methods of the control.

    This also applies to controls added using an adaptation project which can be added added by [Add Fragments to an Aggregation or Extension Point](add-fragments-to-an-aggregation-or-extension-point-6033d56.md) changes or controller coding.

-   Don't call or override any private or protected methods of SAPUI5 app coding.
-   Don’t use any deprecated SAPUI5 artifacts \(controls, properties, methods, or other\).
-   Value helps are not part of the SAP internal stability contract \(for example, they might change after an upgrade\). Do not use value help entity sets in the controller coding and for data binding of controls in XML fragments.
-   For SAP Fiori elements-based applications, follow the guide [Extending Delivered Apps Using Adaptation Extension](https://ui5.sap.com/#/topic/52fc48b479314d0688be24f699778c47).
-   Reuse components might change. Always write resilient coding when accessing any functionality of a reuse component to handle unexpected errors and failures gracefully.
-   The OData metadata can change during the app upgrade so do not hard code against any property values.

