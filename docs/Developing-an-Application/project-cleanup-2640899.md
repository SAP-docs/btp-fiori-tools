<!-- loio2640899ad445407abfefe24bdf74272c -->

# Project Cleanup

The project cleanup procedure is defined with the ![](images/Project_Cleanup_9853741.png) \(*Cleanup*\) icon and removes the following elements:

-   All orphaned `UI.FieldGroup` and `UI.LineItem` with annotations, which are not referenced as the `UI.ReferenceFacet` targets.
-   Annotations with the terms `UI.MultiLineText`, `Common.ValueListWithFixedValues`, `Common.Text`, `Common.ValueList`, and `Common.FieldControl` are applied to entity properties that are not mentioned in any referenced annotations.

