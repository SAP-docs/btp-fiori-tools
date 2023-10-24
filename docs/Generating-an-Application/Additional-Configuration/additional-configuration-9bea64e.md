<!-- loio9bea64e63b824261932d90037ce3c5ae -->

# Additional Configuration



<a name="loio9bea64e63b824261932d90037ce3c5ae__section_itv_dk5_t4b"/>

## Add Deployment Configuration

1.  Select *Yes* if you want to configure deployment settings.
2.  From the *Choose the target* drop-down list, select the deploy target from the following options:
    -   ABAP
    -   Cloud Foundry


When the target system is selected, the SAP Fiori launchpad wizard steps with the prompts appear *Deploy Configuration*.



### ABAP system

-   *Destination name* \(required\). The ABAP destination to the back-end system.
-   *Is this an SAP Cloud Platform system?*

    Select *Yes* or *No*. Applicable only if the system is discovered to be a Steampunk system.

-   *Target System URL*. This field has already been prefilled according to the selected project.

    Not applicable in SAP Business Application Studio.

-   *Client*. A self-contained commercial, organizational, and technical unit within an SAP system. Business data of clients are separated from each other, and clients serve a specific purpose in an SAP instance.

    Not applicable to a Steampunk system and in an SAP Business Application Studio.

    The following options are available to select from:

    -   Use project defined client - xxx
    -   Enter client
    -   Use default system client

-   *Is this an SAP S/4HANA Cloud system?* Select *Yes* or *No*. Not applicable if the user responds *Yes* to the `Is this an SAP Cloud Platform system?` question.
-   *SAPUI5 ABAP Repository* \(required\). The technical name of the SAP Fiori application being deployed.
-   *Package*. A transportable ABAP repository object that groups development objects. An SAP Fiori application deployed in the ABAP backend must be assigned to an appropriate package. If it’s supposed to be a local application that isn't sent to another system, the package can be $TMP. In this case, there’s no Transport Request. Not applicable for SAP S/4HANA Cloud.
-   *Fetch Transport Request list from target system?*. Select *Yes* or *No*. If you select *Yes*, the applicable list of transport requests is retrieved from the target system and displayed in a dropdown for you to choose. If the lists of transport requests are unable to be retrieved from the target system, the existing manual text entry will be required.
-   *Transport Request number*. The ID of a container that is used to transfer data from one SAP installation to another. It collects changes made in a development system, allowing distribution of them across the defined transport landscape.

    Not applicable for SAP S/4HANA Cloud system. For more information on transport requests, see [Managing Transport Requests](https://help.sap.com/viewer/8b923a2175be4939816f0981b73856c7/7.2.12/en-US/60264ffa451548f9857f46423afdd1f1.html).




### Cloud Foundry system

-   *Destination name* \(required\). The Cloud Foundry destination to the back-end system.



<a name="loio9bea64e63b824261932d90037ce3c5ae__section_hbd_gzy_t4b"/>

## Add FLP Configuration

Select *Yes* if you want to add an SAP Fiori Launchpad configuration. A new step appears with the *FLP Configuration* prompts.

> ### Note:  
> If the configuration already exists, the existing values are displayed. In this case, the user still can change the inputs.

-   *Semantic Object*. Represents a business entity, such as a customer, a sales order, or a product. Using semantic objects, the user can bundle applications that reflect a specific scenario and refer to objects in a standardized way, abstracting from concrete implementations of these objects. It’s used in mapping URLs of SAP Fiori applications to objects in the launchpad.
-   *Action*. Describes which operation, such as display or approve Purchase Orders, is intended to be performed on a semantic object. For example, Purchase Order or Product.
-   *Title*. The name of the Fiori application that appears on the SAP Fiori launchpad tile in a free text format.
-   *Subtitle* \(optional\). A free text field where the user can further describe the application in the launchpad.



<a name="loio9bea64e63b824261932d90037ce3c5ae__section_uhj_l2z_t4b"/>

## Configure Advanced Options

Select *Yes* if you want to configure advanced options.

-   Select SAPUI5 theme:
    -   [Quartz Light](https://help.sap.com/viewer/0120a9e442b44ad9925841dde3bc521f/201909.002/en-US/bf53ad16229e4e438dc0ea5c42064cff.html?q=-%09SAP%20Quartz%20Light%20)
    -   [Belize](https://help.sap.com/viewer/8ec2dae34eb44cbbb560be3f9f1592fe/1709%20002/en-US/977672c6940f48578d08d770bee236f2.html?q=SAP%20Belize)
    -   [Quartz Dark](https://help.sap.com/viewer/085edb30fb3d413da552832f3d5c01c0/2002.500/en-US/ed83b3029c724c9cb267cc4c6eff1068.html?q=SAP%20quartz%20dark)

        > ### Note:  
        > Quartz Dark is only available on SAPUI5 versions 1.72 and later.

    -   [Morning Horizon](https://experience.sap.com/fiori-design-web/theming/)
    -   [Evening Horizon](https://experience.sap.com/fiori-design-web/theming/)

        > ### Note:  
        > Morning Horizon and Evening Horizon are shown in the dropdown if the minimum SAPUI5 version selected is **1.102** or above. **Morning Horizon** is selected by default.


-   *Add Eslint configuration to the project*.

    Choosing this option includes the Fiori [eslint plugin library](https://www.npmjs.com/package/eslint-plugin-fiori-custom) in the generated application that allows the developer to check and ensure that the Fiori application adheres to the best practice for Fiori code development. Executing the target `npm run lint` in the generated application checks for any linting errors.

-   *Add javascript code assist libraries to your project*

    With this option, libraries are included in the generated project to provide `ui5` code completion prompts in the editor along with the `eslint` rules and recommended configuration for the static `jsdoc` code checks.

    For more information, see [Adding Javascript Code Assist](adding-javascript-code-assist-5c561ed.md).

-   *Update project to use NPM Workspaces \(CAP only\)*

    Optionally update your *CAP* application to support NPM workspaces which will permit the generated SAP Fiori application to maintain and define the *NPM* libraries it needs inside the application and not at the root of the *CAP* project. This is a pre-requisite to adding support for *TypeScript* for SAP Fiori application in a CAP project.

-   *Enable TypeScript \(Experimental\)*

    You can optionally choose to generate your application with *TypeScript* support. This is currently an experimental feature and is subject to future updates to enhance support.

    > ### Note:  
    > *TypeScript* support in a *CAP* application requires *NPM* workspaces to be enabled as detailed above.


