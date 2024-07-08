<!-- loio09171c8bc3a64ec7848f0ef31770a793 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Use Run Control



<a name="loio09171c8bc3a64ec7848f0ef31770a793__section_lqw_zf5_t4b"/>

## VS Code

Use `Run Control` \([CTRL\] + [Shift\] + [D\] \) in VS Code for different options of running your application.

-   Start **project name**. Runs the application based on the SAPUI5 version selected during the generation.
-   Start **project name** with SAPUI5 Version. Runs the application with the possibility to select from a list of SAPUI5 versions.

    > ### Note:  
    > After the SAPUI5 version is selected, the application will start automatically.

-   Start **project name** Mock. Runs the application using mock data by executing the `npm run start-mock` script. Only available in OData V2 service.
-   Start **project name** Mock with SAPUI5 Version. Runs the application using mock data and enables selection of an SAPUI5 version. Only available in OData V2 service.
-   Start **project name** Local. Runs the application using mock data against a local copy of the SAPUI5 library that was selected during generation.

In VS Code, you can aslo create additional launch configurations. To know more, see [Create a New Run Configuration in Visual Studio Code](create-a-new-run-configuration-in-visual-studio-code-3b1f37e.md).

> ### Note:  
> Using the run tool in VS Code is specific to the open workspace. If you change your workspace or folders open in VS Code, your run options may no longer be available.



<a name="loio09171c8bc3a64ec7848f0ef31770a793__section_djd_yms_v4b"/>

## SAP Business Application Studio

1.  In SAP Business Application Studio, navigate to the Run Configuration pane:

    -   One the left-side toolbar, click the <span class="SAP-icons-V5"></span> \(*Run Configuration*\) icon.
    -   On the main menu, click *View* \> *Run Configuration*.

2.  In the Run Configuration pane, see the list with different options of running your application:

    -   Start **project name**. Runs the application based on the SAPUI5 version selected during the generation.
    -   Start **project name** Mock. Runs the application using mock data by executing the `npm run start-mock` script. Only available in OData V2 service.
    -   Start **project name** Local. Runs the application using mock data against a local copy of the SAPUI5 library that was selected during generation.

    In SAP Business Application Studio, you can also create additional run configurations. To know more, see [Create a New Run Configuration in SAP Business Application Studio](create-a-new-run-configuration-in-sap-business-application-studio-05f2a9e.md).

3.  Select the required option of running your application and click the <span class="SAP-icons-V5"></span> \(*Run Module*\) icon.

