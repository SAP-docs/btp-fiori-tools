<!-- loioa50bc4a67c9e4caebfff4e1ad158796c -->

# Search for a Guide

On the main screen of the guided development extension, you can see a list of available guides. To see a brief description of a feature to implement and its sample preview, expand the respective entry. To get to the guide itself, click *Start Guide* under the description.

Each guide has **categories**, **tags**, and other attributes. A **category** reflects an OData version, template, and annotations type the guide is relevant for. A **Tag** is a kind of metadata assigned to a piece of information in the guides. Both **categories** and **tags** make searching for a guide easier.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_hdm_wzp_jpb"/>

## Group by

The *Group by* list changes how the guides are grouped in the list based on their categories.

-   **Page Type** refers to the page or template. Some features can be applied to different page types, and such guides are displayed under all categories that they’re relevant for.

    When a guide available for multiple page types is selected, only the guide relevant to the page type of the current project is highlighted.

-   **OData version** refers to the OData service version for which the guide steps are relevant. If a selected guide isn’t currently available for a given OData version, a warning message appears.

    Some features are available for both V2 and V4 OData versions and the guides for these features display under both categories. The instructions in such guides could be different for `OData V4` and `OData V2`. In such cases, you can find a guide relevant to your OData version by looking for the right category.

-   **Application Artifacts** refers to the type of change the guide describes. The options include manifest change, flex change, and annotations.

Annotations-specific guides are further grouped into three categories: XML Annotations, CDS Annotations, and ABAP CDS Annotations.

For features that can be implemented via different annotation types \(depending on what is applicable your project\); guides may display under multiple categories. For example, a guide may appear under both the XML Annotations and CDS Annotations categories if variants for the two different annotation types exist. The parameters and code snippets will differ depending on which guide variant is opened.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_o4h_yzp_jpb"/>

## View

By default, only the guides that are relevant to the current project are displayed. This ensures that code inserted into your project is appropriate for the project's template, OData version, and UI5 version.

Using the *View* filter, you can see all the guides available in guided development.

To start working with the *View* filter, perform the following steps:

1.  Select a project from the *Project* dropdown list in the upper-left corner.
2.  In the *View* dropdown list, pick from the following options:
    -   *All Guides*. This option displays the list of all the guides in guided development.

        > ### Note:  
        > When *All Guides* are selected, the updated list of guides appears with the information icon and message similar to the following:
        > 
        > `Not all guides are applicable to [project name]. Click here to see all project guides.`
        > 
        > Click the provided link to switch to the *Project Guides* list.

        The guides that aren’t relevant to the current project are indicated by a warning symbol next to the guide title. After you open the guide, the following warning message can be viewed:

        `This guide isn’t compatible with the current project and will not work as intended.`

    -   *Project Guides*. This option displays only those guides that apply to the current project.

3.  Click the guide applicable to your project and follow its steps to modify your application.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_anm_b1q_jpb"/>

## Filter

The *Filter* ![Filter Icon](images/FilterIcon_d3d5f5a.png) icon next to the *View* list allows you to select one or more predefined tags assigned to the guides. The guide list is then narrowed down to show only those guides that have all selected tags.



<a name="loioa50bc4a67c9e4caebfff4e1ad158796c__section_qp1_c1q_jpb"/>

## Search guides

The *Search guides* field allows you to enter free text to search for a specific term in all the guides content, including titles, descriptions, steps, and code snippets. For example, if you look for all the guides that are relevant to the `UI.LineItem` annotation, you can type in the search term and narrow it down to the list of guides using this annotation term. The search works on *as you type* principle, so each successive character entered filters the list further.

