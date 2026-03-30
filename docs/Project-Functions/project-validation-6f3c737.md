<!-- loio6f3c737aa18c4181b1f0a343755f335e -->

# Project Validation

You can validate a project using the `Fiori: Validate Project` command.

When the project is generated, you can validate it by opening the Command Palette \([CMD/CTRL\] + [Shift\] + [P\] \) and executing the `Fiori: Validate Project` command. Select a project for validation from the projects in your workspace.

The validation comprises of the following steps:

-   **project**

    The project step checks that files such as `package.json`, `manifest.json`, and `ui5.yaml` exist and their mandatory fields are filled.

-   **annotation**

    The annotation step validates the project annotation files using the same modules as the XML annotation language server extension.

-   **specification**

    The specification step validates the `manifest.json` file and files in the `changes` folder. The `@sap/ux-specification` module is used to import the project and provide error messages about an invalid configuration.

-   **`eslint`**

    The `eslint` step checks if `eslint` is installed as a dependency. If it is, the project validation runs the ESLint check based on the project's configuration. We recommend using the `@sap-ux/eslint-plugin-fiori-tools` ESLint plugin. For more information, see [@sap-ux/eslint-plugin-fiori-tools](https://www.npmjs.com/package/@sap-ux/eslint-plugin-fiori-tools).


After all validation steps are executed, a report is generated and displayed as a Markdown \(`.md`\) file and in the *Problems* tab of Visual Studio Code \(VS Code\) or SAP Business Application Studio.

