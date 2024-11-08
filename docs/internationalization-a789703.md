<!-- loioa7897032b0864542872654a26434bf0b -->

# Internationalization

Adaptation projects support internationalization \(i18n\) which enables you to provide easily translatable text for applications. This topic describes the ways in which you can provide text for internationalization. You can define i18n key-value pairs and change the value for existing i18n keys.

**Context**

Internationalization is the process of designing and developing a software application so that it can be adapted to multiple languages without making major engineering changes.

When you create an adaptation project, an `i18n.properties` file is created for every page of the application. Define a key-value pair in the `i18n.properties` file to refer to when providing text for the UI controls.

**Folder Structure**

In your workspace, under the adaptation project, the folder structure is:

-   Project name

    -   webapp

        -   i18n

            -   page 1

                -   collection

                    -   i18n.properties



            -   page 2

                -   collection

                    -   i18n.properties







**Define Key-Value Pair**

Define your key-value pairs in the `i18n.properties` file. Refer to the keys while you edit the project using the Adaptation Editor. In the *Properties* pane, refer to the i18n key for a SAPUI5 control instead of typing in the text. Run the project as a web application and check whether the i18n value associated to the key appears on the UI control. You can also change the text of existing UI controls by overriding the associated i18n key-value pairs in the source application.

