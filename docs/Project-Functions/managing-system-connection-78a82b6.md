<!-- loio78a82b6852ce4061ba0825afdb79cda6 -->

# Managing System Connection

SAP Fiori tools running in VS Code enables to save the connection information to a remote system. This functionality provides faster authentication while creating an application, generating deployment configuration, and deploying an application. The credentials are saved in the operating system secured storage, such as Credential Manager in Windows and Keychain in Mac.



<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_jv1_xgh_3qb"/>

## View Saved Systems Details

To view the saved systems details, perform the following steps:

1.  On the activity toolbar from the left side, click *SAP Fiori* \(![Wrench/Pencil icon](images/SAP_Fiori_tools_Wrench_Pencil_9d6b0f8.png)\).
2.  Expand the *SAP Systems* view.

    You can see the list of saved systems along with the usernames used for authentication.

3.  To see the stored system details in a new view, click a specific system entry or right-click and select *Show SAP System Details*.

> ### Note:  
> You can create an SAP Fiori application with your selected SAP system by clicking on the *Create SAP Fiori application* link. This will open the SAP Fiori application generator and pre-select your SAP system as the data source.



<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_mrq_tbr_2rb"/>

## Test Saved Systems Connection

To view the saved systems details, perform the following steps:

1.  Open the details of a saved system. For more information, see [View Saved Systems Details](managing-system-connection-78a82b6.md#loio78a82b6852ce4061ba0825afdb79cda6__section_jv1_xgh_3qb).
2.  Click *Test Connection*.

    As a result, you’ll see if the system connection was successful and whether it supports OData V2 and/or OData V4 services.


> ### Note:  
> We recommend that you test a saved system connection to ensure the service catalog of a selected system works as expected.



<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_v2b_wpy_lqb"/>

## Edit Saved Systems

For editing an existing SAP system connection detail, perform the following steps:

1.  Right-click a saved system name and click the *Show SAP System Details* button or click a saved system name to open system details tab to open *SAP system Details*.
2.  For *ABAP On Premise*, update any of the following fields:
    -   System Name
    -   URL
    -   Client
    -   Username
    -   Password

3.  For *ABAP Environment on SAP Business Technology Platform*, update the following fields:

    -   System Name: editable
    -   Authentication Type: non-editable

4.  For authentication type *Service Key*, update the following fields:

    -   URL: non-editable \(determined\)

    -   Client: non-editable \(determined\)

    -   Service Key: editable


5.  For authentication type *Reentrance Ticket*, update the following fields:

    -   URL: editable


6.  Click on *Test Connection*.

    > ### Note:  
    > We recommend that you test the connection before saving to ensure it’s working as expected.

7.  Click *Save*.



<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_hr1_zhh_3qb"/>

## Delete Saved Systems

To delete the saved systems, perform the following steps:

1.  On the activity toolbar from the left side, click *SAP Fiori* \(![Wrench/Pencil icon](images/SAP_Fiori_tools_Wrench_Pencil_9d6b0f8.png)\).
2.  Expand the *SAP Systems* view.
3.  Select any saved system.
4.  Click the delete icon ![](images/Delete_icon_VS_Code_86e90a9.png) next to the system name.
5.  Click *Yes* in the confirmation dialogue box.



<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_cn1_1lh_3qb"/>

## Create New System

To create a new ABAP On Premise system, perform the following steps:

1.  Click the [\+\] icon with the tooltip *Add SAP System* on the right side of the system panel.
2.  Enter valid values for ABAP On Premise system that you have access to:
    -   *System Name*: your choice
    -   *URL*: system URL
    -   *Client*: usually 3 digits, leave empty if not required
    -   *Username*: your username
    -   *Password*: your password

3.  Click*Test Connection* and verify that the following message is shown: **This SAP system connected successfully**.
4.  Click *Save* and verify the following:

    -   that the message *System information saved* is displayed

    -   that the saved system is shown in the systems panel in the format **<name of added system\> \[username\]**



> ### Note:  
> You can save the new system without first validating that the connection is successful. However, we recommend that you test the connection before saving to ensure it works as expected.

To create a new ABAP Environment on SAP BTP, perform the following steps:

1.  Click the [\+\] icon with the tooltip *Add SAP System* on the right side of the system panel.

2.  Under *System Type*, select *ABAP Environment on SAP Business Technology Platform*.

3.  Under *Authentication Type*, select either *Service Key* or *Reentrance Ticket*.

    **Service Key**

    1.  For authenticating with a Service Key, enter valid values for the ABAP Environment on SAP Business Technology Platform system that you have access to:

        -   *System Name*: your choice

        -   *Service Key*: copy and paste the service key of your chosen SAP BTP system


    2.  Click *Test Connection*.

        -   that the URL value has been filled in by the system

        -   that the message *This SAP system connected successfully* is displayed


    3.  Click *Save* and verify the following:

        -   that the message *System information saved* is displayed

        -   that the added system is shown under the systems panel in the format **<name of added system\> \(BTP\)**



    **Reentrance Ticket**

    > ### Note:  
    > Authenticating with reentrance tickets requires SAP S/4HANA Cloud 2408 or higher.

    1.  For authenticating with a Reentrance Ticket, enter the following valid values:

        -   *System Name*: your choice

        -   *URL*: the required ABAP system URL


    2.  Click *Test Connection*.

        As a result, you’ll see if the system connection was successful and whether it supports OData V2 and/or OData V4 services. If the connection fails, you'll be asked to check the Output Tab for more details.

    3.  After successful connection, click *Save* and verify the following:

        -   that the message *System information saved* is displayed

        -   that the added system is shown under the systems panel in the format **<name of added system\> \(S4HC\)**






<a name="loio78a82b6852ce4061ba0825afdb79cda6__section_jxl_rtf_c5b"/>

## Export/Import an Existing ABAP On Premise SAP System

To export an existing ABAP On Premise system, perform the following steps:

1.  Right-click a saved system name and click *Show SAP System Details* or click a saved system name to open the *SAP Systems* details.
2.  Click *Export System*. A copy of the saved system will be downloaded in JSON format. Please note that no sensitive credential information is included in the exported JSON file.

To import an ABAP On Premise system, perform the following steps:

1.  On the activity toolbar from the left side, click *SAP Fiori* \(![Wrench/Pencil icon](images/SAP_Fiori_tools_Wrench_Pencil_9d6b0f8.png)\) .
2.  Alongside the SAP Systems title bar, click *Import SAP System* \( ![](images/Fiori_tools_Saved_Systems_9dce22e.png)\).
3.  Navigate to the JSON file that you would like to import.
4.  Upon successful import, provide your credentials for that system and click *Test Connection*.
5.  Once the connection is successfully tested, click *Save* to finish importing the system.

> ### Note:  
> If you already have a saved local SAP system with the same name, you’ll be asked to confirm before overwriting.

> ### Note:  
> You can only import and export saved SAP systems between development environments that are using VS Code. You cannot import or export systems between VS Code and SAP Business Application Studio.

