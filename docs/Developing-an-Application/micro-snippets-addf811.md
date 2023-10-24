<!-- loioaddf811a782a4b97baddb56fa3e1f7a6 -->

# Micro-Snippets

Micro-snippets are context-specific blocks of code that can be inserted using the code completion feature instead of typing the code manually or using a sequence of the word based completions.

For example if you are within the `<Schema>` tag, you can define the annotation target `<Annotations Target=""></Annotations>` in 3 different ways:

-   Type it in manually
-   Type in opening tag bracket `<` and use the word based completions to add`Annotations` then space and trigger the code completion again to add `Target`.
-   Use code completion and select the micro-snippet to add the complete code block, with the cursor automatically placed within `""` to enable one-step target selection.

    > ### Note:  
    > You can view the code snippet for the highlighted option in the code completion list in the documentation window. For more information, see [Documentation \(Quick Info\)](documentation-quick-info-8728bd7.md) feature.

    > ### Note:  
    > XML Annotation LSP provides micro-snippets for annotation targets, terms, records and property values.


The micro-snippets is the fastest way to define annotations and together with the word based completion for annotation or metadata elements it eliminates a need to type in the code, thus speeding up the process and helping you to avoid typos or semantical errors.

For annotation records, two types of micro-snippets are provided for each option: one containing only mandatory properties defined in the respected vocabulary as *nullable=false* and one containing all properties defined for this record.

Usually you need to add just a subset of **properties** to the record, you can either select a full record and then remove the **properties** you don’t need, or add the record containing only required properties and then add the remaining properties one by one or all together.

