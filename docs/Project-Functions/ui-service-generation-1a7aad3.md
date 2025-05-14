<!-- loio1a7aad346618443a86ebd7250bac0ef0 -->

# UI Service Generation

Use the UI Service Generator to create a UI service for your SAP Fiori project.



## Procedure

1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori: Generate UI Service command`.

2.  Select the following depending on your integrated development environment \(IDE\):

    -   Visual Studio Code: Select a saved SAP system.
    -   SAP Business Application Studio: Select a destination.

3.  Select *Business Object Interface* or *ABAP Core Data Service*.

4.  Select an object from the dropdown.

5.  Click *Next*.

6.  Select a *Package*.

7.  Select a *Transport Request*.

8.  \(Optional\) Select the *Yes* radio button for *Draft Enabled*. Note: The *Draft Enabled* prompt is only available if the selected business object supports drafts.

9.  \(Optional\) Select the *Yes* radio button for *Do you want to create an SAP Fiori application with the newly generated service?*

10. Click *Finish*.




<a name="loio1a7aad346618443a86ebd7250bac0ef0__result_epm_s3l_ncc"/>

## Results

The UI service is generated. This can take some time.

If you have chosen to create an SAP Fiori application with the newly generated service, the SAP Fiori Generator will automatically launch and the service will be used in the generated SAP Fiori application.

