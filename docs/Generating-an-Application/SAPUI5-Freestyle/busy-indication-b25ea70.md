<!-- loiob25ea703cc3c47229b6cf241bca7149a -->

# Busy Indication

The List-Detail application implements a busy indication concept as specified by the SAP Fiori Design Guidelines. Calling the application will result in the following:

-   Only initially a global busy indicator is displayed that overlays the whole application until the metadata of the service is loaded.
-   Afterwards, a local busy indicator is displayed on the list and the detail page.
-   When the detail page is loaded, the line item table on the detail page is set to busy until the line items are loaded with a separate service call.
-   When controls are loading additional data or getting refreshed, a local busy indication is displayed automatically.

By default, the busy indicator delay is set to one second for all controls. This would first show the UI for a second, then show a busy indication until the data is loaded. To avoid this behavior initially and show the busy indicator immediately without delay, the following concept is implemented in the application: The `busyIndicatorDelay` and `busy` properties of certain controls \(`AppView`, `List` on the *List* page, `DetailPage` and `Table` on the *Detail* page\) are bound to the local view model and manipulated in the controllers of the application. The delay is initially set to *0* for displaying the busy indicator immediately, and reset to the previous value after the initial loading is done.

You can simulate server delays to test this implementation running with mocked application data by using the URL parameter `serverDelay=true` in the hash. The default is set to *1000ms*.

> ### Note:  
> You can find more information about busy indicators, busy states, and busy handling in general in the [SAP Fiori Design Guidelines](https://experience.sap.com/fiori-design/).

