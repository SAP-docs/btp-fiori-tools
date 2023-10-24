<!-- loio1fd8f54bbba9425eb3abfd5f2978aa9c -->

# Diagnostics

XML annotation language server validates the annotation file against the project metadata, annotation vocabularies, and OData specification. Validation is performed when you open the annotation file and then is retriggered with each change to the annotation files, metadata, or project structure.

> ### Note:  
> Annotations embedded in the metadata and dynamic expressions aren’t supported by Diagnostics feature.

Annotation LSP provides error, warning, and info messages, as well as actions to fix problems - Quick Fixes.



<a name="loio1fd8f54bbba9425eb3abfd5f2978aa9c__section_rcf_rnt_1mb"/>

## Working with Diagnostics

You can view the diagnostic messages by hovering over the highlighted part in the annotation file or by opening the Problems panel.

> ### Note:  
> Click on the message in Problems panel to navigate to the related place in the annotation file.

You can fix the diagnostic message in several ways, depending on the issue:

-   Using the Code Completion \(provided when the issue is related to the incorrect element or value\)
    -   Trigger the code completion by [Ctrl\] + [Space\]  \(Win\),[CMD\] + [Space\]  \(Mac\)
    -   Choose one of suggested values.

-   Choosing one of the suggested Quick Fix actions \(if provided\)
    -   Click on Light bulb icon is showed along with diagnostic error
    -   Choose one of the suggested actions to fix the problem

-   Manually

> ### Note:  
> Diagnostics for annotations in the local copies of the metadata and back-end annotation file is provided for the information purposes only. All the relevant fixes should be made in the original service metadata. Changes to the local copies will not affect the deployed app or preview with the real service data.

