<!-- loioe7f9f8c26ebb4ab181372d09bb054cac -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Generating an Application Using Text

Learn how to generate an application with the Project Accelerator using SAP Fiori tools AI and text.



<a name="loioe7f9f8c26ebb4ab181372d09bb054cac__section_dbw_jbt_51c"/>

## Procedure

1.  Launch the Project Accelerator using SAP Fiori tools AI through one of the following options:

    1.  Command Palette

        Open the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and execute the *Fiori tools AI: Launch the Project Accelerator* command.

    2.  SAP Fiori

        Click the *SAP Fiori* \(wrench and pencil\) icon on the activity bar.

    3.  Joule

        Click the <span class="SAP-icons-TNT-V3"></span> \(*Joule*\) icon on the activity bar.


    > ### Note:  
    > Once you’ve opened the Project Accelerator in SAP Fiori tools AI, your query must be related to generating an SAP Fiori elements application. You cannot make general requests to the AI assistant.

2.  Depending on the method you used to launch SAP Fiori tools AI, enter your business requirements as follows:

    -   Text input:
        -   Command Palette and SAP Fiori: Under *Project Accelerator*, enter your business requirements in the *Application requirements* textbox.
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

3.  Click *Generate*.

    > ### Note:  
    > If you launch SAP Fiori tools AI using Joule, you are transferred to the Project Accelerator to generate your application.

    Depending on your business requirements, generation may take some time.

    You can stop generation if you want to cancel the process and make further changes. To stop generation, click the :white_large_square: \(*Stop*\) icon. Then, click *Yes* at the *Are you sure you want to stop generation?* prompt. The process is stopped and the staging files are discarded. You can then edit your business requirements and generate a new application.

4.  Review the generated application to see if it meets your requirements. You can edit your business requirements as needed and click *Regenerate* to re-run generation.
    -   To start again, click the <span class="SAP-icons-TNT-V3"></span> *\(Clear\)* icon. This will clear your business requirements and the staging area to enable you to start from scratch.
    -   Click *Preview* to launch a preview of the application in a new browser window.

    -   Examine the generated files in the *Staging Area*.

5.  To accept the generated application, click *Accept Project* to move the project to your filesystem. You can then make further changes using SAP Fiori tools.


