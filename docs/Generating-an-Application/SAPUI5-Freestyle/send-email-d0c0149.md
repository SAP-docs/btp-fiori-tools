<!-- loiod0c0149e4bb44c47800bc479d60f18bf -->

# Send Email

The **Send Email** feature is a sharing option that can be found in the share menu of each view.

This feature simply triggers a `sap.m.URLHelper` action that will show a new email with preconfigured texts in the default client of the user.

The placeholder texts are located in the resource model and can be adjusted to your use case. The texts already include the current context and the current location. The texts may vary for each view, therefore they are configured with the local view model and updated when the business object context has changed.

For more information about `sap.m.URLHelper`, see the [sample](https://sapui5.hana.ondemand.com/#/api/sap.m.URLHelper%23methods/Summary) in the Demo Kit.

