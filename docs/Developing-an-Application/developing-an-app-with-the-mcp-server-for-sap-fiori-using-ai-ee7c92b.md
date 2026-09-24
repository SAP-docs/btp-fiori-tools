<!-- loioee7c92b4373b4011a39f654db4505513 -->

# Developing an App with the MCP Server for SAP Fiori Using AI

You can use the Model Context Protocol \(MCP\) server for SAP Fiori to generate and modify SAP Fiori elements applications using natural language.

Included in Application Modeler, it empowers GitHub Copilot to perform the following actions based on your prompt:

-   Search across the SAPUI5, SAP Fiori elements, SAP Fiori tools, and OPA5 documentation to answer your queries
-   Generate SAP Fiori elements applications for CAP and RAP projects
-   Discover existing SAP Fiori applications and SAP systems to modify and use
-   Modify SAP Fiori applications with the following changes:
    -   Add and delete pages
    -   Add and modify controller extensions
    -   Modify manifest properties

-   Download and save EDMX metadata from an SAP system

For more information about prompts, see [@sap-ux/fiori-mcp-server](https://www.npmjs.com/package/@sap-ux/fiori-mcp-server).



## Using the MCP Server for SAP Fiori

To use the MCP Server for SAP Fiori in Visual Studio Code, open the *Chat* view. For more information, see [Use Chat in VS Code](https://code.visualstudio.com/docs/chat/chat-overview).

To use the MCP Server for SAP Fiori in SAP Business Application Studio, open the chat menu and select *Open Chat*. For more information, see [AI Chat](https://help.sap.com/docs/bas/sap-business-application-studio/ai-chat?version=Cloud).

For more information about how to use this MCP server outside of these IDEs or with other AI coding assistants, see [@sap-ux/fiori-mcp-server - Setup](https://www.npmjs.com/package/@sap-ux/fiori-mcp-server#setup).



## Setting a Specific Version and Disabling the MCP Server for SAP Fiori

You can set a specific version ahead of the automatic update and disable the MCP server in the settings of your IDE. To do so, proceed as follows:

-   Open the Command Palette using [CTRL\]/[CMD\][Shift\] + [P\]  and execute *Preferences: Open User Settings*.
-   Search for `MCP for SAP`.
-   Set a specific version number in *Sap* \> *Ux* \> *Fiori Tools* \> *Mcp Server: Version*.
-   Disable the *Sap* \> *Ux* \> *Fiori Tools* \> *Mcp Server: Enable*.

