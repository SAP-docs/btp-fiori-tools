<!-- loio2386ce830706482ba134b7d92315db5a -->

# Deleting RAP Artifacts Manually

Learn how to manually delete a RAP-based application and its related back-end artifacts from an ABAP system using ABAP Development Tools \(ADT\).



## Prerequisites

-   You use ABAP Development Tools \(ADT\).
-   You have access to the relevant ABAP package.
-   You have unpublished the service if it is published.



## Deleting RAP Artifacts

RAP services have a defined dependency chain. To avoid activation errors and broken references, artifacts must be deleted in the following order:

1.  Service Binding
2.  Service Definition
3.  Access Controls
4.  Behavior Definition
5.  CDS Data Definition \(Entity and View\)
6.  Dictionary Database Tables
7.  SAP Object Node Types and Object Types \(if applicable\)
8.  Behavior Implementation Classes
9.  Authorization Defaults

After deletion, activate the package and verify that the OData service is inaccessible and the application no longer appears in catalogues or roles.

