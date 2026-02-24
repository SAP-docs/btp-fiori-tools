<!-- loioe7f9f8c26ebb4ab181372d09bb054cac -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Generating an Application Using Text

Learn how to generate an application with the Project Accelerator using SAP Fiori tools AI and text.



<a name="loioe7f9f8c26ebb4ab181372d09bb054cac__section_dbw_jbt_51c"/>

## Procedure

1.  Launch the Project Accelerator using SAP Fiori tools AI through one of the following options:

    1.  Command Palette

        Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori tools AI: Launch the Project Accelerator` command.

    2.  SAP Fiori

        Click the <span class="SAP-icons-TNT-V3"></span> \(*SAP Fiori*\) icon on the activity bar.

    3.  Joule

        Click the <span class="SAP-icons-TNT-V3"></span> \(*Joule*\) icon on the activity bar.


    > ### Note:  
    > Once you’ve opened the Project Accelerator in SAP Fiori tools AI, your query must be related to generating an SAP Fiori elements application. You cannot make general requests to the AI assistant.

2.  Depending on the programming model, choose either the *CAP Accelerator* or *RAP Accelerator* tab.

    For *RAP Accelerator*, provide the following information:


    <table>
    <tr>
    <td valign="top">
    
    *Destination\** 
    
    </td>
    <td valign="top">
    
    Select a destination system from the dropdown.

    Basic authentication \(user and password-based authentication\) is supported for all back-end systems.

    Additionally, you can configure OAuth2 authentication for a destination on SAP Business Technology Platform cockpit.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *SAPUI5 ABAP Repository\** 
    
    </td>
    <td valign="top">
    
    Enter the name for the deployed application.

    Note: The name must follow the rules of creating a Business Server Page Application \(BSP\) application. It must not exceed 15 characters and must consist of alphanumeric characters or underscores only. The name must be unique in the BSP repository and its namespace must be compatible with the selected package.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Select How You Want to Enter the Package\** 
    
    </td>
    <td valign="top">
    
    -   *Enter Manually:* Manually provide the package name.


    -   *Choose from Existing*: Select a package from the dropdown.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Package\**
    
    </td>
    <td valign="top">
    
    Select a package from the dropdown or enter a valid package name.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Select How You Want to Enter the Transport Request\**
    
    </td>
    <td valign="top">
    
    -   *Enter Manually*: Manually provide the transport request.


    -   *Choose from Existing*: Select a transport request from the dropdown. If the list of transport requests cannot be retrieved, you must enter the transport request manually.



    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *ABAP Artifact Prefix* \(Optional\)
    
    </td>
    <td valign="top">
    
    Enter three alphanumeric characters.

    For example, if you enter the *TRV* prefix, then the generated ABAP artifact name is <package\_namespace\> *TRV* MANAGE\_TRAVEL.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *ABAP Artifact Suffix* \(Optional\)
    
    </td>
    <td valign="top">
    
    Enter three alphanumeric characters.

    For example, if you enter the *TRV* suffix, then the generated ABAP artifact name is <package\_namespace\> MANAGE\_TRAVEL *TRV*.
    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > If the package is local, a transport request is not required.
    > 
    > This feature does not create ABAP transport requests. If the target ABAP package requires a transport, you must provide an existing transport request.

3.  Depending on the method you used to launch SAP Fiori tools AI, enter your business requirements as follows:

    -   Text input:
        -   Command Palette and SAP Fiori: Under *Project Accelerator*, enter your business requirements in the *Business Requirements* textbox.
        -   Joule: Enter `/fiori-gen-spec-app #(path to your docx, markdown, or text file)` and click the *Send* icon.

    -   File input:
        -   Upload the file to your workspace folder in SAP Business Application Studio.
        -   Command Palette and SAP Fiori: Under *Project Accelerator*, click *Choose File \(docx, .md, .txt, .jpg\)* and choose your markdown, text, or docx file.
        -   Joule: Enter the `/fiori-gen-spec-app` command followed by your business requirements and click the *Send* icon.


    For the best results, use English and follow the provided examples:

    -   [Example 1: Manage Contracts and Customer Information in the System](example-1-manage-contracts-and-customer-information-in-the-system-c1bccf2.md)

    -   [Example 2: Display Customers with Related Contracts](example-2-display-customers-with-related-contracts-a6c978f.md)

    > ### Note:  
    > The Project Accelerator cannot generate a second application for the same project, so ensure your request only refers to a single application.

4.  By default, the application is generated into the open folder. Provide a *Project Folder Path* if you want to generate the project into another folder.
5.  Click *Generate*.

    > ### Note:  
    > If you launch SAP Fiori tools AI using Joule, you are transferred to the Project Accelerator to generate your application.

    Depending on your business requirements, generation may take some time.

    You can stop the generation if you want to cancel the process and make further changes. To stop the generation, click the :white_large_square: \(*Stop*\) icon. Then, click *Yes* at the *Are you sure you want to stop generation?* prompt. The process is stopped. You can then edit your business requirements and generate a new application.

6.  The generated project is added to your filesystem at the project folder path you chose. Then, *Application Information* is launched for the associated SAP Fiori application. You can then make further changes using SAP Fiori tools.


> ### Note:  
> **RAP**
> 
> -   If any back-end artifacts have already been generated, they are not removed.
> 
> -   You can preview applications with mock data generated using AI with the `start-mock` script.

