<!-- loio458f1f3280a04df3805849f1c29ac5c5 -->

# Deleting the Adaptation Project



<a name="loio458f1f3280a04df3805849f1c29ac5c5__context_yzq_v4p_qlb"/>

## Context

> ### Caution:  
> If a key user has created further app variants based on the app variant you just deleted, these key user app variants will be deleted, as well.

There are three options – using the tool you have already used for deployment, using the Command Line Interface \(CLI\), or using an ABAP report.

<a name="task_ubv_13p_wtb"/>

<!-- task\_ubv\_13p\_wtb -->

## Using the deployment tool



<a name="task_ubv_13p_wtb__prereq_y5l_m3p_wtb"/>

## Prerequisites

You have deployed an app variant, which you created via an adaptation project, to your ABAP system.

In order to be able to delete any deployed adaptation project you should have the role `SAP_UI_FLEX_DEVELOPER` assigned.



<a name="task_ubv_13p_wtb__steps_msy_x3p_wtb"/>

## Procedure

1.  Right-click on main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and select *Open Deployment Wizard*.

2.  Choose the system you want to undeploy the project from. Have in mind that the one you have used to create the project will be selected by default. Select *Next* to continue.

3.  Choose *Undeploy* and select *Finish* to start the undeployment.


<a name="task_ecy_r3p_wtb"/>

<!-- task\_ecy\_r3p\_wtb -->

## Using ABAP report



<a name="task_ecy_r3p_wtb__prereq_elw_kf3_3vb"/>

## Prerequisites

You have deployed an app variant, which you created via an adaptation project, to your ABAP system.

Тhe minimum required version of the software component to have this report is SAP\_UI 7.55.



<a name="task_ecy_r3p_wtb__steps_ak2_z3p_wtb"/>

## Procedure

1.  In your project folder, open the `manifest.appdescr_variant` file in your adaptation project and copy the value of the id element.

2.  In the respective back-end system, start transaction SE38 and execute report `/UI5/DEL_ADAPTATION_PROJECT`.

3.  Paste the copied ID of the app variant that you want to delete, or use the F4 help to find it.

4.  Choose *Execute* \(F8\).

5.  If prompted, select or create a transport request.

6.  In the overview of the files that will be deleted, choose *Execute* \(Shift+F1\) again.

7.  The app variant is deleted from all systems as soon as you release the transport request.


