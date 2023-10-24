<!-- loioc06b9cbb3f3641aabfe3a5d199e855a0 -->

# Generate Deployment Configuration ABAP



<a name="loioc06b9cbb3f3641aabfe3a5d199e855a0__section_lmt_bq3_k4b"/>

## ABAP Pre-Requisites

The deployment to ABAP task allows deploying SAP Fiori applications to SAP systems using the [SAPUI5 Repository OData service](https://sapui5.hana.ondemand.com/#/topic/a883327a82ef4cc792f3c1e7b7a48de8.html).



### Prerequisites:

-   SAP component SAP\_UI 7.53 or higher is installed in your SAP system

    > ### Note:  
    > For systems below 7.53, the alternative is to [upload](https://help.sap.com/viewer/0ce0b8c56fa74dd897fffda8407e8272/7.5.17/en-US/a560bd6ed4654fd1b338df065d331872.html) the application.

-   Service needs to be enabled and accessible from your development environment \([activate and maintain services](https://help.sap.com/viewer/68bf513362174d54b58cddec28794093/7.52.5/en-US/bb2bfe50645c741ae10000000a423f68.html)\)
-   For operations on a SAPUI5 ABAP repository, you need the S\_DEVELOP authorization



### Limitations

-   The task doesn’t create ABAP transports, therefore, it requires an existing transport if the target ABAP package requires a transport
-   Basic Authentication \(user/password based authentication\) is supported for all back-end systems. Additional support for OAuth2 authentication is provided for ABAP systems on SAP Business Technology Platform.



<a name="loioc06b9cbb3f3641aabfe3a5d199e855a0__section_nv5_bxx_3nb"/>

## Generation of Deployment Configurations

In order to create deployment configuration, launch the deployment configuration wizard from the command palette entry `Fiori: Add Deployment Configuration` and chose the **Fiori** project you would like to configure, or you can launch from the command line using the command `npx fiori add deploy-config` while in the required **Fiori** project folder.

You're prompted for required information and then the `ui5-deploy.yaml` file is created based on your input and the content of the existing `ui5.yaml` file used for preview. In addition to creating the configuration, the create deployment command will also update your `package.json` so that you can execute `npm run deploy` - afterwards to deploy your application. See [Deployment of Application](deployment-of-application-607014e.md).

When prompted, add or choose:


<table>
<tr>
<td valign="top">

Please choose the target



</td>
<td valign="top">

ABAP



</td>
</tr>
<tr>
<td valign="top">

Select Target System



</td>
<td valign="top">

Choose a system from your SAP saved systems or provide a Target system URL\(VS Code only\).



</td>
</tr>
<tr>
<td valign="top">

Destination



</td>
<td valign="top">

Choose the deployment destination from list provided \(SAP Business Application Studio only\).



</td>
</tr>
<tr>
<td valign="top">

Enter client



</td>
<td valign="top">

Add a new client or leave **default**.



</td>
</tr>
<tr>
<td valign="top">

SAPUI5 ABAP Repository



</td>
<td valign="top">

Add a name for the deployed application.



</td>
</tr>
<tr>
<td valign="top">

Deployment Description



</td>
<td valign="top">

Add the optional description for the deployed application.



</td>
</tr>
<tr>
<td valign="top">

Package



</td>
<td valign="top">

Add a valid package name.



</td>
</tr>
<tr>
<td valign="top">

How do you want to enter Transport Request



</td>
<td valign="top">

-   **Enter manually:** Manually provide the transport request.
-   **Choose from existing:** The applicable list of transport requests and their description is retrieved from the target system and displayed in a list for you to choose from. If the list of transport requests is unable to be retrieved from the target system, a user must provide the entry manually.
-   **Create new:** A new transport request is automatically created for use. If the transport request is unable to be created from the target system, user must provide the entry manually.
-   **Create during deployment:** The transport request is automatically created the first time the application is deployed. If the transport request is unable to be created from the target system, deployment fails.




</td>
</tr>
<tr>
<td valign="top">

Transport Request



</td>
<td valign="top">

When prompted, either choose a transport request from the list or add a valid transport request.



</td>
</tr>
</table>



<a name="loioc06b9cbb3f3641aabfe3a5d199e855a0__section_a5d_mfd_l4b"/>

## Example Configuration - ABAP

Executing `ui5 build --config ui5-deploy.yaml` in your project with the configuration below in a `ui5-deploy.yaml` manually added to the project, would deploy all files of your `dist` folder except files ending with `.test.js` and the `internal.md` file. The target system is `XYZ` with client 200. Username and password for authentication is read from the environment variables `XYZ_USER` and `XYZ_PASSWORD`.

Based on this example, the application is created/updated as `/TEST/SAMPLE_APP` in package `/TEST/UPLOAD` and all changes is recorded in transport request `XYZQ300582`.

Sample **content of `ui5-deploy.yaml`**

> ### Sample Code:  
> ```
> builder:
>   customTasks:
>   - name: deploy-to-abap
>     afterTask: replaceVersion
>     configuration:
>       target:
>         url: https://XYZ.sap-system.corp:44311
>         client: 200
>         auth: basic
>       credentials:
>         username: env:XYZ_USER
>         password: env:XYZ_PASSWORD
>       app:
>         name: /TEST/SAMPLE_APP
>         package: /TEST/UPLOAD
>         transport: XYZQ300582
>       exclude:
>       - .*\.test.js
>       - internal.md
> ```



<a name="loioc06b9cbb3f3641aabfe3a5d199e855a0__section_qdj_kr4_fvb"/>

## Example Configuration - Additional Params

For example, you can add additional settings params such as `sap-language` to your yaml file.

Sample **content of `ui5-deploy.yaml`**

> ### Sample Code:  
> ```
> builder:
>   customTasks:
>   - name: deploy-to-abap
>     afterTask: replaceVersion
>     configuration:
>       target:
>         url: https://XYZ.sap-system.corp:44311
>         client: 200
>         auth: basic
>         params: 
>           sap-language: en
>       credentials:
>         username: env:XYZ_USER
>         password: env:XYZ_PASSWORD
>       app:
>         name: /TEST/SAMPLE_APP
>         package: /TEST/UPLOAD
>         transport: XYZQ300582
>       exclude:
>       - .*\.test.js
>       - internal.md
> ```

