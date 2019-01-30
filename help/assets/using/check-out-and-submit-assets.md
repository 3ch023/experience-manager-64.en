---
title: Check In and Check Out Files in Assets
seo-title: Check In and Check Out Files in Assets
description: null
seo-description: Learn how to check out assets for editing and check them back in after the changes are complete.
uuid: 379240ba-cbdc-4bb8-bd3c-1cf388de45ca
acrolinxdate: 2019-01-12T17 26 40.099-0500
acrolinxlastcheckedby: asgupta
acrolinxpagestatus: yellow
acrolinxreporturl: http //acrolinx.corp.adobe.com 8031/output/en/check_out_and_submit_assets_krs_workflow_f3c2f2ccebf6138e_110_report.xml
acrolinxsentences: 32
acrolinxwords: 393
contentOwner: User
products: SG_EXPERIENCEMANAGER/6.4/ASSETS
topic-tags: managing-assets
content-type: reference
discoiquuid: a371c138-04e4-463c-9a45-4803fa724ebd
disttype: dist5
gnavtheme: light
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Check In and Check Out Files in Assets{#check-in-and-check-out-files-in-assets}

Adobe Experience Manager (AEM) Assets lets you check out assets for editing and check them back in after you complete making the changes. After you check out an asset, only you can edit, annotate, publish, move, or delete the asset. Checking out an asset locks the asset. Other users cannot perform any of these operations on the asset untill you check the asset back in to AEM Assets. However, they can still change the metadata for the locked asset.

To be able to check out/in assets, you require Write access on them.

This feature helps prevent other users from overriding the changes made by an author where multiple users collaborate on editing workflows across teams.

## Checking Out Assets {#checking-out-assets}

1. From the Assets UI, select the asset you want to check out. You can also select multiple assets to check out.

   ![](assets/chlimage_1-481.png)

1. From the toolbar, click/tap the **Checkout** icon.

   ![](assets/chlimage_1-482.png)

   Observe that the **Checkout** icon toggles to the **Checkin** icon with the lock open.

   ![](assets/chlimage_1-483.png)

   To verify whether other users can edit the asset you checked out, log in as a different user. A lock icon appears on the thumbnail of the asset that you checked out.

   ![](assets/chlimage_1-484.png)

   Select the asset. Notice that the toolbar does not display any options that let you edit, annotate, publish, or delete the asset.

   ![](assets/chlimage_1-485.png)

   You can, however, click/tap the **View Properties** icon to edit the metadata for the locked asset.

1. Click/tap the Edit icon to open the asset in edit mode.

   ![](assets/chlimage_1-486.png)

1. Edit the asset and save the changes. For example, crop the image and save. 

   ![](assets/chlimage_1-487.png)

   You can also choose to annotate or publish the asset.

1. Select the edited asset from the Assets UI, and click/tap the **Checkin** icon from the toolbar.

   ![](assets/chlimage_1-488.png)

   The modified asset is checked in to AEM Assets and is available to other users for editing.

## Forced Check In {#forced-check-in}

Administrators can check in assets that are checked out by other users.

1. Log in to AEM Assets as an administrator.
1. From the Assets UI select one or more assets that have been checked out by other users.

   ![](assets/chlimage_1-489.png)

1. From the toolbar, click/tap the **Release Lock** icon. The asset is checked back in and available for edit to other users.

   ![](assets/chlimage_1-490.png)
