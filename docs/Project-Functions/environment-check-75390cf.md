<!-- loio75390cf5d81e43aea5db231ef4225268 -->

# Environment Check



<a name="loio75390cf5d81e43aea5db231ef4225268__section_fgy_xgy_dvb"/>

## Destination Checks: SAP Business Application Studio

SAP Fiori tools environment check creates a report that the users can use to identify and change the issues. In addition, the report also contains information that can be very useful for SAP Product Support to gather the initial set of information to further process an incident. Please note that SAP Fiori tools environment check is a tool to help troubleshoot some common destination-related issues. To use SAP Fiori tools environment check:

1.  In SAP Business Application Studio, execute the command `Fiori: Open Environment Check` and choose `Check destination`.
2.  Choose a `destination` from the quick pick.
3.  If prompted, enter credentials.
4.  To view the results, choose *View the results*.
5.  To create a zip file to be shared with SAP Product Support, choose *View and Save results*.

The environment check report for SAP Fiori tools has the following sections:

-   **Environment**: It displays all the important details like Dev Space type, node version, and other information about the environment.
-   **Destination Details**: It displays chosen destination-specific information like destination parameters. It may also contain some messages specific to SAP Fiori tools usage.
-   **All Destination Details**: This section lists all the destinations and their properties available to the user in the current subaccount.
-   **Messages**: This section has raw log messages of chosen destination which can be useful for SAP Product Support.



<a name="loio75390cf5d81e43aea5db231ef4225268__section_nkk_cvy_dvb"/>

## Gather Environment Information: SAP Business Application and VSCode

SAP Fiori tools environment check can also check and create report on the development environment in SAP Business Application Studio or VS Code. This information will be very useful to add to a support ticket so that SAP Product Support has relevant information about your development environment to start with. For example, you can have an older version of SAP Fiori application generator or some required `npm` package can be missing.

To get the environment information, follow the steps:

1.  In SAP Business Application Studio or VS Code, execute the command `Fiori: Open Environment Check` and choose `Gather environment information`.
2.  To see the results immediately, choose *View and Copy results*. The environment check details will also be copied to your clipboard for easy access.
3.  To see the results and create a zip file to be shared with SAP Product Support, choose *View and Save results*. You see a report that has details, such as tools and `npm` packages installed along with the version numbers.

