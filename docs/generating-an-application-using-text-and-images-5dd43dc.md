<!-- loio5dd43dc5dcab4c36b8a654ce20bac71e -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Generating an Application Using Text and Images

Learn how to generate an application with the Project Accelerator using SAP Fiori tools AI and a combination of text and images.

To generate an application using a combination of text and images, or using multiple images, you must either create a Microsoft Word document \(`.docx`\) file or create a markdown \(`.md`\) file that references the images you want to use. If you are using a markdown file, the images must be uploaded to your workspace folder in SAP Business Application Studio.

> ### Tip:  
> -   Each image must represent a single list report or object page and be accompanied by text explaining the relation between the pages.
> 
> -   The text can also provide some additional information that is not adequately described from the image, such as code list values.
> -   If the page contains multiple views that are not visible, such as different tabs or sections, the user input should have multiple images depicting the same page in these different states, along with an explanatory text.
> 
>     For example, if an object page contains multiple sections and their content is not visible in a single image, the text should list all of the sections and describe which section corresponds to which image.
> 
> -   If you are using a Microsoft Word document \(.docx\) file, ensure it only contains text and images. Do not add advanced formatting such as headers, footers, and tables.



<a name="loio5dd43dc5dcab4c36b8a654ce20bac71e__section_dbw_jbt_51c"/>

## Procedure

1.  Prepare the file you will use as your business requirements. For the best results, label your images using English and follow the provided example: [Example: Manage Travel App List Report Object Page](example-manage-travel-app-list-report-object-page-d17b256.md).
2.  Upload the file to your workspace folder in SAP Business Application Studio.

3.  Launch the Project Accelerator using SAP Fiori tools AI through one of the following options:

    1.  Command Palette

        Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori tools AI: Launch the Project Accelerator` command.

    2.  SAP Fiori

        Click the <span class="SAP-icons-TNT-V3"></span> \(*SAP Fiori*\) icon on the activity bar.


    > ### Note:  
    > Once you’ve opened the Project Accelerator in SAP Fiori tools AI, your query must be related to generating an SAP Fiori elements application. You cannot make general requests to the AI assistant.

4.  Depending on the programming model, choose either the *CAP Accelerator* or *RAP Accelerator* tab.

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

5.  Under *Project Accelerator*, click *Choose File \(.docx, .md, .txt, .jpg\)* and choose your file.

    > ### Note:  
    > The Project Accelerator cannot generate a second application for the same project, so ensure your request only refers to a single application.

6.  By default, the application is generated into the open folder. Provide a *Project Folder Path* if you want to generate the project into another folder.
7.  Click *Generate*.

    Depending on your business requirements, generation may take some time.

    You can stop the generation if you want to cancel the process and make further changes. To stop the generation, click the :white_large_square: \(*Stop*\) icon. Then, click *Yes* at the *Are you sure you want to stop generation?* prompt. The process is stopped. You can then edit your business requirements and generate a new application.

8.  The generated project is added to your filesystem at the project folder path you chose. Then, *Application Information* is launched for the associated SAP Fiori application. You can then make further changes using SAP Fiori tools.


> ### Note:  
> **RAP**
> 
> -   If any back-end artifacts have already been generated, they are not removed.
> 
> -   You can preview applications with mock data generated using AI with the `start-mock` script.

