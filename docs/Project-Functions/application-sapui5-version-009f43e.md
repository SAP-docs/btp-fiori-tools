<!-- loio009f43e381234626b41e542dd7335672 -->

# Application SAPUI5 Version



<a name="loio009f43e381234626b41e542dd7335672__section_dk3_c11_cdc"/>

## Minimum SAPUI5 Version

The minimum SAPUI5 version declares the version which is required at runtime to support the features used in application development. It is set using the `minUI5Version` property in the `manifest.json` file. For more information, see [Descriptor for Applications, Components, and Libraries \(manifest.json\)](https://ui5.sap.com/#/topic/be0cf40f61184b358b5faedaec98b2da.html%23loiobe0cf40f61184b358b5faedaec98b2da/section_sap_ui5)

> ### Sample Code:  
> JSON
> 
> ```
> {
>   "sap.ui5": {
>     "dependencies": {
>       "minUI5Version": "1.120.4"
>     }
>   }
> }
> ```

If the target system does not have the required minimum SAPUI5 version, a warning message appears when deploying your application. For more information, see [Deploying an Application](../Deploying-an-Application/deploying-an-application-1b7a3be.md). The minimum SAPUI5 version is set during generation when selecting a version for the project and can also be changed using the `Fiori: Change Minimum SAPUI5 Version` command.

It is also used to determine which version of the [@sap/ux-specification](https://www.npmjs.com/package/@sap/ux-specification) module is installed to provide the matching feature set in Application Modeler and Guided Development. Changing the minimum SAPUI5 version with the `Fiori: Change Minimum SAPUI5 Version` command will update the `@sap/ux-specification` module if needed.



<a name="loio009f43e381234626b41e542dd7335672__section_m1n_3c1_cdc"/>

## SAPUI5 Preview Version

The application's minimum SAPUI5 version is used by default for previewing an application in the development environment. You can use a different version by creating a run configuration. For more information, see [Previewing an Application](../Previewing-an-Application/previewing-an-application-b962685.md).

The SAPUI5 preview version is fetched by default from `https://ui5.sap.com`. If the requested version is not found, the next higher available version is used. You can set different source paths and different default SAPUI5 preview versions by configuring `@sap/ux-ui5-tooling`. For more information, see [@sap/ux-ui5-tooling](https://www.npmjs.com/package/@sap/ux-ui5-tooling?activeTab=readme).



<a name="loio009f43e381234626b41e542dd7335672__section_tbd_gd1_cdc"/>

## SAPUI5 Deployed Version

The SAPUI5 version used for a deployed application depends on the target platform and whether an application is running standalone or embedded in the SAP Fiori launchpad.



### ABAP Environment

**SAP Fiori launchpad** 

SAP Fiori applications deployed to an ABAP environment and embedded in SAP Fiori launchpad will use the SAPUI5 version deployed in the backend. Therefore, you should use the same SAPUI5 version in your project.

**Standalone** 

If the application is running standalone using a deployed `index.html`, then the version depends on the configuration in the `index.html` file. Applications generated with the SAP Fiori Generator contain an `index.html` file with a relative path to the host:

> ### Sample Code:  
> HTML
> 
> ```
> <script id="sap-ui-bootstrap" src="resources/sap-ui-core.js">
> ```

These applications will also use the SAPUI5 version installed in the backend system. Their path can be modified to load resources directly from `https://ui5.sap.com` or a specific SAPUI5 version:

> ### Sample Code:  
> HTML
> 
> ```
> <script id="sap-ui-bootstrap" src="https://ui5.sap.com/1.114.12/resources/sap-ui-core.js">
> ```



### Cloud Foundry Environment

**SAP Build Work Zone Service** 

SAP Fiori applications deployed to Cloud Foundry run in an iFrame using the SAPUI5 version of the backend. For more information, see [SAP Build Work Zone](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/what-is-sap-build-work-zone-standard-edition).

**Standalone** 

If the application is running standalone, the `Fiori: Add Deployment Configuration` command adds a route to a destination for SAPUI5 resources to the `xs-app.json`:

> ### Sample Code:  
> JSON
> 
> ```
> {
>   "routes": [
>     {
>       "source": "^/resources/(.*)$",
>       "target": "/resources/$1",
>       "authenticationType": "none",
>       "destination": "ui5"
>     }
>   ]
> }
> ```

Also, an instance based destination pointing to `https://ui5.sap.com` is added to the `mta.yaml`:

> ### Sample Code:  
> YAML
> 
> ```
> instance:
>   destinations:
>     - Authentication: NoAuthentication
>       Name: ui5
>       ProxyType: Internet
>       Type: HTTP
>       URL: https://ui5.sap.com
> ```

By default, the application uses the latest SAPUI5 version. This can be changed in the `mta.yaml` or by configuring the generated destination service using SAP Business Technology Platform \(SAP BTP\). You can also replace the instance based destination with an account level destination. For more information, see [Configure Application Routing \(xs-app.json\)](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/configure-application-routing-xs-app-json).

