<!-- loio07012f9c566342bf8f1bb1c2d74e3d81 -->

# Actions

Actions are displayed in Form sections as buttons. Form actions based on `UI.DataFieldForAction` are performed within the application whereas those based on `UI.DataFieldForIntentBasedNavigation` are used for external navigation from the current application to a different \(target\) application configured in the SAP Fiori launchpad.

You can add, delete and maintain the header actions same as described in the [Table Actions](table-actions-da1931b.md) section.

> ### Note:  
> Properties applicable only to action columns \(**Importance, Requires Context**\) are not relevant and therefore not provided for header actions.

You can move actions from the form sections to other form sections based on the same entity. You can move the external navigation actions i.e. based on `UI.DataFieldForIntentBasedNavigation` to the page header. You can move actions performed within the application, i.e. based on `UI.DataFieldForAction` to the page header and footer, as long as your form section is based on the main entity of the page.

