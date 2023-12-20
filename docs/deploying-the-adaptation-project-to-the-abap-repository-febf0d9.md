<!-- loiofebf0d9e3266451b8fc751ed25736ce1 -->

# Deploying the Adaptation Project to the ABAP Repository



<a name="loiofebf0d9e3266451b8fc751ed25736ce1__prereq_spv_ccq_jpb"/>

## Prerequisites

This prerequisite is only valid for on premise customer developers who deploy their adaptation projects to SAP NW AS ABAP. In order to deploy, your user should be assigned to the role `SAP_UI_FLEX_DEVELOPER`, if SAP\_UI version is 7.55 and above, or to the role `S_DEVELOP`, if SAP\_UI version is below 7.55. Also, if a cloud connector is in use, `POST` and `PUT` requests should be allowed for this path: `/sap/bc/lrep/dta_folder/`.



<a name="loiofebf0d9e3266451b8fc751ed25736ce1__context_zbx_nmv_zjb"/>

## Context

After you have created the app variant, you deploy it to your ABAP system. Since the app variant is a new semantic app with a new ID, you also need to configure a new target mapping for the app variant to create a new tile on the SAP Fiori launchpad.



## Procedure

1.  Right-click the main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and select Open Deployment Wizard

2.  Choose the system you want to use to deploy the project. Have in mind that the one you have used to create the project will be selected by default. Select *Next* to continue.

3.  This step depends on if you have previously deployed this project to the selected system or not:

    -   If you haven’t previously deployed this project to the selected system, you need to enter the package to be used for the deployment. If the package entered does not require transport request number, choose *Finish*. If needed by the package, enter the transport request number on the next page. Choose *Finish*.

    -   If you have deployed this project to the system, you need to choose the type of operation you want to perform. Choose *Update* and then select *Finish* to start the process of deployment.


4.  You will be notified if the deployment process is successful, or there was some kind of an error.

    The UI changes you made in the adaptation project are applied to the layered repository in the selected SAP NetWeaver Application Server ABAP for your application. To add the new app variant to the SAP Fiori launchpad, you need to configure target mappings in the SAP Fiori launchpad designer. For more information, see [Configuring Target Mappings](https://help.sap.com/docs/ABAP_PLATFORM_NEW/a7b390faab1140c087b8926571e942b7/33daedef95454af68903ef1238aa0373.html?version=latest).

    In case of error "ZIP archive contains disallowed files or has an incorrect structure", refer to SAP Note[3073188](https://me.sap.com/notes/3073188).

    In case of error “500 Internal server error” or “Transport check could not be performed”, refer to SAP Note [3243791](https://me.sap.com/notes/3243791).


