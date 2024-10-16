<!-- loio104620657c3b4723ad142e0d1f94d8e1 -->

# Releasing an SAP Fiori Application to Be Extensible in Adaptation Projects on SAP S/4HANA Cloud and SAP BTP, ABAP Environment

If you develop an SAP Fiori application as an SAP partner and want to make it extensible in adaptation projects, you need to make sure that the UI adaptations made by your customers don't break during an upgrade.



<a name="loio104620657c3b4723ad142e0d1f94d8e1__section_tmm_c1d_p1c"/>

## Prerequisites

-   Follow the best practices for developing SAPUI5 applications. See [Best Practices for Developers](https://ui5.sap.com/#/topic/28fcd55b04654977b63dacbee0552712).

-   Enable your app for UI adaptation. See [SAPUI5 Flexibility: Enable Your App for UI Adaptation](https://ui5.sap.com/#/topic/f1430c0337534d469da3a56307ff76af.html).

-   Before releasing a new version of your application, increment the version number in the `manifest.json` file, under `sap.app/applicationVersion/version`. See [Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da).

    A new version number is required for the consumer to be notified by an ATC check when the base app is updated. See [Check Whether Your Adaptation Project Is Up-To-Date with Base App Upgrades](check-whether-your-adaptation-project-is-up-to-date-with-base-app-upgrades-c6ef105.md).




<a name="loio104620657c3b4723ad142e0d1f94d8e1__section_hhm_zzc_p1c"/>

## Steps

1.  Release the OData service of your application with a C1 contract.

    Set the state of the C1 contract to *Released*.

    The C1 contract forbids incompatible changes of the structure of the service, but has no restrictions for changing annotations.

    For more information, see [Setting the API Release State](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/90339a4e940e44f2be4e96bb9d3b3d4d.html).

2.  Release the BSP \(WAPA object\) of your application with a C0 contract.

    In the `manifest.json` file, set the attribute `sap.fiori/cloudDevAdaptationStatus` to `released`.

    Other allowed values are no value \(= not released\), `deprecated`, and `obsolete`.

    As a prerequisite for providing the manifest setting `sap.fiori/cloudDevAdaptationStatus`, the C1 contract for the OData service of the SAP Fiori app must be set to the state *Released*. The app can only be deployed if this prerequisite is met.

    In the `manifest.json` file, make sure that the attribute `sap.app/id` has at least 2 segments.

3.  Release the authorization objects and the restriction types that are used by the OData service.

    Set the state of the C1 contract to *Released*.

    Activate the checkbox *Use in Cloud Development*.

    > ### Note:  
    > This step is not a prerequisite for releasing the OData service and the Fiori app. You can still create app variants even if the authorization objects and the restriction types of the OData service are not released. However a drawback is that the authorizations of the application variant are then identical to the authorizations of the original application. Furthermore the original app and the original app's business catalogs have to be assigned to the user's role,

4.  Create an API snapshot including the released APIs, ideally directly before shipment, using the app *Manage API Snapshots*. See [Manage API Snapshots](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6aa39f1ac05441e5a23f484f31e477e7/8dda6b60464540e1afe50d6d03320c99.html).


Once you've set these contracts, they're enforced by ATC checks. For more information, see [Check Consistency of Release State](check-consistency-of-release-state-1f91cd4.md).

**Related Information**  


[Extend \(C0\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/2ce344a782d74d8aab073fa188af5116.html?version=latest)

[Use System-Internally \(C1\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/3ccb57a1a4d04ee192fdc2a849a89158.html?version=latest)

[Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da)

[Develop an SAP Fiori Application UI and Deploy it to SAP S/4HANA Cloud Using SAP Business Application Studio](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6aa39f1ac05441e5a23f484f31e477e7/2a4ae231df8843379df7a36fa3462d4c.html)

