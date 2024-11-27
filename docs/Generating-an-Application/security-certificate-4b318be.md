<!-- loio4b318bede7eb4021a8be385c46c74045 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Security Certificate

During application generation, invalid security certificate errors may occur when the system the user is connected to is using SSL to support secure HTTPS traffic. In some cases, the certificate is generated using a local certificate authority that is unknown to the user operating system. If this happens, the SAP Fiori application generator will by default reject the connection request and report an error. We recommend that you fix this error by installing the required certificates using the instructions below. You can optionally choose to ignore the error and continue generation with the invalid certificate \(not recommended\).

> ### Tip:  
> Please ensure you have Node.js installed locally. For more information, see [Visual Studio Code](../Getting-Started-with-SAP-Fiori-Tools/visual-studio-code-17efa21.md#loio17efa217f7f34a9eba53d7b209ca4280).

> ### Note:  
> The instructions below are applicable where the security certificate is valid, but using a local certificate authority that is unknown to the operating system. If the SSL cert is invalid such as an expired cert, wrong host or unable to verify leaf signature, please contact your administrator. In these cases, they cannot be resolved by SAP Fiori tools.

1.  Ensure that you have a copy of the local certificate authority saved locally.

    > ### Note:  
    > Create a folder or select a folder that can permanently keep your downloaded certificate. To export the certificate from your browser, follow the instructions based on your web browser and its version.

2.  Once the certificate file is downloaded, the issue can be resolved for VS Code by importing it into your global certificate store. To do so, perform the following steps:
    -   Microsoft Windows

        -   Right-click the *CA certificate* file and select *Install Certificate*.

        -   Follow the prompts to add the certificate to the trust store either for the current user only or for all users logging onto this computer.

    -   macOS.
        -   Right-click the *CA certificate* file.

        -   Select *Open With* and naviagte to *Keychain Access*.

        -   Select *System* as the keychain to import into.


3.  To resolve the issue for using the command line with Yeoman, set the following environment variable to point to the location of the downloaded certificate file: `NODE_EXTRA_CA_CERTS`
    -   Microsoft Windows:

        -   Right-click the :desktop_computer: \(*Computer*\) icon and select *Properties*. Alternatively, in Windows Control Panel, select *System*.
            -   Microsoft Windows 10
                -   Right-click*Windows Start Button* and select *System*.
                -   In *System Settings* under *Related Settings*, select *System info*.


            -   Select *Advanced system settings*.
            -   On the Advanced tab, select *Environment Variables*.
            -   Click *New* to create a new environment variable.
            -   Add `NODE_EXTRA_CA_CERTS` and ensure the value points to the downloaded certificate file that is stored in the folder from **Step 1**.
            -   Click *Apply* and then *OK* for the changes to take effect.


        macOS

        -   In the command-line terminal, before executing the Yeoman command to run the generators, execute the following command:

            `export NODE_EXTRA_CA_CERTS=path/to/certificate/file`

            Replace `path/to/certificate/file` with the location of the downloaded certificate.




