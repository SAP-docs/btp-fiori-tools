<!-- loioeb427f25160a4bef9f723e8256735922 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Internationalization \(i18n\)

Internationalization, often abbreviated as i18n, is the process by which developers prepare a software product to be adapted in other languages. This topic covers the following aspects of managing i18n translation files for your projects:

-   [i18n Configuration](internationalization-i18n-eb427f2.md#loioeb427f25160a4bef9f723e8256735922__section_wf2_g11_bsb)
-   [Label Translation Cases](internationalization-i18n-eb427f2.md#loioeb427f25160a4bef9f723e8256735922__section_ols_yb1_bsb)
-   [Mass i18n Creation](internationalization-i18n-eb427f2.md#loioeb427f25160a4bef9f723e8256735922__section_n1s_f31_bsb)

To enable translation, click the :globe_with_meridians: \(*Internationlization*\) icon.

When a new confirmation pop-up window appears, click *Apply* to confirm the action. Changes are applied to 18n property.



<a name="loioeb427f25160a4bef9f723e8256735922__section_wf2_g11_bsb"/>

## i18n Configuration

A resource bundle folder is also known as i18n folder and file names are maintained in the configuration as follows:

-   Non-CAP projects at `/webapp/manifest.json`.
-   CAP projects at `.cdsrc.json or package.json`. CAP has a configuration setting where the folder names can be used. The default value is `['_i18n', 'i18n', 'assets/i18n']`.



<a name="loioeb427f25160a4bef9f723e8256735922__section_ols_yb1_bsb"/>

## Internationalizing UI Texts

Most UI texts in the application page, such as sections or field labels, are translation relevant and are eligible for internationalization. When you add elements that aren’t directly based on an entity property, such as a section, you’re asked to enter a desired text for the label directly in the *Add* dialog. When you add an element that is based on a property, such as section field or basic table column, you aren’t prompted to enter a label text. Instead a label defined on the property is used if it’s already defined or generated based on a property name. You have then the option to change this label for the given context in the *Property Panel*.

Independent on the origin of the translation relevant texts, whenever it appears in the *Page Editor* UI, e.g. properties pane or *Add* dialog, the*Internationalization \(i18n\)* icon appears on the right side of the input field. With this icon, you can handle the internationalization of the text string used in that specific field. It works as follows:

1.  When the label isn’t internationalized:

    Click the *Internationalization \(i18n\)* icon and the following message appears with the user actions *Apply* and *Cancel*:

    ```
    Generate a text key <uniquekey> in the i18n file and substitute <actual text> by {i18n>uniquekey}.
    ```

    With the *Apply* action, a new i18n key with text is generated and written to the i18n file, as well as referenced as a label.

    > ### Note:  
    > If the **Field** or **Column** label is defined directly on the property with `@title` or `@Common.Label` annotations in the lower layer, the Label property is generated in the respective `UI.DataField` record with the reference to the i18n text in the resource bundle. The existing `@title` or `@Common.Label` annotations aren’t modified or overridden.

    > ### Note:  
    > If the `UI.FieldGroup` or `UI.Facet` annotation is located in the lower layer, then it first creates a copy in the application layer.

2.  When the label is defined as a reference to the text key but the text key is missing in the i18n files:

    Click the *Internationalization \(i18n\)* icon and the following message appears with the user actions *Apply* and *Cancel*:

    ```
    Generate a text key <uniqueKey> with value <uniquekey> in i18n file.
    ```

    With the *Apply* action, the i18n key, and text with the same value as the key is written to the i18n file.

3.  When the label is defined as plain text but the text key for that text already exists in the i18n file:

    Click the *Internationalization \(i18n\)* icon and the following message appears with the user actions *Apply* and *Cancel*:

    ```
    Text key <uniqueKey> for value <sample text> is available in i18n file. Substitute <sample text> by {@i18n>uniqueKey}.
    ```

    With the*Apply* action, an existing i18n key is referenced as a label.


> ### Note:  
> The i18n key is generated in camelCase for non-CAP projects and PascalCase for CAP projects.

> ### Note:  
> As you often need to change the labels several times during the application development, the *Internationalization \(i18n\)* icon creates a new entry in the i18n file for each new text, so you can end up with a number of unused i18n texts that will be provided for translation. To avoid the redundant keys and reduce the translation cost, it is recommended to handle i18n at the end of the development phase when labels are not likely to change.



<a name="loioeb427f25160a4bef9f723e8256735922__section_n1s_f31_bsb"/>

## Mass i18n Creation

In addition to the internationalization on the single text level, the :globe_with_meridians: \(*mass i18n generation*\) icon is provided on the top of the screen. It reduces the effort for preparing multiple UI texts for translation.

