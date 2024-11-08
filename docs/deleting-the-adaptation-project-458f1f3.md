<!-- loio458f1f3280a04df3805849f1c29ac5c5 -->

# Deleting the Adaptation Project

Learn how to delete an adaptation project.



<a name="loio458f1f3280a04df3805849f1c29ac5c5__context_yzq_v4p_qlb"/>

## Context

> ### Caution:  
> If a key user has created app variants based on the app variant you have just deleted, these will also be deleted.

There are three methods to delete an adaptation project: using the deployment tool, using the Command Line Interface \(CLI\), or using an ABAP report.

<a name="task_ubv_13p_wtb"/>

<!-- task\_ubv\_13p\_wtb -->

## Using the deployment tool



<a name="task_ubv_13p_wtb__prereq_y5l_m3p_wtb"/>

## Prerequisites

You have deployed an app variant, which have you created using an adaptation project, to your ABAP system.

You have the `SAP_UI_FLEX_DEVELOPER` role assigned.



<a name="task_ubv_13p_wtb__steps_msy_x3p_wtb"/>

## Procedure

1.  Right-click on the main folder, the `webapp` folder, or the `manifest.appdescr_variant` file and click *Open Deployment Wizard*.

2.  Choose the system you want to undeploy the project from. The system you have used to create the project will be selected by default. Click *Next* to continue.

3.  Click *Undeploy* and click *Finish* to start the undeployment.


<a name="task_ecy_r3p_wtb"/>

<!-- task\_ecy\_r3p\_wtb -->

## Using ABAP report



<a name="task_ecy_r3p_wtb__prereq_elw_kf3_3vb"/>

## Prerequisites

You have deployed an app variant, which you created using an adaptation project, to your ABAP system.

Тhe minimum required version of the software component is `SAP_UI 7.55`.



<a name="task_ecy_r3p_wtb__steps_ak2_z3p_wtb"/>

## Procedure

1.  In your project folder, open the `manifest.appdescr_variant` file in your adaptation project and copy the value of the `id` element.

2.  In the back-end system, start transaction `SE38` and execute report `/UI5/DEL_ADAPTATION_PROJECT`.

3.  Paste the copied `ID` of the app variant that you want to delete or use the [F4\] help to find it.

4.  Click *Execute* \([F8\]\).

5.  If prompted, select or create a transport request.

6.  In the overview of the files that will be deleted, click *Execute* \([Shift\] + [F1\]  \) again.




<a name="task_ecy_r3p_wtb__result_pkn_srb_fdc"/>

## Results

The app variant is deleted from all systems as soon as you release the transport request.

