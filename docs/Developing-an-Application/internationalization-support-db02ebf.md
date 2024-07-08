<!-- loiodb02ebfcee1a47808ee4e4c4a9e07098 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Internationalization Support



XML annotation language server provides support for internationalization of language-dependent strings in your annotation file.

Language-dependent strings are the string values of annotation properties tagged with*IsLanguageDependent* in the respective vocabulary. For example, out of the two string values below, only that for *Label* property is considered as language dependent, as it is tagged as*IsLanguageDependent* in the [UI vocabulary](https://sap.github.io/odata-vocabularies/vocabularies/UI.html). Any value of property ID isn’t tagged as language dependent in the vocabulary and thus is not considered for internationalization by Annotation LSP.

When you open an annotation file, all language-dependent string values are checked against the`i18n.properties` file.

> ### Note:  
> Annotation LSP uses the`i18.properties` file referenced in the @18n model of the `manifest.json` file of your project. If the model or file is missing, you see the respective warning message for your annotation file.

Each value that doesn’t represent a valid reference to the existing text key in the `i18n.properties` file, is indicated in the annotation file with a warning. If the text key for the string value is already available in `i18n.properties` file, you can apply a **Quick Fix** to automatically reference it in your annotation file. Otherwise, a **Quick Fix** action is suggested to generate a new text key and then substitute your string value with the reference to that entry.

The same check is performed when you add a new value for a language-dependent property. As an alternative, you can use the [Code Completion](code-completion-dd4fc3b.md) directly in the string value of the language-dependent property. It will show the list of references to text entries already available in the properties file. You can use [Documentation \(Quick Info\)](documentation-quick-info-8728bd7.md) feature to view the text value and attributes for each list item.

If you want to view or update the text value or attributes in `i18n.properties` file, use the Pick Definition or Go To Definition features, see [Peek and Go to Definition](peek-and-go-to-definition-1ccb911.md).



<a name="loiodb02ebfcee1a47808ee4e4c4a9e07098__section_yr4_3hl_1mb"/>

## Using Internationalization Support



### Adding Internationalized Values

Reusing Existing Texts

-   With Code Completion

    -   Trigger the Code Completion [Ctrl\] + [Space\]  \(Win\),[CMD\] + [Space\]  \(Mac\) for the string value in the language-dependent element.

        The list of existing text key reference / text value pairs from the `i18n.properties` file is displayed.

    -   Select a value from the Code Completion list.

        The text key reference from the selected completion item is inserted.


-   With Quick Fix Action

    -   Click on the :bulb: \(*Light Bulb*\) icon that is shown along with a warning
    -   Choose the suggested action


Defining new texts

-   Enter a string value for the language-dependent element.

    Annotation LSP checks if the value is already provided as a text key in`i18n.properties` file.

    If the value isn’t provided a warning along with Quick Fix action is shown.

-   Click on the :bulb: \(*Light Bulb*\) icon and choose the suggested action.

    Text key and default attributes are generated in the `i18n.properties` file and the text string is substituted with the reference.

    > ### Note:  
    > You can add translation comments or update other attributes as described below.




### Highlighting and Fixing Missing References

-   Open the annotation file.

    If missed referenced are found - a warning is shown.

-   Apply Quick Fix action. See Adding Internationalized Values for more details.




### Updating Text Properties from Annotation File

**Using Go to Definition**

Place your text cursor inside the path referencing the translatable string value and trigger *Go To Definition*:

-   Using keyboard: press [F12\] in VS Code, [Ctrl\] + [F11\]  in SAP Business Application Studio

-   Using the mouse: right-click and select *Go To Definition*

-   Using the keyboard and mouse: [Ctrl\] + mouse click \(Win\), [CMD\] + mouse click \(Mac\)


**Using Peek Definition**

Place your text cursor inside the path referencing to translatable string value and trigger *Peek Definition*:

-   Using the keyboard: press [Alt\] + [F12\]  \(Win\), [Option\] + [F12\]  \(Mac\)
-   Using the mouse: right-click and select *Peek Definition*

