<!-- loio07012f9c566342bf8f1bb1c2d74e3d81 -->

# Actions

Actions are displayed in form sections as buttons. Form actions based on `UI.DataFieldForAction` are performed within the application whereas those based on `UI.DataFieldForIntentBasedNavigation` are used for external navigation from the current application to a different \(target\) application configured in SAP Fiori launchpad.

You can add, delete, and maintain the header actions in the same way as described in the [Table Actions](table-actions-da1931b.md) section.

> ### Tip:  
> Properties applicable only to action columns such as *Importance* and *Requires Context* are not relevant to form actions.

You can move actions from the form sections to other form sections based on the same entity. You can move the external navigation actions, for example, based on `UI.DataFieldForIntentBasedNavigation`, to the page header. You can move actions performed within the application, for example, based on `UI.DataFieldForAction`, to the page header and footer, as long as your form section is based on the main entity of the page.

You can group annotation-based actions into action menus based on `UI.DataFieldForActionGroup`. To do this, add an action menu with one or more annotation-based actions. You can also add annotation-based actions to existing action menus and move actions to them. Note: You cannot move actions with criticality to action menus because criticality is not supported for actions in menus.

> ### Restriction:  
> Manifest-based actions cannot be grouped in menus using the *Page Editor*.

