<!-- loio5dd43dc5dcab4c36b8a654ce20bac71e -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Generating an Application Using Text and Images

Learn how to generate an application with the Project Accelerator using SAP Fiori tools AI and a combination of text and images.

To generate an application using a combination of text and images, or using multiple images, you must either create a Microsoft Word document \(.docx\) file or create a markdown \(`.md`\) file that references the images you want to use. If you are using a markdown file, the images must be uploaded to your workspace folder in SAP Business Application Studio.

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

        Click the *SAP Fiori* \(wrench and pencil\) icon on the activity bar.


    > ### Note:  
    > Once you’ve opened the Project Accelerator in SAP Fiori tools AI, your query must be related to generating an SAP Fiori elements application. You cannot make general requests to the AI assistant.

4.  Under *Project Accelerator*, click *Choose File \(.docx, .md, .txt, .jpg\)* and choose your file.

    > ### Note:  
    > The Project Accelerator cannot generate a second application for the same project, so ensure your request only refers to a single application.

5.  Click *Generate*.

    Depending on your business requirements, generation may take some time.

    You can stop generation if you want to cancel the process and make further changes. To stop generation, click the :white_large_square: \(*Stop*\) icon. Then, click *Yes* at the *Are you sure you want to stop generation?* prompt. The process is stopped and the staging files are discarded. You can then edit your business requirements and generate a new application.

6.  Review the generated application to see if it meets your requirements. To choose a new markdown file, click the :wastebasket: \(*Delete*\) icon, choose another file, and click *Regenerate* to re-run generation.
    -   To start again, click the <span class="SAP-icons-TNT-V3"></span> *\(Clear\)* icon. This will clear your markdown file and the staging area to enable you to start from scratch.
    -   Click *Preview* to launch a preview of the application in a new browser window.

    -   Examine the generated files in the *Staging Area*.

7.  To accept the generated application, click *Accept Project* to move the project to your filesystem. You can then make further changes using SAP Fiori tools.


