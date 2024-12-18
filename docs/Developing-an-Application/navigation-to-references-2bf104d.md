<!-- loio2bf104d939c543f1a3407b3de4fbf679 -->

# Navigation to References

XML annotation language server lets you check where your annotations and metadata elements are referenced within the codebase. For example, if your annotation or metadata file contains `UI.LineItem` annotation, you can check if and in which other annotations such as `UI.Facets` it’s referenced.

Similarly, you can check if a specific metadata element, such as entity type, property, and action is used within the annotation values or whether any annotations are applied to it.

Checking the references before making any changes to annotations or metadata elements gives you an overview of the potential impact of these changes.



<a name="loio2bf104d939c543f1a3407b3de4fbf679__section_a2g_kvk_gxb"/>

## Find All References

Place your cursor inside the metadata element name or annotation term/qualifier and trigger *Find All References*

-   Using the keyboard: press [Alt\] + [Shift\] + [F12\]  in Windows and [Option\] + [F12\]  in macOS

-   Using the mouse: right-click and select *Find All References*


The list of references opens in the *References* pane. You can then choose the individual reference to view or update in the file.

> ### Note:  
> When triggered for metadata elements, the definitions are also included in the list.



<a name="loio2bf104d939c543f1a3407b3de4fbf679__section_lb2_5vk_gxb"/>

## Go to References

Place your cursor inside the metadata element name or annotation term/qualifier and trigger *Go To References*

-   Using the keyboard: press [Shift\] + [F12\] 

-   Using the mouse: right-click and select *Go To References*


The list of references opens in the peeked editor. You can make quick edits right there without leaving the file.

