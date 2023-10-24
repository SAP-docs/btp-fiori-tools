<!-- loiod7f20f306af14d34999f56a536f28d47 -->

# Run Control Overview

The **Run** dialog in VS Code as well as in SAP Business Application Studio looks for the file `<workspace_root>/.vscode/launch.json`, but won’t traverse into any subfolders and consequently will not find any configurations in `launch.json` files, that reside in nested folders. It is possible to merge configurations from multiple`launch.json` files by using workspaces. Here is a sample that shows different development environment setups.



<a name="loiod7f20f306af14d34999f56a536f28d47__section_sdc_rwh_fsb"/>

## Example

Assuming the following file system structure:

![](images/RunConfig_Image1_5cfcf01.png)

The `launch.json` files contain the configuration noted next to them: **Config One**, **Config Two**, and**Config Subfolder**. In VS Code you can open a folder in via `File->Open`. Regardless in which environment you open the folder, VS Code or SAP Business Application Studio, depending on which folder you choose, you will get different results.

When opening **Folder\_One**, **Config One** is shown in `Run and Debug` view.

![](images/Runconfiguration_Image2_247b086.png)

![](images/Runconfig_Image3_ad1782a.png)

If you open**Folder Two** the `Run and Debug` view shows **Config Two**.

![](images/Runconfig_image4_7cc5305.png)

> ### Note:  
> The config from Subfolder isn’t shown in this case, as the configuration file `launch.json` can't be found in `<workspace_root>/.vscode`.

When you open **Subfolder** in your development environment, only **Config Subfolder** would be shown.

In addition, you can create a workspace, by opening one of the folders and selecting `Add Folder to Workspace` in your development environment. The workspace could be configured in many ways, here are some examples:

-   **workspace root:** Folder\_One

    Only **Config One** is displayed, same as shown above in Open Folder\_One.

-   **workspace roots**: Folder\_One, Folder\_Two

    ![](images/Runconfig_Image5_7d410a4.png)

    in this case Config One and Config Two are displayed, because these two configurations can be found in `Folder_One/.vscode/launch.json` and `Folder_Two/.vscode/launch.json`

    ![](images/Runconfig_Image6_7fe89a4.png)

-   **workspace roots**: Folder\_One, Folder\_Two, Subfolder

    ![](images/Runconfig_Image7_9d494db.png)

    in this case configurations from all three `launch.json` files are displayed:

    ![](images/Runconfig_Image8_40f2fe8.png)


> ### Note:  
> As seen in the last example, it’s possible to add a subfolder of an existing workspace root folder as stand-alone workspace root.

For more information on run configurations, refer to.[Launch configurations](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) 

**Related Information**  


[Create a New Run Configuration in Visual Studio Code](create-a-new-run-configuration-in-visual-studio-code-3b1f37e.md)

[Create a New Run Configuration in SAP Business Application Studio](create-a-new-run-configuration-in-sap-business-application-studio-05f2a9e.md)

