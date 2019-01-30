---
title: Selecting your UI
seo-title: Selecting your UI
description: null
seo-description: For convenience to authoring users, the touch-enabled UI does allow for switching to the classic UI when necessary.
uuid: fccfb8ce-e47b-452b-b9c8-084a5296e4f5
contentOwner: Chris Bohnert
products: SG_EXPERIENCEMANAGER/6.4/SITES
topic-tags: introduction
content-type: reference
discoiquuid: a0911003-21e0-41ba-afa7-7a38bdddaea4
isreadyforlocalization: false
jcr-lastmodifiedby: remove-legacypath-6-1
index: y
internal: n
snippet: y
---

# Selecting your UI{#selecting-your-ui}

Since the touch-optimized UI is designed to supersede the classic UI, the user or administrator of the AEM instance must make an active decision to continue using the classic UI. Because the classic UI is no longer maintained, there is no way for the authoring user to simply switch from the classic UI to the equivalent in the touch-optimized UI.

For convenience to authoring users, the touch-optimized UI does allow for switching to the classic UI when necessary. See the [Selecting your UI](../../../sites/authoring/using/select-ui.md) in the standard Authoring documentation for details.

>[!NOTE]
>
>Instances upgraded from a previous version will retain the classic UI for page authoring.
>
>After upgrade, page authoring will not be automatically switched to the touch-optimized UI, but you can configure this using the the [OSGi configuration](../../../sites/deploying/using/configuring-osgi.md) of the **WCM Authoring UI Mode Service** ( `AuthoringUIMode` service). See [UI Overrides for the Editor](#uioverridesfortheeditor).

### Configuring the Default UI for Your Instance {#configuring-the-default-ui-for-your-instance}

A system administrator can configure the UI that is seen at startup and login by using [Root Mapping](../../../sites/deploying/using/osgi-configuration-settings.md#daycqrootmapping).

This can be overridden by user defaults or session settings.