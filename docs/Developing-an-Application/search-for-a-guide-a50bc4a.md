<!-- loioa50bc4a67c9e4caebfff4e1ad158796c -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Search for a Guide

You can find the list of available guides in guided development. Click on a guide to see a description and sample preview. To launch the guide, click *Start Guide*.

Each guide has categories, tags, and other attributes. A category reflects the OData version, template, and annotations type, the guide is relevant for. A tag is a type of metadata assigned to a piece of information in an guide. Both categories and tags make searching for guides easier.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_hdm_wzp_jpb"/>

## Group by

The *Group by* dropdown defines how the guides are grouped based on their categories.

-   *Page Type* refers to the page or template type. Some features can be applied to different page types, and such guides are displayed under all the categories they are relevant for.

    When a guide available for multiple page types is selected, only the guide relevant to the page type of the current project is highlighted.

-   *OData Version* refers to the OData service version for which the guide steps are relevant. If the selected guide is not currently available for a given OData version, a warning message appears.

    > ### Tip:  
    > Some guides are available for both `OData V2` and `OData V4` versions but the instructions can differ.

-   *Application Artifacts* refers to the type of change the guide describes. The options are Manifest Change, Flex Change, and Annotations.

Annotations-specific guides are further grouped into three categories: XML Annotation, CAP CDS Annotation, and ABAP CDS Annotation.

> ### Tip:  
> Some guides are available for multiple annotation types but the parameters and code snippets differ.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_o4h_yzp_jpb"/>

## View

By default, only the guides that are relevant to the current project are displayed. This ensures that code inserted into your project is appropriate for the project's template, OData version, and SAPUI5 version.

Using the *View* filter, you can see all the guides available in guided development.

To use the *View* filter, perform the following steps:

1.  Select a project from the *Project* dropdown.
2.  In the *View* dropdown, choose from the following options:
    -   *All Guides* - displays the list of all the guides in guided development.

        > ### Note:  
        > When *All Guides* is selected, the updated list of guides appears with the <span class="SAP-icons-V5"></span> \(*Information*\) icon and message:
        > 
        > `Not all guides are applicable to [project name]. Click here to see all project guides.`
        > 
        > Click the provided link to switch to the *Project Guides* list.

        The guides that aren’t relevant to the current project are indicated by a warning symbol next to the guide title. After you open the guide, the following warning message appears:

        `This guide isn’t compatible with the current project and will not work as intended.`

    -   *Project Guides* - displays only the guides that apply to the current project.

3.  Click the guide applicable to your project and follow its steps to modify your application.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_anm_b1q_jpb"/>

## Filter

The <span class="SAP-icons-V5"></span> \(*Filter*\) icon allows you to select one or more predefined tags assigned to the guides. The guide list is then narrowed down to show only those guides that have all the selected tags.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_qp1_c1q_jpb"/>

## Search guides

The *Search guides* field allows you to search for a specific term, which includes titles, descriptions, annotation terms, and information links, to filter the list of guides. For example, if you want to find all the guides that are relevant to the `UI.LineItem` annotation, you can type in the search term and narrow it down to the list of guides using this annotation term. The search works as you type, so each successive character entered filters the list further.

