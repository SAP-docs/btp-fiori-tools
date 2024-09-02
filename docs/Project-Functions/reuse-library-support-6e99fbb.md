<!-- loio6e99fbb264eb4911a8e01ae5882bc52e -->

# Reuse Library Support

Currently, a library to be used in your project has to reside in your workspace, in either SAP Business Application Studio or Visual Studio Code \(VS Code\). With SAP Fiori tools, you can reuse a library or component in your SAP Fiori apps by adding a reference to another project.



<a name="loio6e99fbb264eb4911a8e01ae5882bc52e__section_q44_n5k_wxb"/>

## Creating a Reusable Library

To create a new reusable library that can be referenced in your SAP Fiori application, do the following steps:

1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the *Fiori: Open Reusable Library Generator* command.
2.  Provide your library module name and namespace, and choose a minimum version of SAPUI5.
3.  From the Library Folder Path drop-down list, choose the directory for the new reusable library. The library folder generated consists of the namespace and module name.
4.  You can optionally choose to generate your library with *TypeScript*.



<a name="loio6e99fbb264eb4911a8e01ae5882bc52e__section_lvq_qfg_3qb"/>

## Adding Reference to Reuse a Library



### Prerequisites

1.  A reuse library project is cloned or imported into your workspace.
2.  An SAP Fiori project is already in your workspace.



### Steps

To add a reference for reusing an SAP Fiori library, perform the following steps:

1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the *Fiori: Add Reference to SAP Fiori Reusable Libraries* command.
2.  From the *Project Folder Path* drop-down list, select the SAP Fiori project that exists in your current workspace.
3.  Select *Reusable Library Source* as a workspace.
4.  Select reusable libraries or components from the list.
5.  Click *Finish*.

When you click *Finish*, the following files get updated with a reference to the selected reuse library:

-   `ui5.yaml`
-   `ui5-local.yaml`
-   `manifest.json`



<a name="loio6e99fbb264eb4911a8e01ae5882bc52e__section_a4h_r1v_j5b"/>

## Deploying a Reuse Library Project Using SAP Fiori tools

Deploying a Reuse Library Project using SAP Fiori tools.

1.  Add a Reuse Library project to your workspace.
2.  In the resulting migration pop-up window, click on *Start Migration*.
3.  From the list, select the project that you would like to migrate.
4.  Now, click on *Start Migration*.
5.  Once the dependencies are installed, you're ready to use SAP Fiori tools to deploy to an ABAP environment.
6.  To generate the deployment configuration, see [Generate Deployment Configuration ABAP](../Deploying-an-Application/generate-deployment-configuration-abap-c06b9cb.md)
7.  To deploy the project to ABAP environment, see [Deployment to ABAP](../Deploying-an-Application/deployment-of-application-607014e.md#loio607014e278d941fda4440f92f4a324a6__abap)

