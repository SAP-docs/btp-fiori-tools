<!-- loio802f01cb252746468038b856b6c56c56 -->

# Adapting an Application



<a name="loio802f01cb252746468038b856b6c56c56__section_lnk_cmx_pxb"/>

## Overview

> ### Note:  
> Have in mind that this feature is in experimental state.

Extend an existing SAP Fiori application available in the on-premise system, using VS Code.



<a name="loio802f01cb252746468038b856b6c56c56__section_lvj_pyl_qxb"/>

## General Prerequisites

-   Make sure you have configured the connectivity to your on-premise ABAP system as described in [Managing System Connection](Project-Functions/managing-system-connection-78a82b6.md).
-   Activate the `/sap/bc/adt` and the `/sap/bc/ui2/app_index/` services in your on-premise ABAP system.
-   Give access to `/sap/bc/adt/discovery`.

    When creating an adaption project the created connection only needs access to the following URI `/sap/bc/adt/discovery`. Fine-granular access to adaptation resources can be controlled using authorization object `S_ADT_RES` and its URI field.




<a name="loio802f01cb252746468038b856b6c56c56__section_adaptprereq"/>

## Adaptation Project Prerequisites

Adaptation projects are currently only supported on on-premise ABAP systems with the minimum required software component version being SAP\_UI 7.54. The minimum SAPUI5 version of the base app is 1.30.

You can create an adaptation project for the following applications:

-   The application is not a scaffolding application \(an application that uses `sap.ca.scfld.md` in its `manifest.json` file\).
-   The application has a `manifest.json` file.
-   The application's SAPUI5 version in the system is 1.72 or higher.

If any of these conditions don't apply, it will not be possible to create an adaptation project.

> ### Note:  
> Adaptation project can also be used as a basis, but only when it is SAP or partner provided and with the following conditions:
> 
> -   If the selected system has SAPUI5 version lower than 1.96, you need to implement [3223667](https://me.sap.com/notes/3223667) on your system, for the adaptation project to work after the deployment.
> -   If the selected system has SAPUI5 version lower than 1.90 it does not support adaptation project as а base for a new adaptation project. You will be able to create such а project, but after deployment it will not work until the SAPUI5 version of the system is updated.

> ### Note:  
> Adaptation project does not support as a basis:
> 
> -   An application that requires a mandatory parameter to start.
> -   An application variant that has already been deployed with an adaptation project.



<a name="loio802f01cb252746468038b856b6c56c56__section_ahh_cnx_pxb"/>

## Typical Workflow for Extending an SAP Fiori Application

A typical workflow for extending an SAP Fiori application includes the following steps:

1.  [Creating the Project](creating-the-project-072f566.md).
2.  \(Optional\) Use source control, such as Git, to maintain your project source code.

    You must use the project source code to preview and modify it.

3.  [Making Adaptations](making-adaptations-2a076dd.md).
4.  [Previewing the Adaptation Project](previewing-the-adaptation-project-8701335.md).
5.  [Deploying the Adaptation Project to the ABAP Repository](deploying-the-adaptation-project-to-the-abap-repository-febf0d9.md).



<a name="loio802f01cb252746468038b856b6c56c56__section_c3y_wwh_2qb"/>

## Things to Consider

Have in mind that you **cannot deploy and use** adaptation project with a package that is enabled for ABAP for Cloud Development. You will be able to create adaptation project and use its Adaptation Editor \(Visual Editor\) but you won't be able to deploy it. In such case you can refer to [**Developer Extensibility**](https://help.sap.com/docs/ABAP_PLATFORM_NEW/b5670aaaa2364a29935f40b16499972d/155909e3569941e08831c78cf4c2d495.html) in the ABAP Platform documentation.



Adaptation project runs the preview of the applications in its Adaptation Editor \(Visual Editor\) and in a separate browser tab preview, both of which are sandbox-like environments and not within any SAP Fiori launchpad. Therefore, have in mind that features that depend on SAP Fiori launchpad may not function as expected \(for example, navigation between different applications\) when previewing the application during development, but will work after deployment and in the presence of an actual SAP Fiori launchpad.

