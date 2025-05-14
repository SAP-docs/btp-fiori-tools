<!-- loiobda83a4c13414ded887d4255bf95f536 -->

# Use Mock Data



<a name="loiobda83a4c13414ded887d4255bf95f536__section_ymv_ph5_t4b"/>

## Using Mock Data in VS Code

> ### Note:  
> You need to install Mockserver before using `npm run start-mock`. For more information, see [Installing MockServer](installing-mockserver-2538055.md).

Start the application using `npm run start-mock`. The application runs on `localhost:8080` but uses a mock server to reflect the OData endpoint. This way, you can use the application without having to connect to a live OData service and generate mock data on the fly. If you want to generate `.json` files for your mock data, see: [Data Editor](../Project-Functions/data-editor-18e43b5.md). The preview of the application opens automatically in a new browser tab.

1.  In Visual Studio Code \(VS Code\), open the terminal.

    > ### Note:  
    > To open the terminal in VS Code,you can:
    > 
    > -   Use the [CTRL\] + [\`\]  keyboard shortcut with the backtick character.
    > -   Select *View* \> *Terminal* in the menu.
    > -   Execute the `View: Toggle Integrate Terminal` command from the *Command Palette* \([CMD/CTRL\] + [Shift\] + [P\] \) .

2.  Ensure you are in the root directory of your project.
3.  In the terminal pane, type `npm run start-mock` and press *Enter*.

    > ### Note:  
    > If port 8080 is already in use, the system chooses the next available port to start the application on.




<a name="loiobda83a4c13414ded887d4255bf95f536__section_s5v_th5_t4b"/>

## SAP Business Application Studio

> ### Note:  
> You need to install Mockserver before using `npm run start-mock`. For more information, see [Installing MockServer](installing-mockserver-2538055.md).

Start the application using `npm run start-mock`. The application runs on `localhost:8080` but uses a mock server to reflect the OData endpoint. This way, you can use the application without having to connect to a live OData service.

1.  In SAP Business Application Studio, open the terminal.

    > ### Note:  
    > To open the terminal in SAP Business Application Studio, you can:
    > 
    > -   Select *Terminal* \> *New Terminal* from the menu.

2.  Ensure that you are in the root directory of your project.
3.  In the terminal pane, type `npm run start-mock` and press *Enter*.

