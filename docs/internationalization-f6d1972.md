<!-- loiof6d19722616f47bc8df05b6e858bbd89 -->

# Internationalization

Adaptation project supports internationalization \(i18n\), which enables you to provide easily translatable text for applications. The topic describes the ways in which you provide text for internationalization. You can define i18n key-value pairs and change the value for existing i18n keys.

**Context**

Internationalization refers to the process of designing and developing a software application and its content so that it can be adapted to multiple languages without making much engineering changes.

When you create an Adaptation project, an *i18n.properties* file is created for every page of the application. Define a key-value pair in the *i18n.properties* file that you can refer to while providing text for the UI controls.

**Sample Folder Structure**

In your workspace, under the Adaptation project, the folder structure looks like \(this is an example\):

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

Define your key-value pairs in the *i18n.properties*. Refer to the keys while you edit the project using SAPUI5 Visual Editor. In the *Properties* pane, refer to the i18n key for a SAPUI5 control instead of typing-in the text. Run the project as a web application and check whether the i18n value associated to the key appears on the UI control. Similarly, you can change the text of existing UI controls by overriding the associated i18n key-value pairs in the source application.

