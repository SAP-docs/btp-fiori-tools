<!-- loio1b391bd22c0341a6948ddc49b0aa1184 -->

# Footer

**Actions**

Actions are displayed in the *Footer* as buttons. Header actions are based on the `UI.DataFieldForAction` records with `Determining` property set to `true` in `UI.Identification` annotation that is applied to the main entity.

> ### Note:  
> External navigation actions cannot be set in the *Footer*, irrespective of the `Determining` value.

You can add, delete and maintain the footer actions in the same way as the actions based on `UI.DataFieldForAction` described in [Table Actions](table-actions-da1931b.md).

> ### Note:  
> The properties *Importance* and *Requires Context* are not relevant for the header actions.
> 
> The *Criticality* property impacts the sequence of the actions in the *Object Page* footer. Therefore, once you change its value from *None* to *Positive* or *Negative* \(or vice versa\), the sequence of the action nodes in the *Page Editor* outline view is automatically updated.

You can move actions from the *Footer* to the page header and to the *Form* sections based on the main entity of the page, as long as these actions are not semantically highlighted.

