---
title: Authoring
seo-title: Authoring
description: null
seo-description: Concepts of authoring in AEM
uuid: 1ef5e545-f8ae-4b13-baf5-3a30f373c022
contentOwner: Janice Kendall
products: SG_EXPERIENCEMANAGER/6.4/SITES
topic-tags: introduction
content-type: reference
discoiquuid: d448bcea-0ed1-470d-a603-fa5d6c0146c3
disttype: dist5
gnavtheme: light
isreadyforlocalization: false
jcr-lastmodifiedby: remove-legacypath-6-1
thumbmode: true
index: y
internal: n
snippet: y
---

# Authoring{#authoring}

>[!NOTE]
>
>Authoring by default is performed in the standard, touch-enabled AEM UI, which is the focus of this authoring documentation.
>
>For an explanation of the differences between the standard UI and the classic UI, see [Working with the Author Enviornment](../../../sites/authoring/using/author-environment.md).
>
>If you are looking for authoring documentation for the classic UI, see [Authoring in the Classic UI User Guide](/sites/classic-ui-authoring/user-guide).

## Concept of Authoring (and Publishing) {#concept-of-authoring-and-publishing}

AEM provides you with two environments:

* Author
* Publish

These interact to enable you to make content available on your website - so that your visitors can read it.

The author environment provides the mechanisms for creating, updating and reviewing this content before actually publishing it:

* An author creates and reviews the content (this can be of several types; for example, pages, assets, publications, etc)  
* which will, at some point, be published to your website.

![](assets/chlimage_1-289.png)

On the author environment the functionality of AEM is made available through two UIs. For the publish environment you design the entire look-and-feel of the interface made available to your users.

>[!NOTE]
>
>AEM itself is used to author the AEM documentation. 
>
>Together with the Dispatcher it is also used for publishing.

#### Author Environment {#author-environment}

The author works in what is known as the ** [author environment](../../../sites/authoring/using/author-environment.md)**. This provides an easy to use interface (graphical user interface (GUI or UI)) for creating the content. It is usually located behind a company's firewall that provides full protection and requires the author to login, using an account that has been assigned the appropriate access rights.

>[!NOTE]
>
>Your account needs the appropriate access rights to create, edit or publish content.

Depending on how your instance and your personal access rights are configured you can perform many tasks on your content, including (amongst others):

* generate new content, or edit existing content, on a page
* use predefined templates to create new content pages  
* create, edit and manage your assets and collections
* create, edit and manage your publications  
* develop your campaigns and the related resources
* develop and manage community sites  
* move, copy or delete content pages, assets, etc  
* publish (or unpublish) pages, assets, etc

Additionally, there are administrative tasks that help you manage your content:

* workflows that control how changes are managed; for example. enforcing a review before publication
* projects that coordinate individual tasks

>[!NOTE]
>
>AEM is also [administered](/sites/administering/user-guide) (for a majority of tasks) from the author environment.

#### Publish Environment {#publish-environment}

When ready, the AEM site's content is published to the **publish environment**. Here the website's pages are made available to the intended audience in accordance with the look-and-feel of the designed interface.

Usually, the publish environment is located inside the demilitarized zone; in other words, available to the internet, but no longer under the full protection of the internal network.

When the AEM site is a [community site](../../../communities/using/overview.md), or includes [Communities components](../../../communities/using/author-communities.md), signed-in site visitors (members) may interact with Communities features. For example, they may post to a forum, post a comment, or follow other members. Members may be granted permission to perform activites normally limited to the author environment, such as create new pages (community groups), blog articles, and moderate other members' posts.

<!--
Comment Type: remark
Last Modified By: unknown unknown (ims-author-D9FB647253FD17BE0A4C98A6@AdobeID)
Last Modified Date: 2017-12-04T03:44:39.849-0500
<p>In case I went too far with my edits, below is the original paragraph that I replaced - Note that the change in referencing Communities features should remain. - jkendall</p>
<p> </p>
<p>"When ready, the content is published to the <strong>publish environment</strong>. Here your pages are made available to your intended audience, according to the entire look-and-feel of the interface that you have designed. For a normal internet site, the publish environment is located inside the demilitarized zone; in other words, available to the internet, but no longer under the full protection of your internal network. On the published website visitors can also post comments on the individual pages or interact with the <a href="/sites/authoring/using/author/communities/forum">forums</a>."</p>
-->

<!--
Comment Type: remark
Last Modified By: Alison Heimoz (aheimoz)
Last Modified Date: 2017-12-04T03:44:39.885-0500
<p>following note also on /content/docs/en/cq/6-0/author/page-authoring/publishing-pages.html<br /> </p>
<p>update one....update both</p>
-->

>[!NOTE]
>
>Unfortunately there is sometimes an overlap in the terminology used. This can happen with:
>
>* **Publish / Unpublish** 
>  These are the primary terms for the actions that make your content publicly available on your publish environment (or not).  
>
>* **Activate / Deactivate** 
>  These terms are synonymous with publish/unpublish. They are more common in the classic UI.  
>
>* **Replicate / Replication** 
>  These are the technical terms used to indicate the movement of data (e.g. page content, files, code, user comments) from one environment to another; i.e. when publishing, or reverse-replicating user comments.
>

#### Dispatcher {#dispatcher}

To optimize performance for visitors to your website, the ** [dispatcher](/content/help/en/experience-manager/dispatcher/user-guide)** implements load balancing and caching.