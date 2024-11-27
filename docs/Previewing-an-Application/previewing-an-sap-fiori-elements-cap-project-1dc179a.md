<!-- loio1dc179a7f74d48c7816e90b867058887 -->

# Previewing an SAP Fiori Elements CAP Project

Once your CAP project is generated, you can preview it in Visual Studio Code or SAP Business Application Studio.



<a name="loio1dc179a7f74d48c7816e90b867058887__section_abn_fyb_s4b"/>

## Visual Studio Code

To run an application preview in VS Code, perform the following steps:

1.  In VS Code, open the terminal.

    > ### Note:  
    > To open the terminal in VS Code:
    > 
    > -   Use the [Ctrl+\`\] keyboard shortcut with the backtick character.
    > -   Use the *View* \> *Terminal* menu command.
    > -   From the *Command Palette* \([CMD/CTRL\] + [Shift\] + [P\] \), execute the *View: Toggle Integrate Terminal* command.

2.  Ensure you are in the root directory of your project.
3.  In the terminal, type `cds run` and press *Enter*.

    A new line appears, such as:

    ```
    server listening on { url: 'http://localhost:4004' }
    ```

    > ### Note:  
    > If an error occurs when executing `cds run`, enter the following commands:
    > 
    > ```
    > npm i -g @sap/cds
    > npm i -g @sap/cds-dk --force
    > ```

4.  Open the link in the terminal using the [Ctrl+Click\] combination.

    A new browser window with a list of links opens.

5.  Click the HTML link in the list, such as `/incidents/webapp/index.html`.

    Your application is displayed on the launchpad.

6.  Navigate back to VS Code and stop the server by executing `Ctrl-C` in the terminal window.



<a name="loio1dc179a7f74d48c7816e90b867058887__section_rpn_2bc_s4b"/>

## SAP Business Application Studio

To run an application preview in SAP Business Application Studio, perform the following steps:

1.  In SAP Business Application Studio, open the terminal.

    > ### Note:  
    > To open the terminal in SAP Business Application Studio:
    > 
    > -   Select *Terminal* \> *New Terminal* from the menu bar.

2.  Ensure you are in the root directory of your project.
3.  In the terminal, type `cds run` and press *Enter*.

    A new line appears, such as:

    ```
    server listening on { url: 'http://localhost:4004' }
    ```

    > ### Note:  
    > If an error occurs when executing `cds run`, enter the following commands:
    > 
    > ```
    > npm i -g @sap/cds
    > npm i -g @sap/cds-dk --force
    > ```

4.  Open the link in the terminal using the [Ctrl+Click\] combination.

    A new browser window with a list of links opens.

5.  Click the upper link in the list in HTML format, such as `/incidents/webapp/index.html`.

    Your application is displayed on the launchpad.

6.  Navigate back to SAP Business Application Studio and stop the server by executing `Ctrl-C` in the terminal window.

