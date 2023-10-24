<!-- loio1c859274b511435ab6bd45f70e7f9af2 -->

# Deployment Configuration



<a name="loio1c859274b511435ab6bd45f70e7f9af2__section_gxy_lqm_ylb"/>

## Configuration Options

In addition to defining parameters in the `ui5.yaml` file, every parameter can also be defined as environment variable that is referenced in `yaml`. Using the `dotenv` module, the task also supports project-specific environment variables defined in the `.env` file in the root of your project. Use the pattern `env:VAR_NAME` to reference an environment variable.



### target

The target object contains properties identifying your target SAP system.

**url**

-   `<string> pattern <protocol>://<hostname>[:<port>]` **\(Required\)**
-   This parameter must contain a url pointing to your target SAP system.

**client**

-   `<number> range [0..999]` **\(Optional\)**
-   The client property is used to identify the SAP client that is to be used in the backend system. It translates to the url parameter`sap-client=<client>`. If the client parameter isn’t provided, the default client is used.

**params \(Optional\)**

-   `<string>` \(optional\)
-   Specifiy addtional query paramaters to pass to the backend deployment `API`. It translates to the url parameter e.g. `sap-language=<2-digit sap language code>`. If the parameter isn’t provided, the backend/user default is used.

**scp**

-   `<boolean>` \(default: `false`\)
-   By default the deployment task uses basic authentication when connecting to the backend. If the target system is ABAP Environment on SAP Business Technology Platform, this parameter needs to be set to `true`.

**service**

-   `<string>` \(default: `/sap/opu/odata/UI5/ABAP_REPOSITORY_SRV`\)
-   Path pointing to the SAPUI5 ABAP repository OData service in your target system. This parameter only needs to be used if the service is exposed at a different path in your backend system, for example, via alias.



### credentials \(optional\)

The credentials object is required for `CI/CD` based deployments and it needs to contain the required parameters to authenticate at your target system. We strongly encourage to not add the credentials directly but use references to environment variables example `env:MY_VARIABLE` here.

For local usage \(not in SAP Business Application Studio\), we do not recommend to use the credentials object at all. As a result, the deployment task utilizes the operating systems secure storage maintain credentials.

**username**

-   `<string>` **\(Required\)**
-   SAP business user for the target system. The user requires authorizations to create/update the target ABAP development object.

**password**

-   `<string>` **\(Required\)**
-   Password required to authenticate the previously configured user. **IMPORTANT**: while technically possible to add the password to your configuration, we strongly **DISCOURAGE** that but recommend instead the use of environment variables.



### app

The app object describes the backend object that is created/updated as result of the deployment.

**name**

-   `<string>` **\(Required\)**
-   Unique name of the application. The name is used as a part of the application url as well as the name of the ABAP development object used as container for the app.

**package**

-   `<string>` **\(Required for new apps\)**
-   Name of an existing ABAP package that is used as parent of the deployed application. The parameter is required for the creation of the application in the backend. Any following deployment updating the application does not require the package parameter, that is ignored .

**transport**

-   `<string>` **\(Optional\)**
-   The transport parameter refers to a transport request number that is used to record changes to the backend application object. The property is optional as it is only needed if the package for deployments requires transport requests.

**description**

-   `<string>` **\(Optional\)**
-   Optional description added to the created application object in the backend.

**exclude**

-   `<string[] array of regex>` **\(Optional\)**
-   By default, the deployment task creates an archive \(zip file\) of all build files and sends it to the backend. By using exclude, you can define expressions to match files that shall not be included into the deployment.

    > ### Note:  
    > `string.match()` is used to evaluate the expressions.


**index**

-   `true|false` **\(Default: `false`\)**
-   If set to `true`, then an additional `index.html` is generated and deployed to run the application standalone.





### Location of MTA Directory

The tool finds the nearest parent directory that contains `mta.yaml` and offers that as the MTA directory. Failing that, it defaults to the parent directory of the application.



### Destination

Destination configured to connect to the backend on Cloud Foundry. If there's a setting in `ui5.yaml`, that value is offered as the default.



### Prefix

Prefix is used for the ID of the MTA and the service names. It defaults to the namespace of the app. If a namespace is not found, it defaults to `test`. Select a prefix so that the service names are unique to your MTA. Otherwise, deployment by multiple people will overwrite the same service. At the end of the generation, it is possible to optionally generate SAP Fiori launchpad configuration \(default: no\).



<a name="loio1c859274b511435ab6bd45f70e7f9af2__section_bxq_gp3_k4b"/>

## \(Optional\): Setting environment variables in an .env file

If you prefer to keep the environment variables in a file, you can create the `.env` file at the root of your project that contains the environment variables to be referenced in the `ui5-deploy.yaml` file.

We recommend that you do not have your actual username and password in the `ui5-deploy.yaml`. In this case, you will be asked to provide these credentials during deployment if needed.

> ### Sample Code:  
> ```
> XYZ_USER=[MY_USER_NAME]
> XYZ_PASSWORD=[MY_PASSWORD]
> ```

