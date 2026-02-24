<!-- loio8182ff3b19574f038bd636b9991aa24e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Managing Service and Annotation Files

SAP Fiori elements applications use OData services to expose data and functionality from the back end. These services often contain annotations that specify how data is to be displayed and how it behaves.

SAP Fiori tools uses a local copy of the OData service metadata and annotations as a basis for visualizing the application structure. It is also used for adding or modifying UI features and previewing your application. This local metadata copy is saved in the project when the application is generated.

OData V4 services that come from RAP back ends often do not contain metadata for value help directly. They reference additional metadata files that contain value list information using the `Common.ValueListReferences` annotation. The local copies of these metadata files can be retrieved and stored in the project along with the main service of the application.

If OData services or any associated annotations have been modified in the back end after the project was generated, these changes are not automatically applied to the local copy. This can result in discrepancies between SAP Fiori tools and the application runtime. For example, if a new property was added in the back end, you cannot use it in Application Modeler until you refresh the service. If this property was already used in a back-end annotation, Application Modeler and Annotation LSP cannot find it in the local copy and errors or warnings are displayed. To avoid these errors and ensure Application Modeler can access new properties, always synchronize the local copy with the service metadata after making changes in the back end.



<a name="loio8182ff3b19574f038bd636b9991aa24e__section_khb_j3p_ylb"/>

## Manage Service Files

> ### Note:  
> The ability to add, refresh, and delete services is only supported for the SAP Fiori elements list report page, analytical list report page, and overview page floorplans and freestyle SAPUI5 projects.



### Add Services to a Project

1.  Right-click the `manifest.json` file for your application.
2.  Click *Service Manager*.
3.  Click *Add Service*.
4.  Choose Connection Type:
    1.  Destination \(SAP Business Application Studio\) - Select the server destination from the dropdown. Enter your username and password, if needed.
    2.  SAP System \(Visual Studio Code\) - Select the server SAP System from the dropdown. Enter your username and password, if needed.
    3.  Hostname - Enter the server hostname, SAP Client, and username and password, if needed.

5.  To specify the OData service URL:
    1.  Enter the Service URL manually.
    2.  Fetch Services from the server catalog and select from the dropdown list.

6.  Click *Add*.

    A new service appears in a service list. A service`metadata.xml` is added to a local service folder of the project along with the service back-end annotations, if available.




### Refresh a Service from the Server

1.  Right-click the `manifest.json` file for your application.
2.  Click *Service Manager*.
3.  Click the :pencil2: \(*Pencil*\) icon opposite the service.
4.  Choose a *Connection Type*:
    1.  Destination \(SAP Business Application Studio\) - Select the server destination from the dropdown. Enter your username and password, if needed.
    2.  SAP System \(Visual Studio Code\) - Select the server SAP System from the dropdown. Enter your username and password, if needed.
    3.  Hostname - Enter the server hostname, SAP Client, and username and password, if needed.

5.  Click
    -   *Refresh* - Refresh the local copy of service metadata and annotation files. Use *Refresh* to just refresh the service.
    -   *Refresh & Save* - Refresh the local copy of service metadata and annotation files and save any changes to the UI5 `YAML` files. For more information on UI5 `YAML` files, see [UI5 CLI - Configuration](https://ui5.github.io/cli/stable/pages/Configuration/). Use *Refresh & Save* to refresh the service and save any changes to the UI5 `YAML` files.


> ### Note:  
> If the project is generated based on an OData V4 service from a RAP back end, it may also contain local copies of metadata files from value list services. You can choose to download or refresh this metadata when refreshing the service.



### Delete a Service:

1.  Right-click the `manifest.json` for your application.
2.  Click *Service Manager*.
3.  Click the :wastebasket: \(*Delete*\) icon.

The `metadata.xml`, related annotation XML files and mockdata is deleted from the project. Also, the `ui5*.yaml` files remove any back-end routing and mockserver entries specific to the service being deleted.

For more information about mockserver, see [Use Mock Data](../Previewing-an-Application/use-mock-data-bda83a4.md).



<a name="loio8182ff3b19574f038bd636b9991aa24e__section_sl5_xd4_ylb"/>

## Manage OData Annotations Files

OData services can have multiple local annotation files associated with a service. The Annotation File Manager can be used to manage local annotation files associated with a service.

> ### Note:  
> Managing annotations is limited to the OData service and not applicable to CAP CDS.

**Open the Annotation File Manager**

1.  Right-click the `manifest.json` file for your project.
2.  Click *Annotation File Manager*.
3.  Select the target service from the dropdown.

Alternatively, you can click *Annotation Hierarchy* in the **Annotation List View** for a particular projection or property of service.



### Add Annotation Files:

1.  Right-click the `manifest.json` file for your project.
2.  Click *Annotation File Manager*.
3.  Select the target service from the dropdown.
4.  Click *Create Local Annotation File*.
5.  Fill in the criteria required for creating an annotation file.
6.  Click *Create*.

The newly created annotation file appears in the *Annotation File Manager* for that service, and also in the *Annotation List View* for the target projection.



### Change the Hierarchy of a Local Annotation File

> ### Note:  
> The highest-ranked annotation file in the *Annotation File Manager* table is at the bottom which mimics the precedence rules in the `manifest.json` file.

1.  In the *Annotation File Hierarchy*, use the <span class="SAP-icons-V5"></span>\(*Move Up*\) and <span class="SAP-icons-V5"></span> \(*Move Down*\) icons to change the order of the files.

![Annotation File Hierarchy](images/Annotations_File_Hierarchy_a7d0242.png)



### Activate and Deactivate Local Annotation Files

1.  Right-click the `manifest.json` file and click *Open Annotation File Manager*.
2.  Select or clear the checkbox in the active column of the *Annotation File Manager* table to activate or deactivate the annotation.

    > ### Note:  
    > When a file is deactivated, it is no longer considered a part of the annotation file hierarchy.




### Delete an Annotation File

1.  Select the active checkbox.
2.  Click the :wastebasket: \(*Delete*\) icon next to the annotation file.

