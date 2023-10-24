<!-- loio42a062e9abe44e72be16cfc904c09735 -->

# Testing

The templates include basic testing features, unit tests as well as integration tests for a basic test coverage of the initial app. The tests are written independently of the actual data displayed in the app.

The `webapp` folder of the template app contains a `test.html` file which serves as an overview for the different test pages. You can run the app with or without mock data and run the unit and integration tests. This section describes which application tests are provided and how they are structured.



## Integration Tests

The integration tests shipped with the template cover all basic functionality and provide several "journeys". Journeys include a series of OPA tests that belong to the same functionality and should be executed together:

-   `NavigationJourney`: This journey will trigger user interactions and navigate through the application. The routing configuration, basic navigation events, and error handling are tested here.

-   `NotFoundJourney`: Several "not found" cases of the application are tested here. Faulty navigation scenarios are introduced intentionally to simulate errors.

-   `WorklistJourney`: A series of tests for the *Worklist* page that check the busy indication and sharing features built into the app.

-   `ObjectJourney`: A series of tests for the *Object* page that check the busy indication and sharing features built into the app.

-   `FLPIntegrationJourney`: This journey is available if you have enabled SAP Fiori launchpad \(FLP\) for your app. It tests the FLP integration features *Save as tile* and *Share on SAP Jam*.

-   `AllJourneys`: This is a convenience journey that will call all the other journeys specified above and is used in the test suite file.


You can execute all journeys by calling the test suite file `opaTests.qunit.html` in the `webapp/test/integration` folder or selecting the *run all integration tests* link in the `test.html` file in the app’s root folder.

For more information, see [Integration Testing with One Page Acceptnce Tests \(OPA5\)](https://ui5.sap.com/#/topic/2696ab50faad458f9b4027ec2f9b884d.html) and [sap.ui.test.Opa5](https://sapui5.hana.ondemand.com/explored.html#/entity/sap.ui.test.Opa5/samples) in the *Samples* within the Demo Kit.



## Unit Tests

In the `unit` subfolder you can find all unit tests for our application. They are structured similarly to the structure of the `webapp` folder. For example, controller tests are located in the `controller` folder whereas formatter tests are located in the `model` folder.

Unit tests are included for the following functionality:

-   App controller tests
-   Worklist controller tests
-   Formatters
-   Device model

As with the integration tests, you can execute all unit tests by calling the test suite file `unitTests.qunit.html` in the `webapp/test/unit` folder or selecting the *run all unit tests* link in the `test.html` file in the app’s root folder.

For more information, see [Unit Testing with QUnit](https://ui5.sap.com/#/topic/09d145cd86ee4f8e9d08715f1b364c51.html),, [https://qunitjs.com/](https://qunitjs.com/) and [http://sinonjs.org/](http://sinonjs.org/).

