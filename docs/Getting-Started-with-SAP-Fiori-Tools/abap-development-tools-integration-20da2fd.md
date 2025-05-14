<!-- loio20da2fd6cec64fc38d6d50641a4cf8d5 -->

# ABAP Development Tools Integration

You can launch the SAP Fiori Generator directly when working with ABAP Development Tools \(ADT\) in Eclipse. You can either launch the Application Generator from SAP Fiori tools in SAP Business Application Studio in your browser, or directly launch Visual Studio Code \(VS Code\) locally if that is your preferred integrated development environment \(IDE\).

First, you configure the integration between ADT and SAP Fiori tools. This is a one-time setup within ADT for each system you want to integrate. Proceed as follows:

1.  Choose the system you want to integrate, right-click it and select *Properties*. Then click *ABAP Development* \> *IDE Configuration*.

2.  Select the *Configure the target IDE* checkbox and choose to launch either SAP Business Application Studio or VS Code.


After the configuration, a new button is displayed alongside the service details in ADT. *Create Fiori Project* allows you to launch your IDE environment and automatically start the SAP Fiori Generator with these system details.

When you launch the SAP Fiori Generator, the data source selection step is skipped since you’ve already selected your data source in ADT, and the main entity for your template is pre-selected with the entity you chose in ADT.

Alternatively, if you have used the Quick Fiori Application generator in ADT to already deploy an application with the selected service, then you can click *Create Fiori Project* to launch SAP Fiori tools and download the deployed application into your workspace. After it is downloaded, the application is updated to support the capabilities of SAP Fiori tools.

Finally, executing the `Fiori: Download ADT Deployed App from SAPUI5 ABAP Repository` command in your IDE environment allows you to directly download an application that was deployed from ADT, without needing to launch ADT. Choose your desired system from the dropdown and you are presented with a list of SAP Fiori applications that were deployed from ADT.

> ### Note:  
> For the integration with VS Code, please ensure you have saved your ABAP system with the same system URL that is used by ADT. To check, click *SAP Fiori* \(![Wrench/Pencil icon](images/SAP_Fiori_tools_Wrench_Pencil_9d6b0f8.png)\) on the activity toolbar from the left side, then click *SAP Systems*. If the saved system cannot be matched after launching from ADT, you can choose any of the existing systems you have already saved. If you already have any SAP Fiori projects in your workspace that use the same system and main entity, you'll get the option to choose an existing matching SAP Fiori project or to create a new one with the SAP Fiori Generator.

