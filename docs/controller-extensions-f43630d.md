<!-- loiof43630d820c64a1cb88a48a0fe7eb1cc -->

# Controller Extensions

Controller extensions allow you to add functionality to a fragment that you add to the SAPUI5 application. You can also override the functionality of the base methods inherited from the source application and lifecycle methods such as `onInit`, `onBeforeRendering`, `onAfterRendering`, and `onExit`.



<a name="loiof43630d820c64a1cb88a48a0fe7eb1cc__context_jns_z13_tdb"/>

## Context

Controller extensions allow you to enhance the functionality of a controller. You can create a controller extension specific to the view, for example, one controller extension for the list report view and one controller extension for the object page view. Additionally, a controller extension can be delivered with an adaptation project and is dynamically added to an existing controller. Controller extensions that an adaptation project delivers are added to the reserved `.extension` namespace of the controller to avoid name clashes with existing functionality.

Controller extensions let the developer add new methods and override methods. These override methods are optional callback methods that override the existing methods using a special override member. For more information on defining an extension, see [Using Controller Extension](https://sapui5.hana.ondemand.com/#/topic/21515f09c0324218bb705b27407f5d61).

> ### Remember:  
> You can add a controller extension only if:
> 
> -   You use an SAP Fiori elements based application or a freestyle SAPUI5 application.
> -   You use application with asynchronous views.



## Procedure

1.  In your workspace, expand the `webapp` folder, right click the `manifest.appdescr_variant` file and click *Open SAPUI5 Visual Editor*.

    The application opens in the canvas in preview mode.

2.  From the Editor Header, click *Edit*.

3.  On the canvas, select a view or element in the view you want to extend and click *Extend with Controller* from the project context menu.

    > ### Tip:  
    > You can use the *Add Controller to Page* quick action to easily add a controller extension on the page level in the list report or object page.

4.  In the dialog box that appears, provide a name for the controller extension.

    The controller extension file \(`.js`\) is created in the folder, *Your project name* \> *webapp* \> *changes* \> *coding*. The `.js` file opens in the editor.

    When you create a controller extension file, an associated `...codeExt.change` file having reference to the `.js` file is created in the folder, *Your project name* \> *webapp* \> *changes*.

    For list report, object page, and overview page applications, in addition to the lifecycle methods, this `.js` file contains new methods that come from the templates provided by Fiori elements. These methods can be used to override the base methods in the applications. For analytical list page applications, the `.js` file contains only the lifecycle methods. Reuse the methods to write extensions.

    > ### Note:  
    > If you need to add your own separate custom business logic files, they have to be located in the `changes/coding` folder. The same folder that is used for the controller extension files. Do not create additional folders for such additional files on upper levels, because it invalidates the project structure and you cannot deploy your application.

5.  Define a method in the controller extension file for the new fragment or override any lifecycle methods in the override section. Save the file.

    The lifecycle methods are defined within the override section. Make sure that you define the new methods outside the override section.

6.  To assign event handlers from .xml fragment to the controller extension, manually associate the methods with the respective fragments. In the `.xml` file for the fragment, prefix the method with <code>.extension.<i class="varname">&lt;controller extension namespace&gt;</i>.</code>, and save the file.

7.  Navigate to the canvas. You are prompted to reload the project for the controller changes to be applied.

    A loading indicator appears with the message: *Loading SAPUI5 Visual Editor with Controller Extension changes*.


**Related Information**  


[Upgrade Safe Compatibility Rules](upgrade-safe-compatibility-rules-53706e2.md "")

