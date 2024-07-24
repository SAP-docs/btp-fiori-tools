<!-- loio7c755a5e7f914c2f816e5a6e28cf377c -->

# Report Issues and Security



-   See the  <?sap-ot O2O class="- topic/xref " href="160b4d8c680c463daf20c7399e2dc6ad.xml" text="SAP Fiori tools FAQs" desc="" xtrc="xref:1" xtrf="file:/home/builder/src/dita-all/dkl1587758022827/loio042b51923fc64122ac4c1627fb4b42c2_en-US/src/content/localization/en-us/7c755a5e7f914c2f816e5a6e28cf377c.xml" output-class="" outputTopicFile="file:/home/builder/tp.net.sf.dita-ot/2.3/plugins/com.elovirta.dita.markdown_1.3.0/xsl/dita2markdownImpl.xsl" ?>  to get up-to-date information.
-   Check the [SAP Fiori tools Community](https://help.sap.com/viewer/disclaimer-for-links?q=https://answers.sap.com/tags/73555000100800002345).
-   If you can't find an answer in **SAP Community** or need additional assistance, create an incident in **SAP Support Portal** under component: **CA-UX-IDE**. See [Contact SAP Support](https://help.sap.com/viewer/1bb01966b27a429ebf62fa2e45354fea/Latest/en-US/5b5d9dc53aac46b69caebb95c1a242eb.html "") :arrow_upper_right:.



<a name="loio7c755a5e7f914c2f816e5a6e28cf377c__section_rqh_4nm_ylb"/>

## Security

The following best practices are suggested when using SAP Fiori tools:

-   Follow the software development security guidance provided by your organization.
-   Avoid using **OData services** hosted on a production system for developing an SAP Fiori application.
-   Don't use the same user credentials to access development and production systems for the OData service.
-   Use a trusted NPM registry.
-   Follow the security guidelines for the required software you are using.
-   Ensure that you use a source control system and are regularly committing code to it.
-   Ensure that you verify the content of your PATH variable. Commands like `node` or `cds`, which are usually part of the PATH variable and which can be executed from any directory in the terminal, need to point to a trusted origin.

-   For more information about security, see [Security](../Deploying-an-Application/security-8a147c6.md).

**Related Information**  


[SAP Fiori tools FAQ](https://help.sap.com/viewer/42532dbd1ebb434a80506113970f96e9/Latest/en-US)

[SAP Fiori tools Community](https://answers.sap.com/tags/73555000100800002345)

[Contact SAP Support](https://help.sap.com/viewer/1bb01966b27a429ebf62fa2e45354fea/Latest/en-US)

