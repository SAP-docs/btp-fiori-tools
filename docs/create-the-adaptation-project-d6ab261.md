<!-- loiod6ab2614df5c4c5597055e4dd988ad16 -->

# Create the Adaptation Project

Create an adaptation project from existing SAP Fiori elements or freestyle SAPUI5 applications in SAP S/4HANA Cloud Public Edition.



<a name="loiod6ab2614df5c4c5597055e4dd988ad16__steps_b11_dpw_5pb"/>

## Procedure

1.  Open Visual Studio Code \(VS Code\) and start and open the dev space that you want to use. The dev space must have *SAPUI5 Adaptation Project* as a predefined extension or it has been chosen manually as an extension for the dev space during creation.

2.  Choose *File* \> *Open Folder...*. Select the *projects* folder and click *OK*.

3.  To start the Yeoman generator, choose *View* \> *Command Palette*. In the Command Palette, enter `Open Template Wizard` and select the wizard from the list. After the generator loads, click the *Adaptation Project* tile and select *Start*.

4.  Use the wizard to configure the project information.

    1.  In the *Select Environment* step, select ABAP for your *Target Environment*.

    2.  Enter a name for the project and a title for the application. The project name has to be unique in the system.

    3.  The *Namespace* field always starts with `customer.`. Enter the name of your project after `customer.`. Click *Next*.

    4.  Select a system.

    5.  \(Optional\) If required, enter your username and password for the system and select *Login* from inside the password field. Basic authentication is supported.

    6.  The system type will be automatically detected, being *CloudReady*.

    7.  Choose the application that you want to work with. Only applications extensible in adaptation projects will be shown in the list.

    8.  Choose *Finish* and wait until your project gets generated. You will be notified when the project is generated.


5.  A notification message appears that the project has been generated and will be saved for future use.

6.  You can now preview the adaptation project. For more information, see [Preview the Adaptation Project](preview-the-adaptation-project-64cc15b.md). You can also continue developing. For more information, see [Make Adaptations](make-adaptations-6d2cfea.md).


