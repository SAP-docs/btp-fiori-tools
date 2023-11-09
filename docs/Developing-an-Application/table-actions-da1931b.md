<!-- loioda1931b61b9442fd8f5f7d80cdd99aba -->

# Table Actions

Table actions can be placed in a toolbar or inline in table rows in an *Object Page* section, or a *List Report*. With the *Page Editor*, you can configure the actions to be performed within the application and external navigation actions to navigate to a different \(target\) application configured in the SAP Fiori launchpad. The actions to be performed within the application are based on the records of type `UI.DataFieldForAction` and the actions for actions navigation to the different application are based on `UI.DataFieldForIntentBasedNavigation`.

> ### Note:  
> To enable the cross application navigation, the appropriate configuration must be set in the SAP Fiori launchpad and in the `manifest.json` of the target application.

Toolbar and inline action definitions differ in the property `Inline` of `UI.DataFieldForAction`. This means, actions displayed as table columns are defined with the property `Inline` set to `true` in the corresponding record.

![](images/Table_Toolbar_Actions_10ff824.png)



<a name="loioda1931b61b9442fd8f5f7d80cdd99aba__section_nhp_11m_zrb"/>

## Adding Action

Adding the table actions to be performed within the app is possible if there’s an available **Action** or **Function** defined in the service. Bound actions and bound functions are only considered if they’re applied to the same entity type as `UI.LineItem` defining the table for which the action should be created.

Adding external navigation actions is possible as long as you know the semantic object name and action as defined in the target application.

Adding the table actions can be applied to the following nodes in the *Page Editor*:

-   *List Report*: Columns or Toolbar node in a Table node.
-   *Object Page*: Columns or Toolbar node for a Table section.

To add an action, do the following:

1.  Click [\+\] in the respective node and choose the type of action to add.
2.  Provide the requested data:
    -   For the table actions to be performed within the app, choose **Action** or **Function** representing.
    -   For the external navigation actions, enter the semantic object name and action name as defined in the target application.

3.  Choose [Add\]. The Inline property of `UI.DataFieldForAction` or`UI.DataFieldForIntentBasedNavigation` is added and set to true.

When action is added as a table column, the `Inline` property of `UI.DataFieldForAction` is added and set to `true`.



<a name="loioda1931b61b9442fd8f5f7d80cdd99aba__section_yrp_b1m_zrb"/>

## Maintaining Table Action Properties

**Label**

The label for a table action to be performed within the application, is derived from existing annotations `Common.Label` or `@title` \(CAP CDS\) targeting the action.

If these annotations are missing, the property `Label` is generated within `UI.DataFieldForAction`. You can change the label, the changed value is persisted in `UI.DataFieldForAction`.

> ### Note:  
> When an action is deleted, annotations `Common.Label` or `@title` aren’t deleted, only the `Label` property of the `UI.DataFieldForAction` gets deleted along with the table action.

The label for an External navigation action is derived from **Semantic Object Name** and**Semantic Object Action** you entered when adding the action. For example, if you entered **Customer** as **Semantic Object Name** and **display** as **Semantic Object Action**, the label is generated as **Display Customer**.

**Importance**

When the action is added as a table column, the *Importance* property provided. For more information, see [Table Columns/Maintain Table Columns/Importance](table-columns-a80d603.md).

**Semantic Object Name**

This property is required for the external navigation actions and must match the name of the relevant semantic object in the target application.

**Semantic Object Action**

This property is required for the external navigation actions and must match the name of the relevant action for the semantic object as defined in the launchpad configuration.

**Mapping**

If the semantic object name defined for the external navigation action differs in current and target application, this property can be used to define the mapping.

Choose *Add Semantic Mapping* and enter the name of the semantic object property as defined in the target application. Then choose the local property corresponding to it. You can define only one mapping per external navigation action.

**Requires Context**

If the external navigation action is defined in the table toolbar, you can use this property to define whether a table row needs to be selected as a navigation context. By default, it’s set to off state that is interpreted as context not required and the end user can choose this action without the table row selection. This property is not available for the actions set as table columns, as in that case context is always available.



<a name="loioda1931b61b9442fd8f5f7d80cdd99aba__section_ag2_dcw_ksb"/>

## Moving Action

Moving a table action from **toolbar** to **columns** or vice versa will switch the **Inline** property accordingly. Table action can only be moved within the same table.



<a name="loioda1931b61b9442fd8f5f7d80cdd99aba__section_sy4_btn_qxb"/>

## Deleting Actions

You can delete actions by choosing the delete icon ![](../Project-Functions/images/Delete_icon_VS_Code_86e90a9.png).

