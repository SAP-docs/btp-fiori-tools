<!-- loio4ecc286176b1429b98f6f0a243e49ee2 -->

# Viewing Generation Logs

Learn how to view the logs for generating an application with the Project Accelerator using SAP Fiori tools AI.

You can view the logs to learn more about how SAP Fiori tools AI generates your application and obtain further information to assist with troubleshooting.

If generation fails or the generated app is not as expected, you can open a ticket and provide the logs. For generation failures, follow the steps below. For issues with a generated app, attach a `.zip` archive of your generated project. The logs for the generated application are contained in its `.fiori-ai` folder.



<a name="loio4ecc286176b1429b98f6f0a243e49ee2__section_dbw_jbt_51c"/>

## Procedure

1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the *Developer: Set Log Level* command.

2.  Set the *Log Level* to *Info*.

    > ### Tip:  
    > You must set the log level before you generate your application and whenever the dev space is restarted.

3.  Open the Terminal \(*View* \> *Terminal* from the Menu Bar\) and click the *Output* tab.

4.  From the dropdown menu, select *SAP Fiori tools - AI*.

