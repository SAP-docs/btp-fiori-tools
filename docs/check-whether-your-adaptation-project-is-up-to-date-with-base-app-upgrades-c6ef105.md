<!-- loioc6ef105f081648a090b288cd536e11b9 -->

# Check Whether Your Adaptation Project Is Up-To-Date with Base App Upgrades

To ensure that your adaptation project is up-to-date, you need to check whether the adaptation project is still using the newest version of the base app using the ATC check, *Compare Used and Current Version of Base App* \(`UI5_BASE_APP_VERS`\).

Create an ATC check variant and add the ATC check, `UI5_BASE_APP_VERS` to it. For more information, see [Working with ATC Checks](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/438842e71bfa4ff09443562f5ce2282d.html).

To identify any adaptation project where the base app has a higher version than the version used in the adaptation project, run this check for your packages.

> ### Note:  
> SAP will only provide fixes for the latest version of the base application. Therefore, it is necessary to upgrade adaptation projects whenever the base application is updated. To avoid any conflicts, follow the [Upgrade Safe Compatibility Rules](upgrade-safe-compatibility-rules-53706e2.md).

To check if an adaptation project needs to be updated, you can use the *ABAP Test Cockpit* in the *ABAP Development Tools*. For more information, see [ATC Quality Checking](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/4ec1a1126e391014adc9fffe4e204223.html) and [Checking Quality of ABAP Code with ATC](https://help.sap.com/docs/SAP_S4HANA_CLOUD/25cf71e63940453397a32dc2b7676947/4ec5711c6e391014adc9fffe4e204223.html).



<a name="loioc6ef105f081648a090b288cd536e11b9__section_afx_1bw_hzb"/>

## Errors, Warnings, and How to Fix Them

This ATC check may identify the following errors and warnings:


<table>
<tr>
<th valign="top">

Error / Warning

</th>
<th valign="top">

How to Fix

</th>
</tr>
<tr>
<td valign="top">

For the used base app *<base app ID\>* a new version is available, please update

</td>
<td valign="top">

To find out what changed in a base app provided by SAP S/4HANA Cloud, check the [What's New in SAP S/4HANA Cloud](https://help.sap.com/whats-new/7d3d11840a6543329e72391cf4d48e2d).

> ### Tip:  
> In the What's New Viewer, you can filter the *Category* column for *App* and search the *Technical Objects Name* column for the SAP Fiori app ID of the base app. For example, `F3331`.

To update the adaptation project, proceed as follows:

1.  In SAP Business Application Studio, open *Visual Editor* and test that everything is still working with the new base version.

    *Visual Editor* automatically fetches the latest version of the base app.

2.  Once everything is tested, re-deploy your application.

    You may also need to refresh your IAM app.




</td>
</tr>
<tr>
<td valign="top">

The base app *<base app ID\>* was deleted, please check the successor app

</td>
<td valign="top">

If you do not re-deploy your adaptation project, this will not affect anything. We recommend that you create a new adaptation project based on the successor app.

</td>
</tr>
</table>

