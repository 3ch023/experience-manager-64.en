---
title: Authoring in-context help for form fields
seo-title: Authoring in-context help for form fields
description: null
seo-description: AEM Forms allows you to add in-context help to adaptive form fields and panels, as text or rich media, including videos. 
uuid: d6dc7944-c62f-4790-8ea7-24340fc2160e
acrolinxdate: 2016-05-31T06 34 07.976-0400
acrolinxlastcheckedby: vishgupt
acrolinxpagestatus: red
acrolinxreporturl: http //checkstyle.corp.adobe.com 8031/output/en/authoring_in_field_help_admin_5e12de0b318c6865_1963_report.xml
acrolinxsentences: 21
acrolinxwords: 430
products: SG_EXPERIENCEMANAGER/6.4/FORMS
topic-tags: author
discoiquuid: 96c5fcaf-4e8b-433b-9675-9e67a4cf0165
isreadyforlocalization: false
lastpublishqadate: 2015-06-12T04 24 46.698-0400
index: y
internal: n
snippet: y
---

# Authoring in-context help for form fields{#authoring-in-context-help-for-form-fields}

## Introduction {#introduction}

There are situations when end users filling a form are not sure how to fill details in a particular form field. To address such issues, adaptive forms provides support to add text or rich in-context help to a form field. It helps improve the form filling experience and avoids any ambiguity for end users.

This article discusses how form authors can add in-context help while authoring Adaptive Forms.

## Add in-context help {#add-in-context-help}

You can specify in-context help using the following options in the Help Content section of the properties tab in the sidebar.

* [Short description](../../forms/using/authoring-in-field-help.md#main-pars-header-1)
* [Long description](../../forms/using/authoring-in-field-help.md#main-pars-header-2)

![In-context help for form fields](assets/descriptions.png)

>[!NOTE]
>
>Long description overrides the Short description. If you have specified both, only Long description will appear.

### Short description {#short-description}

The Short description field is to provide quick and short hints about filling a form field. The text specified in the Short description field is displayed as a tooltip on hovering mouse over the field.

![Short description for adding in-context help for form fields](assets/tooltip.png)

>[!NOTE]
>
>Select **Always show short description** to permanently display the help text below the field.

![Permanent short in-context help below the field](assets/short1.png)

### Long description {#long-description}

You can use the Long description field to specify long text or embed rich media content, including videos, as in-context help. For example, the following image shows how you can embed a video as in-context help.

![Adding rich media as in-context help for form fields](assets/long-descriptions.png)

Adding Long description displays a **?** icon next to the field. Clicking the icon displays the content added in the long description section.

![Example of rich media in-context help](assets/photoshop.png)

### Panel-level help {#panel-level-help}

In addition to the in-context help for form fields, you can specify help at a panel level in the Help content tab of the panel edit dialog.

![Adding in-context help for a form panel](assets/panel-level-help.png)

Adding help for panel displays a **?** icon next to the panel description. Clicking the icon displays the content added in the Help Content section of the panel edit dialog.

![Example of in-context help at form panel level](assets/photoshop-1.png)
>[!MORE_LIKE_THIS]
>
>* [Introduction to forms authoring](../../forms/using/introduction-forms-authoring.md)
>* [Creating an Adaptive Form](../../forms/using/creating-adaptive-form.md)