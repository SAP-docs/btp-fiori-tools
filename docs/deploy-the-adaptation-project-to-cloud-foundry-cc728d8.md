<!-- loiocc728d886f81438aa190c9191ca8f9ea -->

# Deploy the Adaptation Project to Cloud Foundry

Learn how to deploy the MTA project to Cloud Foundry.

To deploy the MTA project to Cloud Foundry:

1.  Right-click the `manifest.appdescr_variant` file in the `webapp` folder of the project you want to deploy.
2.  Search for `Adaptation project`, expand it and select *Deploy Application*. This triggers a console command.
3.  In the console, the properties for the project are displayed. You need to confirm these properties for the deployment process to continue. After the process ends, confirmation of the deployment is displayed.



<a name="loiocc728d886f81438aa190c9191ca8f9ea__section_ln1_zcx_rxb"/>

## How to configure a site in SAP Build Work Zone, standard edition with your adapted app

1.  In the cockpit of the subaccount, under *Instances and Subscriptions*, select *Go to application* next to *SAP Build Work Zone, standard edition* to start the site configuration.

2.  Follow the instructions in the SAP Build Work Zone, standard edition documentation. For more information, see [Run Applications in SAP Build Work Zone, standard edition](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/Cloud/en-US/490a93e539e445e6b4bf7a6e7a3f4874.html).

3.  You can also use the HTML5 Apps Content Provider. For more information, see the procedure described in [Initial Setup](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/latest/en-US/fd79b232967545569d1ae4d8f691016b.html) and [HTML5 Apps Content Provider](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/latest/en-US/ad2103e2fde342878bcf41a8ae8a0bd8.html) after the *In the Channel Manager, update the HTML5 Apps content provider to obtain the up-to-date content.* step.



<a name="loiocc728d886f81438aa190c9191ca8f9ea__undeploy"/>

## How to undeploy content

To undeploy, follow the procedure described in [Undeploying Content](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/Cloud/en-US/fb5cca52c06949358cc3a0f41fac7118.html).



<a name="loiocc728d886f81438aa190c9191ca8f9ea__alertnotifications"/>

## How to use the SAP Alert Notification service

You can create a notification in order to be informed, if the base app changes. You can retest your adaptation project with the latest base app version and rebuild/redeploy. To do so, follow the procedure described in [SAPUI5 Adaptation Project Events](https://help.sap.com/viewer/5967a369d4b74f7a9c2b91f5df8e6ab6/Cloud/en-US/2692bd54b35c48ef98beeb27aa2ac7a2.html) documentation.

**Related Information**  


[SAP Build Work Zone, standard edition](https://help.sap.com/docs/build-work-zone-standard-edition "SAP Build Work Zone, standard edition")

