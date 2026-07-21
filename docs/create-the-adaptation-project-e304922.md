<!-- loioe3049227a13f4c13a2cb5582e0dd67d7 -->

# Create the Adaptation Project

Create an adaptation project from existing OData v2/v4 SAP Fiori elements-based applications and freestyle SAPUI5 applications.

1.  If you aren't already logged in to your Cloud Foundry account:
    1.  Open console in Visual Studio Code \(VS Code\).
    2.  Type `cf login` and execute the command.
    3.  Follow the onscreen instructions until you are successfully logged in.
    4.  Close the console and continue with the procedure.

2.  To start the process of creation, select *Open Template Wizard* from the VS Code command palette, choose the *Adaptation Project* tile, and select *Next*.
3.  Use the Yeoman generator to configure the project information.
    1.  Select SAP BTP, Cloud Foundry for your Target Environment.
    2.  If you were logged into your Cloud Foundry account before launching the generator, you will be asked to proceed. If you are not logged into your Cloud Foundry account, you will be asked to provide its API Endpoint URL, your username, and password. You can find your API Endpoint URL in your CF Subaccount cockpit, in *Cloud Foundry Environment* section, under *API Endpoint*. Select the *Login* icon and select *Organization*. Then select the *Space* in which you will be working.
    3.  Select the root path of the MTA project where you want to place your new Adaptation Project module.
    4.  Enter a name for the project and a title for the application.

        The name should be unique for the application and subaccount that will be used.

    5.  Select the business service that you want to use and the application to use as a basis for the Adaptation Project.
    6.  Enter a business solution name.

4.  Load the Adaptation Editor.

    > ### Note:  
    > To launch the Adaptation Editor, at least the first time for each browser session, you might need to disable any existing popup blockers in your browser.

    Press [Ctrl\] + [Shift\] + [P\]  to open the command palette, search for *Open Adaptation Editor*, and select it. You can also open the Adaptation Editor by expanding the `webapp` folder, right-clicking the `manifest.appdescr_variant` file, and choosing *Open Adaptation Editor*.

    An information message appears the first time that you load the editor, asking to expose a port needed for the Adaptation Editor. Select *Yes*.


