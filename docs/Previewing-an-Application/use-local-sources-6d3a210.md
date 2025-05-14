<!-- loio6d3a21087ba74ce1a5ba475d9ef4fbd4 -->

# Use Local Sources

Start the application using the `npm run start-local` command. Then, the application runs on `localhost:8080` and uses a mock server to reflect the OData endpoint. A local copy of the SAPUI5 library is downloaded from `npmjs`, if necessary. You can modify the version by updating the `ui5-local.yaml` file in the project folder. This way, you can use the application without connection to a back end.



<a name="loio6d3a21087ba74ce1a5ba475d9ef4fbd4__section_r5s_m5t_r4b"/>

## Visual Studio Code

1.  In VS Code, open the terminal.

    > ### Note:  
    > To open the terminal VS Code:
    > 
    > -   Use the [CTRL\] + [\`\]  keyboard shortcut with the backtick character.
    > -   Use the *View* \> *Terminal* menu command.
    > -   From the *Command Palette* \([CMD/CTRL\] + [Shift\] + [P\] \), execute the `View: Toggle Integrate Terminal` command.

2.  Ensure you are in the root directory of your project.
3.  In the terminal pane, type `npm run start-local` and press *Enter*.

    The preview of your application starts automatically.

    > ### Note:  
    > The automatic download is only supported with SAPUI5 versions 1.76 and higher.




<a name="loio6d3a21087ba74ce1a5ba475d9ef4fbd4__section_jf3_55t_r4b"/>

## SAP Business Application Studio

1.  In SAP Business Application Studio, open the terminal.

    > ### Note:  
    > To open the terminal in SAP Business Application Studio:
    > 
    > -   Select *Terminal* \> *New Terminal* from the menu bar.

2.  Ensure you are in the root directory of your project.
3.  In the terminal pane, type `npm start-local` and press *Enter*.

    The preview of your application starts automatically.

    > ### Note:  
    > The automatic download is only supported with SAPUI5 versions 1.76 and higher.


