---
title: Tips for minimizing database growth
seo-title: Tips for minimizing database growth
description: null
seo-description: Long-lived processes store process data in the AEM forms database. The growth of the AEM forms database can be minimized using a few easy process design and product configuration strategies.
uuid: a1942d2c-e434-421d-ae1c-e573698349e5
acrolinxdate: 2016-05-31T07 03 39.581-0400
acrolinxlastcheckedby: vishgupt
acrolinxpagestatus: yellow
acrolinxreporturl: http //checkstyle.corp.adobe.com 8031/output/en/tips_minimizing_database_growth_admin_5e12de0b318c6865_2382_report.xml
acrolinxsentences: 24
acrolinxwords: 383
contentOwner: admin
content-type: reference
geptopics: SG_AEMFORMS/categories/maintaining_the_aem_forms_database
products: SG_EXPERIENCEMANAGER/6.4/FORMS
discoiquuid: 354086c9-5304-49f3-b5c3-12de3b5624be
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Tips for minimizing database growth{#tips-for-minimizing-database-growth}

Long-lived processes store process data in the AEM forms database. The growth of the AEM forms database can be minimized using a few easy process design and product configuration strategies.

## Process design tips {#process-design-tips}

Use short-lived processes whenever possible. Short-lived processes do not store process data in the database. The disadvantage of using short-lived processes is that their status and state are not tracked in administration console and there is no history of the process.

Some service operations, such as the Assign Task operation (User service), require that they are used in long-lived processes. In this case, you can segment the process into several subprocesses and make them short-lived when possible. If you use this strategy, short-lived subprocesses should handle large data items, such as document values.

Use variables sparingly. When using long-lived processes, for every process instance, space is allocated on the database for each variable in the process. Strategic use of variables can save a considerable amount of space. For example, you can overwrite variable values when old values are no longer needed in the process. And delete any variables that you have created and are not using. You can validate the process to find unused variables.

Use simple variable types (for example, string or int) and avoid using complex variable types when possible. Database space is allocated for variables even when they do not contain a value. Complex variables typically require more space than simple ones.

## Product administration tips {#product-administration-tips}

Use global document storage (GDS) effectively. The GDS directory on the forms server is used to store, among other things, files that are passed to services that are part of AEM forms in processes. To improve performance, smaller documents are instead stored in-memory and persisted in the database.

administration console exposes the Default Document Max Inline Size property for configuring the maximum size of documents that are stored in-memory and persisted in the database. (See [Configure general AEM forms settings](../../../forms/using/admin-help/configure-general-aem-forms-settings.md#configure-general-aem-forms-settings).) If you set this property to a low value, most documents are persisted in the GDS directory instead of in the database. The advantage is that you can more easily delete the files when they are no longer needed when they are stored in the GDS directory.