<!-- loio6f3c737aa18c4181b1f0a343755f335e -->

# Project Validation

When the project is generated, you can validate it by executing `Fiori: Validate Project`. Use a quick pick selection to select a project for validation from the multiple projects in the workspace.

The validation comprises of the following steps:

-   **project**

    In the project step, a validation checks existence and semantic correctness of the mandatory files, such as `package.json`, `manifest.json`, and `ui5.yaml`. In this step, these files are read and mandatory entries are checked, such as the existence of `devDependencies` in `package.json`.

-   **annotation**

    The annotation step validates the project annotation files using the same modules as uses the extension XML annotation language server. It reports the same results as if all local and backend annotation files are opened in the project one by one.

-   **specification**

    In the specification step, the content of `manifest.json` and change files in the changes folder are validated in detail. The module `@sap/ux-specification` is used to **import** the project and in return gives messages in case of invalid configuration.

-   **eslint**

    The validation step for a projects checks if `eslint` is installed as a dependency. If it is, the project validation runs the `eslint` check based on the project's configuration and the rules defines in the <code><a href="https://www.npmjs.com/package/eslint-plugin-fiori-custom">eslint-plugin-fiori-custom</a></code>. The results of this check are then collected. You can enable `eslint` support for a new project by selecting the appropriate options in the Advanced Options of the SAP Fiori application generator, as described in the [Additional Configuration](../Generating-an-Application/Additional-Configuration/additional-configuration-9bea64e.md) section.


After all validation steps are executed, a report is written and displayed as a markdown \(.md\) file and in the **Problems** tab of VS Code or SAP Business Application Studio.

