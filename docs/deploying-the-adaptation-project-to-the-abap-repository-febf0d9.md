<!-- loiofebf0d9e3266451b8fc751ed25736ce1 -->

# Deploying the Adaptation Project to the ABAP Repository

Learn how to deploy an adaptation project to the ABAP repository.



<a name="loiofebf0d9e3266451b8fc751ed25736ce1__prereq_zmv_gz1_fdc"/>

## Prerequisites

> ### Note:  
> This prerequisite is only valid for on-premise developers who deploy their adaptation projects to SAP NW AS ABAP.

If the `SAP_UI` version is 7.55 or above, your user must have the `SAP_UI_FLEX_DEVELOPER` role assigned. If the `SAP_UI` version is below 7.55, your user must have the `S_DEVELOP` role assigned. If you use a cloud connector, `POST` and `PUT` requests must be allowed for the path: `/sap/bc/lrep/dta_folder/`.



<a name="loiofebf0d9e3266451b8fc751ed25736ce1__context_anv_gz1_fdc"/>

## Context

After you have created the app variant, you deploy it to your ABAP system. Since the app variant is a new semantic app with a new ID, you also need to configure a new target mapping for the app variant to create a new tile on the SAP Fiori launchpad.



<a name="loiofebf0d9e3266451b8fc751ed25736ce1__steps_bnv_gz1_fdc"/>

## Procedure

1.  Right-click the main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and click *Open Deployment Wizard*.

2.  Choose the system you want to use to deploy the project. The system you have used to create the project will be selected by default. Click *Next* to continue.

3.  Depending on whether you have previously deployed this project to the selected system, perform the following steps:

    -   If you have not previously deployed this project to the selected system, you need to enter the package to be used for the deployment. If the package entered does not require a transport request number, click *Finish*. If the package does require a transport request number, enter the transport request number on the next page. Click *Finish*.

    -   If you have deployed this project to the system, you need to choose the type of operation you want to perform. Click *Update* and then click *Finish* to start the deployment process.


4.  You will be notified if the deployment process is successful or if there was an error.

    The UI changes you made in the adaptation project are applied to the layered repository in the selected SAP NetWeaver Application Server ABAP for your application. To add the new app variant to the SAP Fiori launchpad, you need to configure target mappings in the SAP Fiori launchpad designer. For more information, see [Configuring Target Mappings](https://help.sap.com/docs/ABAP_PLATFORM_NEW/a7b390faab1140c087b8926571e942b7/33daedef95454af68903ef1238aa0373.html?version=latest).

    If the error "ZIP archive contains disallowed files or has an incorrect structure" occurs, refer to SAP Note [3073188](https://me.sap.com/notes/3073188).

    If the error "500 Internal server error" or "Transport check could not be performed" occurs, refer to SAP Note [3243791](https://me.sap.com/notes/3243791).


