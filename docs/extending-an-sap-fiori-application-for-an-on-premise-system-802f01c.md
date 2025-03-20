<!-- loio802f01cb252746468038b856b6c56c56 -->

# Extending an SAP Fiori Application for an On-Premise System

Discover how to extend an existing SAP Fiori application available in an on-premise system, using Visual Studio Code \(VS Code\).

> ### Caution:  
> This integration is experimental. We recommend you first try it out in a non-productive environment.



<a name="loio802f01cb252746468038b856b6c56c56__section_lvj_pyl_qxb"/>

## General Prerequisites

-   Make sure you have connected your on-premise ABAP system as described in [Managing System Connection](Project-Functions/managing-system-connection-78a82b6.md).
-   Activate the `/sap/bc/adt` and the `/sap/bc/ui2/app_index/` services in your on-premise ABAP system.
-   Give access to `/sap/bc/adt/discovery`.

    When creating an adaption project, the created connection only needs access to `/sap/bc/adt/discovery`. Fine-granular access to adaptation resources can be controlled using the authorization object `S_ADT_RES` and its URI field.




<a name="loio802f01cb252746468038b856b6c56c56__section_adaptprereq"/>

## Adaptation Project Prerequisites

Adaptation projects are only supported on on-premise ABAP systems with a minimum software component version of SAP\_UI 7.54. The minimum SAPUI5 version of the base app is 1.30.

You can create an adaptation project for applications that meet the following requirements:

-   The application has a `manifest.json` file.
-   The application's system SAPUI5 version is 1.72 or higher.
-   The application is not a scaffolding application \(an application that uses `sap.ca.scfld.md` in its `manifest.json` file\).

> ### Note:  
> Adaptation projects can also be used as a basis but only when it is SAP or partner provided and with the following conditions:
> 
> -   If the selected system has a SAPUI5 version lower than 1.96, you need to implement [3223667](https://me.sap.com/notes/3223667) on your system.
> -   If the selected system has a SAPUI5 version lower than 1.90, it does not support an adaptation project as а base for a new adaptation project. You need to update the SAPUI5 version for the project to work after deployment.

> ### Note:  
> Adaptation projects doe not support as a basis:
> 
> -   An application that requires a mandatory parameter to start.
> -   An application variant that has already been deployed with an adaptation project.



<a name="loio802f01cb252746468038b856b6c56c56__section_ahh_cnx_pxb"/>

## Typical Workflow for Extending an SAP Fiori Application

A typical workflow for extending an SAP Fiori application includes the following steps:

1.  [Creating an Adaptation Project](creating-an-adaptation-project-072f566.md)
2.  \(Optional\) Use source control, such as Git, to maintain your project source code.

    You must use the project source code to preview and modify it.

3.  [Making Adaptations](making-adaptations-2a076dd.md)
4.  [Previewing an Adaptation Project](previewing-an-adaptation-project-8701335.md)
5.  [Deploying an Adaptation Project to the ABAP Repository](deploying-an-adaptation-project-to-the-abap-repository-febf0d9.md)



<a name="loio802f01cb252746468038b856b6c56c56__section_c3y_wwh_2qb"/>

## Things to Consider

You cannot deploy and use an adaptation project with a package that is enabled for ABAP for Cloud Development. You will be able to create an adaptation project and use its Adaptation Editor but you won't be able to deploy it. For more information, see [**Developer Extensibility**](https://help.sap.com/docs/ABAP_PLATFORM_NEW/b5670aaaa2364a29935f40b16499972d/155909e3569941e08831c78cf4c2d495.html).



An adaptation project runs the preview of its applications in the Adaptation Editor and in a separate browser tab preview, both of which are sandbox-like environments and not within SAP Fiori launchpad. Therefore, features that depend on SAP Fiori launchpad may not function as expected \(for example, navigation between different applications\) when previewing the application during development but will work after deployment and in SAP Fiori launchpad.

