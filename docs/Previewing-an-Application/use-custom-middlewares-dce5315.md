<!-- loiodce5315a26964ba59d9f3e7f827dceca -->

# Use Custom Middlewares

You can plug custom middleware implementations into the internal express server of the SAPUI5 Server module if you want to handle requests differently. For example, add various headers to a response or parse data of a POST request in a specific way.

SAP Fiori tools use the capabilities of custom middlewares to start and preview SAP Fiori elements applications:

-   [Application reload](use-custom-middlewares-dce5315.md#loiodce5315a26964ba59d9f3e7f827dceca__section_xvv_51q_x4b). The middleware to reload the application automatically in the browser, when any change is done.
-   [Proxy](use-custom-middlewares-dce5315.md#loiodce5315a26964ba59d9f3e7f827dceca__section_uxj_55w_x4b). The middleware to connect to the backend server side and to load the remote SAPUI5 resources.
-   [Serve static](use-custom-middlewares-dce5315.md#loiodce5315a26964ba59d9f3e7f827dceca__section_xty_5vw_x4b). The middleware to serve local resources from your workspace, such as the reuse libraries.



<a name="loiodce5315a26964ba59d9f3e7f827dceca__section_xvv_51q_x4b"/>

## Application Reload Middleware

With the application reload middleware, developers can preview SAP Fiori elements applications while developing or configuring them. Whenever a file relevant for SAP Fiori elements is changed, the application reload middleware will refresh the application preview.



### Example Configuration

To start the application reload middleware with its default settings, execute `npx fiori run` in your project with the configuration below in the `ui5.yaml` file.

```
server:
  customMiddleware:
  - name: fiori-tools-appreload
    afterMiddleware: compression
```



### Configuration options

The application reload middleware does not require any configuration parameters. However, there are optional parameters that can be used if the project structure differs from the standard SAP Fiori elements projects.

**Configuration parameters**


<table>
<tr>
<th valign="top">

Parameter

</th>
<th valign="top">

Type

</th>
<th valign="top">

Default value

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

path

</td>
<td valign="top">

`<string>`

</td>
<td valign="top">

`webapp`

</td>
<td valign="top">

Path to be watched. By default, the standard SAPUI5 `webapp` folder is used.

</td>
</tr>
<tr>
<td valign="top">

ext

</td>
<td valign="top">

`<string>`

</td>
<td valign="top">

`html, js, json, xml, properties, change`

</td>
<td valign="top">

Change this parameter to select a custom set of file extensions that are to be watched.

</td>
</tr>
<tr>
<td valign="top">

port

</td>
<td valign="top">

`<int>`

</td>
<td valign="top">

`35729`

</td>
<td valign="top">

Port to be used to communicate file system changes.

</td>
</tr>
<tr>
<td valign="top">

debug

</td>
<td valign="top">

`<boolean>`

</td>
<td valign="top">

`false`

</td>
<td valign="top">

Set this parameter to get more log information.

</td>
</tr>
</table>



<a name="loiodce5315a26964ba59d9f3e7f827dceca__section_uxj_55w_x4b"/>

## Proxy

The proxy middleware provides you with the capabilities to connect to different backend systems or to switch the SAPUI5 version of the application.



### Configuration Examples

-   **Connect to a backend system**

    To forward any request starting with the `path` parameter to the provided backend `url`, execute `npx fiori run` in your project with the configuration below in the `ui5.yaml` file.

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /sap
          url: https://my.backend.com:1234
    ```

-   **Connect to a backend system with destination**

    If you use a destination to connect to your backend system, you can also provide the `destination` in the configuration.

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /sap
          url: https://my.backend.com:1234
          destination: my_backend
    ```

-   **Connect to multiple backend systems**

    Additionally, you can connect to multiple backend systems as follows:

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /northwind
          url: https://my.backend_2.com:1234
        - path: /sap
          url: https://my.backend.com:1234
    ```

-   **Connect to an ABAP Environment on SAP Business Technology Platform**

    If you want to connect to an ABAP Environment on SAP Business Technology Platform, you need to set the optional property `scp` to `true`. For any other target, remove this property or set it to `false`.

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /sap
          url: https://my.steampunk.com:1234
          scp: true
    ```

-   **Connect to the SAP Business Accelerator Hub**

    If you want to connect to the SAP Business Accelerator Hub, you need to set the optional property `apiHub` to `true`, and set the corresponding `path` and `url`.

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /s4hanacloud
          url: https://api.sap.com
          apiHub: true
    ```

-   **Proxy WebSockets**

    If you want the proxy to handle WebSockets, then you need to set the optional property `ws` to `true`.

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /sap
          url: https://my.backend.com:1234
          ws: true
    ```

-   **Change the path to which a request is proxied**

    It is possible to configure the proxy to send requests from a certain path `/services/odata` to a destination with a specified entry path `/my/entry/path`. To do so, use the following configuration:

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        backend:
        - path: /services/odata
          pathPrefix: /my/entry/path
          url: https://my.backend.com:1234
          destination: my_backend
    ```

-   **SAPUI5**

    By using the proxy configuration, the user can also change the SAPUI5 version, which is used to preview the application. The initial SAPUI5 configuration for the proxy is created along with the application generation. See the following example:

    ```
    - name: fiori-tools-proxy
      afterMiddleware: compression
      configuration:
        ui5:
          path:
          - /resources
          - /test-resources
          url: https://sapui5.hana.ondemand.com
          version: 1.78.0
    ```

    By using the `version` parameter, the user can select the SAPUI5 version which is used when `npx fiori run` is executed.




<a name="loiodce5315a26964ba59d9f3e7f827dceca__section_xty_5vw_x4b"/>

## Serve Static

The serve static middleware provides the capability to serve any static resources locally from your machine. For example, you can serve SAPUI5 locally or any other resources.



### Example Configuration for serving locally SAPUI5

**Prerequisites**

SAPUI5 SDK version is downloaded and extracted locally on your computer. You can download the SAPUI5 sources from the [SAP Development Tools](https://tools.hana.ondemand.com/#sapui5) page.

If you want to serve the SAPUI5 resources from your computer, execute `npx fiori run` in your project with the configuration below in the `ui5.yaml` file. Any request starting with the `path` parameter is forwarded to the local path provided in the `src` parameter.

```
server:
  customMiddleware:
  - name: fiori-tools-servestatic
    afterMiddleware: compression
    configuration:
      paths:
        - path: /resources
          src: "Path/To/SAPUI5-SDK"
        - path: /test-resources
          src: "Path/To/SAPUI5-SDK"
```



### Example Configuration for serving any resources locally

If you want to serve any resources from your computer, execute `npx fiori run` in your project with the configuration below in the `ui5.yaml` file. Any request starting with the `path` parameter is forwarded to the local path provided in the `src` parameter.

```
server:
  customMiddleware:
  - name: fiori-tools-servestatic
    afterMiddleware: compression
    configuration:
      paths:
        - path: /images
          src: "Path/To/images"
        - path: /libs
          src: "Path/To/libs"
```

