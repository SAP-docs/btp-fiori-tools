<!-- loiob78c767eba97469f845f4743e44abd0c -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Contact Field

An SAP Fiori application can display contact information as a quick view for a [Form Section](form-section-4102b3d.md) or [Identification Section](identification-section-b83f501.md) of an *Object Page* as a *Contact Field*.



<a name="loiob78c767eba97469f845f4743e44abd0c__section_al5_jjr_35b"/>

## Adding Contact Field

To add a contact field to a section, perform the following steps:

1.  Click [Add Contact Field\] when choosing [\+\] button in Form or Identification node in the *Page Editor* .
2.  Select `Contact` via a tree control.
3.  Click `Add`, a new `Communication.Contact` annotation is created.

> ### Note:  
> Contact fields are based on the `UI.DataFieldForAnnotation` record type contained in the annotations `UI.FieldGroup`/`UI.Identification` \("base annotation"\) and reference a `Communication.Contact` annotation in the `Target` property.



<a name="loiob78c767eba97469f845f4743e44abd0c__section_srw_hg5_j5b"/>

## Moving Contact Field

A contact field can be moved within a section as any other field. It can be moved between sections unless forbidden by the relative paths of `Communication.Contact` and the base annotations.



<a name="loiob78c767eba97469f845f4743e44abd0c__section_xkr_mg5_j5b"/>

## Deleting Contact Field

To delete the contact column/field in the application, perform the following steps:

1.  Navigate to a field.
2.  Click the :wastebasket: \(*Delete*\) icon to open the *Delete Confirmation* popup window.
3.  Click *Delete* to confirm the action.

