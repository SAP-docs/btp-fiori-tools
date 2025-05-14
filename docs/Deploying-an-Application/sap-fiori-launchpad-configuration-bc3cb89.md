<!-- loiobc3cb890dbb84d51ae80394821ce4990 -->

# SAP Fiori Launchpad Configuration

Depending on deployment to Cloud Foundry or ABAP, you can add configuration to deploy the application to SAP Fiori launchpad.



You can create the configuration required to run the application in an SAP Fiori launchpad. You can use the command: `Fiori: Add Fiori Launchpad Configuration` to launch the wizard which helps update the application's `manifest.json` file with the required inbound navigation property, required for integrating with the SAP Fiori launchpad.


<table>
<tr>
<td valign="top">

Semantic Object

</td>
<td valign="top">

name<unique\>

</td>
</tr>
<tr>
<td valign="top">

Action

</td>
<td valign="top">

display

</td>
</tr>
<tr>
<td valign="top">

Title

</td>
<td valign="top">

Title of an application

</td>
</tr>
<tr>
<td valign="top">

Subtitle \(Optional\)

</td>
<td valign="top">

Subtitle to be used by the tile

</td>
</tr>
</table>

Additionally, from the terminal, you can use the [@sap-ux/create](https://github.com/SAP/open-ux-tools/tree/main/packages/create#sap-uxcreate) module to add SAP Fiori launchpad configuration.

