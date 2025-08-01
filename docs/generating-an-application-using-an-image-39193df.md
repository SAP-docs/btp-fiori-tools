<!-- loio39193dfef3654ded850d39e7008e77d3 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Generating an Application Using an Image

Learn how to generate an application with the Project Accelerator using SAP Fiori tools AI and an image.

To generate an application using an image, the image must be uploaded to your workspace folder in SAP Business Application Studio. The image must represent the application model or the UI of a single list report or object page. To use multiple images, proceed with the following: [Generating an Application Using Text and Images](generating-an-application-using-text-and-images-5dd43dc.md).



<a name="loio39193dfef3654ded850d39e7008e77d3__section_dbw_jbt_51c"/>

## Procedure

1.  Prepare the image you will use as your business requirement. For the best results, label your image using English and follow the provided example: [Example: Manage Travel List Report Page](example-manage-travel-list-report-page-480d33c.md).
2.  Upload the image to your workspace folder in SAP Business Application Studio.

3.  Launch the Project Accelerator using SAP Fiori tools AI through one of the following options:

    1.  Command Palette

        Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the `Fiori tools AI: Launch the Project Accelerator` command.

    2.  SAP Fiori

        Click the <span class="SAP-icons-TNT-V3"></span> \(*SAP Fiori*\) icon on the activity bar.


    > ### Note:  
    > Once you’ve opened the Project Accelerator in SAP Fiori tools AI, your query must be related to generating an SAP Fiori elements application. You cannot make general requests to the AI assistant.

4.  Under *Project Accelerator*, click *Choose File \(.docx, .md, .txt, .jpg\)* and choose your image.

    > ### Note:  
    > The Project Accelerator cannot generate a second application for the same project, so ensure your request only refers to a single application.

5.  Provide the *Project Folder Path* that you want to generate the project into.
6.  Click *Generate*.

    Depending on your business requirement, generation may take some time.

    You can stop the generation if you want to cancel the process and make further changes. To stop the generation, click the :white_large_square: \(*Stop*\) icon. Then, click *Yes* at the *Are you sure you want to stop generation?* prompt. The process is stopped. You can then edit your business requirement and generate a new application.

7.  The generated project is added to your filesystem at the project folder path you chose. Then, *Application Information* is launched for the associated SAP Fiori application. You can then make further changes using SAP Fiori tools.


