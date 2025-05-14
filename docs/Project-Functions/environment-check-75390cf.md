<!-- loio75390cf5d81e43aea5db231ef4225268 -->

# Environment Check



<a name="loio75390cf5d81e43aea5db231ef4225268__section_fgy_xgy_dvb"/>

## Destination Checks: SAP Business Application Studio 

SAP Fiori tools environment check creates a report that you can use to troubleshoot common destination-related issues.

To use SAP Fiori tools environment check, perform the following steps:

1.  Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori: Open Environment Check` command.
2.  Click *Create destination*.
3.  Select a destination from the dropdown.
4.  If prompted, enter your credentials.
5.  To view the results, click *View the results*.
6.  To view the results and save them to a `.zip` file that you can send to SAP Product Support, click *View and Save results*.

The SAP Fiori tools environment check report has the following sections:

-   **Environment** provides the Dev Space type, Node version, and other information about the environment.
-   **Destination Details** provides destination parameters and other information about the destination.
-   **All Destination Details** lists all the destinations and their properties available to the user in the current subaccount.
-   **Messages** provides raw log messages of the chosen destination which can be useful for SAP Product Support.



<a name="loio75390cf5d81e43aea5db231ef4225268__section_nkk_cvy_dvb"/>

## Gather Environment Information: SAP Business Application Studio and Visual Studio Code

SAP Fiori tools environment check can also check and create reports on the development environment in SAP Business Application Studio or Visual Studio Code \(VS Code\). This report provides the SAP Fiori application generator version, a list of `npm` packages, and other information about your development environment.

To gather environment information, perform the following steps:

1.  Open the Command Palette in Visual Studio Code \([CMD\]/[CTRL\] + [Shift\] + [P\]\) and execute the `Fiori: Open Environment Check`command.
2.  Click *Gather environment information*.
3.  To view the results, click *View and Copy results*. The environment check details will be copied to your clipboard for easy access.
4.  To view the results and save them to a `.zip` file that you can send to SAP Product Support, click *View and Save results*.

