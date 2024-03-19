<!-- loioad7b4ae4bc7249e4b9cc5625bc978ab9 -->

# Controller Extensions



<a name="loioad7b4ae4bc7249e4b9cc5625bc978ab9__context_jns_z13_tdb"/>

## Context

Controller extensions allow you to enhance the functionality of a controller. You can create a controller extension specific to the view, for example, one controller extension for the list report view and one controller extension for the object page view. Additionally a controller extension can be delivered with an adaptation project and is dynamically added to an existing controller. Controller extensions that an adaptation project delivers are added to the reserved ".extension" namespace of the controller to avoid name clashes with existing functionality.

Controller extensions let the developer to add new methods and override methods. These override methods are optional callback methods that override the existing methods using a special override member. For more information on defining an extension, see [SAPUI5 Documentation](https://sapui5.hana.ondemand.com/#/topic/21515f09c0324218bb705b27407f5d61).

> ### Remember:  
> You can add a controller extension only if:
> 
> -   You use an SAP Fiori elements-based application, or a freestyle SAPUI5 application.
> -   You use application with asynchronous views.



## Procedure

1.  Right-click on the project main folder, the `webapp` folder, or the`manifest.appdescr_variant` file and choose *Preview Application*. Choose *start-editor*.

    The application opens in the canvas in UI Adaptation mode.

2.  On the canvas, select a view or element in the view you want to extend and choose *Extend with Controller* from the project context menu.

3.  In the dialog box that appears, provide a name for the controller extension.

    The controller extension file \(`.js`\) is created in the folder, *Your project name* \> *webapp* \> *changes* \> *coding*. The `.js` file opens in the editor.

    When you create a controller extension file, an associated **controllerExtension.change** file having reference to the `.js` file is created in the folder, *Your project name* \> *webapp* \> *changes*.

    For list report, object page, and over view page applications, in addition to the lifecycle methods, this `.js` file contains new methods that come from the templates provided by SAP Fiori elements. These methods can be used to override the base methods in the applications. For analytical list page applications, the `.js` file contains only the lifecycle methods. Reuse the methods to write extensions.

    > ### Note:  
    > If you need to add your own separate custom business logic files, they have to be located in the folder `changes/coding`, the same folder that is used for the controller extension files. You should not create additional folders for such additional files on upper levels, because it will invalidate the project structure and you will not be able to deploy.

4.  Define a method in the controller extension file for the new fragment or override any lifecycle methods in the override section. Save the file.

    The lifecycle methods are defined within the override section. Make sure that you define the new methods outside the override section.

5.  To assign event handlers from .xml fragment to the controller extension, manually associate the methods with the respective fragments. In the .xml file for the fragment, prefix the method with <code>.extension.<i class="varname">&lt;controller extension namespace&gt;</i>.</code>, and save the file.

6.  In order to load the added change you need to reload the browser tab in which the adaptation project editor is opened. If you have opened Preview of the application in a separate browser tab, it also needs to be refreshed.


