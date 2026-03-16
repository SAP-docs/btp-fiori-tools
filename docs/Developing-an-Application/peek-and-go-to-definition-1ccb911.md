<!-- loio1ccb911d042942829191b1e27255b6b1 -->

# Peek and Go to Definition

You can enable *Peek Definition* and *Go to Definition* to navigate and preview annotations.



## Prerequisites

You must enable the `cds.contributions.features.index` setting in your user or workspace settings to enable these features in CAP projects.



## Peek Definition

*Peek Definition* lets you preview and update the referenced annotation without switching away from the code that you are writing. It is triggered when your cursor is inside the referenced annotation value.

-   Using the keyboard: press [Alt\] + [F12\]  in Windows and [Option\] + [F12\]  [Option F12\] in macOS.
-   Using the mouse: right-click and select *Peek Definition*.

If an annotation is defined in multiple sources, all these sources are listed. You can select which one you would like to view or update. Annotation layering is not considered.



## Go to Definition

*Go to Definition* lets you navigate to the source of the referenced annotation and opens the source file scrolled to the respective place in a new tab. It is triggered when your cursor is inside the referenced annotation value.

Place your text cursor inside the path referencing the annotation term segment or translatable string value and use *Go To Definition* by performing the following:

-   Using the keyboard: Press [F12\] in Visual Studio Code or [Ctrl\] + [F11\]  in SAP Business Application Studio.

-   Using the mouse: Right-click and select *Go to Definition*.

-   Using the keyboard and mouse: [Ctrl\] + mouse click in Windows and [CMD\] + mouse click in macOS.


If an annotation is defined in multiple sources, the peek definition lists these sources instead. Annotation layering isn’t considered.

