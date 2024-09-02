<!-- loio6f3c737aa18c4181b1f0a343755f335e -->

# Project Validation

When the project is generated, you can validate it by executing `Fiori: Validate Project`. Use a quick pick selection to select a project for validation from the multiple projects in the workspace.

The validation comprises of the following steps:

-   **project**

    The project step checks that files such as `package.json`, `manifest.json`, and `ui5.yaml` exist and their mandatory fields are filled.

-   **annotation**

    The annotation step validates the project annotation files using the same modules as the XML annotation language server extension.

-   **specification**

    Tthe specification step validates `manifest.json` and files in the changes folder. The`@sap/ux-specification`module is used to **import** the project and provide invalid configuration error messages.

-   **eslint**

    The eslint step checks if `eslint` is installed as a dependency. If it is, the project validation runs the `eslint` check based on the project's configuration and the rules defines in the <code><a href="https://www.npmjs.com/package/eslint-plugin-fiori-custom">eslint-plugin-fiori-custom</a></code>. You can enable `eslint` support for a new project by selecting the appropriate options in the *Advanced Options* of the SAP Fiori application generator, as described in the [Additional Configuration](../Generating-an-Application/Additional-Configuration/additional-configuration-9bea64e.md) section.


After all validation steps are executed, a report is generated and displayed as a Markdown \(`.md`\) file and in the *Problems* tab of Visual Studio Code \(VS Code\) or SAP Business Application Studio.

