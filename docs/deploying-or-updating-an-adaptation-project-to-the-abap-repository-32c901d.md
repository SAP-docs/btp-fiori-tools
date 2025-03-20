<!-- loio32c901d0c99d4411a0d1f3ab383841be -->

# Deploying or Updating an Adaptation Project to the ABAP Repository

Deploy or update the app variant to the SAPUI5 ABAP repository in SAP S/4HANA Cloud or SAP Business Technology Platform \(SAP BTP\) system.

<a name="task_vnm_mc3_m2c"/>

<!-- task\_vnm\_mc3\_m2c -->

## Deploy or Update Using the Deployment Wizard



## Procedure

1.  Right-click the `manifest.appdescr_variant` file in the *webapp* folder of the project you want to deploy, search for *Adaptation project*, expand it and select *Open Deployment* wizard.

2.  The first step will be to set up the Fiori Launchpad Configuration of your project. If the base app has a navigation intent specified in its manifest you can choose it. If not, you need to enter semantic object, action, and parameters.

3.  Enter the title and the subtitle \(optional\) for the new tile and press *Next*.

4.  Enter the SAPUI5 ABAP repository you want to use for your deployment.

5.  \(Optional\) Enter the description for your deployment.

6.  Enter the package you want to use for your deployment.

7.  \(Optional\) If needed, you will be asked to enter a transport request number.

8.  Choose *Finish* and wait until your project gets deployed. You will be notified when the deployment process is successful.


<a name="task_a5r_yym_vvb"/>

<!-- task\_a5r\_yym\_vvb -->

## Deploy or Update Using the Command Line Interface



## Context

> ### Note:  
> Please keep your builder up-to-date by calling `npm update` and redeploy your adaptation project to ensure that there is no impact to the deployed adaptation project after an upgrade.



<a name="task_a5r_yym_vvb__steps_a2p_bzm_vvb"/>

## Procedure

1.  Open SAP Business Application Studio main menu and choose *Terminal* \> *New terminal* .

    > ### Note:  
    > When you open the terminal, ensure that you are working in the main project folder.

2.  Then, use the following command for to deploy or update your deployment: `npm run deploy`.


