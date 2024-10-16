<!-- loio1f91cd43fa9f44bc9d45703fe5688f13 -->

# Check Consistency of Release State



This section is only relevant for developers who release their apps to be consumed in adaptation projects in SAP S/4HANA Cloud and SAP BTP, Cloud Foundry environment.

Such apps need to be released with an `Extend (C0)` contract and must keep their OData services stable \(`Use System Internally (C1)` contract\). The release state of the app is also indicated in the app's `manifest.json` file, under `sap.fiori/cloudDevAdaptationStatus`.

The ATC check *SAPUI5 Component Consistency* \(`CI_UI5_COMP`\) verifies the consistency of the release state. The following checks are performed:

-   Verify that the `sap.fiori/cloudDevAdaptationStatus` of the UI5 app in the SAPUI5 ABAP repository \(based on the BSP repository\) is the same as in the back-end system. This is relevant due to issues during the deployment or due to manual adjustments of the `manifest.json` file.

-   Verify the consistency of release states of the UI5 app and the services it uses \(C0 and C1 contracts\).


The ATC check `CI_UI5_COMP` also performs some other checks. For more information on these, see [ATC Check SAPUI5 Component Consistency](https://ui5.sap.com/#/topic/a71400bc82284449bb6c680a4516cc63).

For more information, see the following documentation:

-   [Extend \(C0\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/2ce344a782d74d8aab073fa188af5116.html) contract

-   [Use System-Internally \(C1\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/3ccb57a1a4d04ee192fdc2a849a89158.html) contract

-   [Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da)

-   [Develop an SAP Fiori Application UI and Deploy it to SAP S/4HANA Cloud Using SAP Business Application Studio](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6aa39f1ac05441e5a23f484f31e477e7/2a4ae231df8843379df7a36fa3462d4c.html)


