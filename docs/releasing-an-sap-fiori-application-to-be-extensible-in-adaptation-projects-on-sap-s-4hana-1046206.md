<!-- loio104620657c3b4723ad142e0d1f94d8e1 -->

# Releasing an SAP Fiori Application to Be Extensible in Adaptation Projects on SAP S/4HANA Cloud and SAP BTP, ABAP Environment

Ensure the UI adaptations that your customers make do not cause breaking changes when upgrading your project.



<a name="loio104620657c3b4723ad142e0d1f94d8e1__section_tmm_c1d_p1c"/>

## Prerequisites

-   Follow the best practices for developing SAPUI5 applications. For more information, see [Best Practices for Developers](https://ui5.sap.com/#/topic/28fcd55b04654977b63dacbee0552712).

-   Enable your application for UI adaptation. For more information, see [SAPUI5 Flexibility: Enable Your App for UI Adaptation](https://ui5.sap.com/#/topic/f1430c0337534d469da3a56307ff76af.html).

-   Before releasing a new version of your application, increment the version number in the `manifest.json` file, under `sap.app/applicationVersion/version`. For more information, see [Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da).

    A new version number is required for the consumer to be notified by an ATC check when the base app is updated. For more information, see [Check Whether Your Adaptation Project Is Up-To-Date with Base App Upgrades](check-whether-your-adaptation-project-is-up-to-date-with-base-app-upgrades-c6ef105.md).




<a name="loio104620657c3b4723ad142e0d1f94d8e1__section_hhm_zzc_p1c"/>

## Steps

1.  Release the OData service of your application with a C1 contract.

    Set the state of the C1 contract to *Released*.

    The C1 contract forbids incompatible changes of the structure of the service but has no restrictions for changing annotations.

    For more information, see [Setting the API Release State](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/90339a4e940e44f2be4e96bb9d3b3d4d.html).

2.  Release the BSP \(WAPA object\) of your application with a C0 contract.

    In the `manifest.json` file, set the attribute `sap.fiori/cloudDevAdaptationStatus` to `released`.

    Other allowed values are no value \(which means not released\), `deprecated`, and `obsolete`.

    As a prerequisite for providing the manifest setting, `sap.fiori/cloudDevAdaptationStatus`, the C1 contract for the OData service of the SAP Fiori application must be set to the state *Released*. The application can only be deployed if this prerequisite is met.

    In the `manifest.json` file, ensure that the attribute: `sap.app/id` has at least two segments.

3.  Release the authorization objects and the restriction types that are used by the OData service.

    Set the state of the C1 contract to *Released*.

    Select the *Use in Cloud Development* checkbox.

    > ### Note:  
    > This step is not a prerequisite for releasing the OData service and the SAP Fiori application. You can still create app variants even if the authorization objects and the restriction types of the OData service are not released. However, the authorizations of the application variant are then identical to the authorizations of the original application. Also, the original application and the original application's business catalogs must be assigned to the user's role.

4.  Create an API snapshot including the released APIs, directly before shipment, using the *Manage API Snapshots* application. For more information, see [Manage API Snapshots](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6aa39f1ac05441e5a23f484f31e477e7/8dda6b60464540e1afe50d6d03320c99.html).


Once you have set these contracts, they are enforced by ATC checks. For more information, see [Check Consistency of Release State](check-consistency-of-release-state-1f91cd4.md).

**Related Information**  


[Extend \(C0\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/2ce344a782d74d8aab073fa188af5116.html?version=latest)

[Use System-Internally \(C1\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/3ccb57a1a4d04ee192fdc2a849a89158.html?version=latest)

[Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da)

[Develop an SAP Fiori Application UI and Deploy it to SAP S/4HANA Cloud Using SAP Business Application Studio](https://help.sap.com/docs/SAP_S4HANA_CLOUD/6aa39f1ac05441e5a23f484f31e477e7/2a4ae231df8843379df7a36fa3462d4c.html)

