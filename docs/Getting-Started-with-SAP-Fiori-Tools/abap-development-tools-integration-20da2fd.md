<!-- loio20da2fd6cec64fc38d6d50641a4cf8d5 -->

# ABAP Development Tools Integration

You can launch the SAP Fiori generator directly whilst working with ABAP Development Tools \(ADT\) in Eclipse. You can either launch the Application Generator from SAP Fiori tools in SAP Business Application Studio \(BAS\) in your browser, or directly launch Visual Studio Code locally if that is your preferred integrated development environment \(IDE\).

First, you configure the integration between ADT and SAP Fiori tools. This is a one-time setup within ADT for each system you want to integrate. Proceed as follows:

1.  Choose the system you want to integrate, right-click it and select *Properties*. Then click *ABAP Development* \> *IDE Configuration*.

2.  Select the *Configure the target IDE* checkbox and choose to launch either SAP Business Application Studio or Visual Studio Code.


After the configuration, a new button is displayed alongside the service details in ADT. *Create Fiori Project* launches your IDE environment and automatically starts the SAP Fiori generator with these system details.

When you launch the SAP Fiori generator, the data source selection step is skipped since you’ve already selected your data source in ADT, and the main entity for your template is pre-selected with the entity you chose in ADT.

> ### Note:  
> For the integration with Visual Studio Code, please ensure you have saved your ABAP system with the same system URL that is used by ADT. To check, click *SAP Fiori* \(the wrench and pencil icon\) on the activity toolbar from the left side, then click *SAP Systems*. If the saved system cannot be matched after launching from ADT, you can choose any of the existing systems you have already saved.

