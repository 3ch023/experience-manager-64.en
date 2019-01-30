---
title: Camera Raw Support
seo-title: Camera Raw Support
description: null
seo-description: Learn how to enable Camera Raw support in Adobe Experience Manager (AEM) Assets.
uuid: b9288340-38a5-4bbc-b03a-1b8f154d281d
acrolinxdate: 2019-01-12T17 26 15.127-0500
acrolinxlastcheckedby: asgupta
acrolinxpagestatus: red
acrolinxreporturl: http //acrolinx.corp.adobe.com 8031/output/en/camera_raw_krs_workflow_f3c2f2ccebf6138e_108_report.xml
acrolinxsentences: 35
acrolinxwords: 427
contentOwner: Chiradeep Majumdar
products: SG_EXPERIENCEMANAGER/6.4/ASSETS
topic-tags: administering
content-type: reference
discoiquuid: 549c7074-fc18-467c-bf3a-890a0ab7b49d
isreadyforlocalization: false
index: y
internal: n
snippet: y
---

# Camera Raw Support{#camera-raw-support}

The Camera Raw package enables support for various raw file formats, such as .cr2, .nef, .raf, and so on. The Camera Raw functionality is supported in AEM to render your assets in JPEG format. The supported pacakge is available at [http://blogs.adobe.com/lightroomjournal/2017/03/acr-9-9-now-available.html](http://blogs.adobe.com/lightroomjournal/2017/03/acr-9-9-now-available.html).

>[!NOTE]
>
>The functionality supports only JPEG renditions.

To enable Camera Raw support in Adobe Experience Manager (AEM) Assets:

1. Based on the AEM version and the operating system, download the appropriate Camera Raw package and install it:

<table border="0" cellpadding="0" cellspacing="0" width="0"> 
 <tbody>
  <tr>
   <td><p><strong>Supported Platforms</strong></p> </td> 
   <td><p><strong>Package Share Link</strong></p> </td> 
   <td><p><strong>Supported AEM Versions</strong></p> </td> 
  </tr>
  <tr>
   <td><p>Windows 64 Bit, Mac OS, RHEL 7.x</p> </td> 
   <td><p><a href="https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/aem630/product/assets/aem-assets-cameraraw-pkg">1.3.16</a></p> </td> 
   <td><p>6.3, 6.4</p> </td> 
  </tr>
  <tr>
   <td><p>Windows 64 Bit, Mac OS, RHEL 7.x</p> </td> 
   <td><p><a href="https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/aem620/product/assets/aem-assets-cameraraw-pkg">1.2.8</a></p> </td> 
   <td><p>6.2 </p> </td> 
  </tr>
  <tr>
   <td><p>Windows 64 Bit, Mac OS, RHEL 7.x</p> </td> 
   <td><p><a href="https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/aem610/product/assets/aem-assets-cameraraw-pkg">1.1.22</a></p> </td> 
   <td><p>6.1</p> </td> 
  </tr>
 </tbody>
</table>

1. Go to `http://[AEM server]:[Port]/workflow`. For example, go to `http://localhost:4502/workflow` and open the **[!UICONTROL DAM Update Asset]** workflow.
1. Open the sample workflow **[!UICONTROL Sample DAM Update Asset With Camera RAW and DNG Handling Step]**. Using this workflow as a reference, configure the **[!UICONTROL DAM Update Asset]** workflow for AEM Assets.
1. Open the **[!UICONTROL Process Thumbnails]** step.  

1. Provide the following configuration in the **[!UICONTROL Thumbnails]** tab:

    * Thumbnails: `140:100:false, 48:48:false, 319:319:false`
    * Skip Mime Types: `skip:image/dng, skip:image/x-raw-(.*)`

   ![](assets/chlimage_1-288.png)

1. In the **[!UICONTROL Web Enabled Image]** tab, specify the following:

    * Skip List: `audio/mpeg, video/(.*), image/dng, image/x-raw-(.*)`

   ![](assets/chlimage_1-289.png)

1. From SideKick, add the **[!UICONTROL Camera Raw/DNG Handler]** step below the **[!UICONTROL Thumbnail creation]** step.
1. In the **[!UICONTROL Camera Raw/DNG Handler]** step, provide the following configuration in the **[!UICONTROL Arguments]** tab:

   Mime Types: `image/dng, image/x-raw-(.*)`

   Command:

    * `DAM_Raw_Converter ${directory}/${filename} ${directory} cq5dam.web.1280.1280.jpeg 1280 1280`
    * `DAM_Raw_Converter ${directory}/${filename} ${directory} cq5dam.thumbnail.319.319.jpeg 319 319`
    * `DAM_Raw_Converter ${directory}/${filename} ${directory} cq5dam.thumbnail.140.100.jpeg 140 100`
    * `DAM_Raw_Converter ${directory}/${filename} ${directory} cq5dam.thumbnail.48.48.jpeg 48 48`

   ![](assets/chlimage_1-290.png)

1. Click **[!UICONTROL Save]**.

   You can now import camera raw files into AEM Assets.

   >[!NOTE]
   >
   >Linux, Windows, and Mac (with 64-bit JVM) support the Camera Raw package.

   After you install the Camera RAW package and configure the required workflow, **[!UICONTROL Image Adjust]**** **option appears in the list of panes.

   ![](assets/chlimage_1-291.png)

   Click **[!UICONTROL Image Adjust]** from the list and use the options in the **[!UICONTROL Image Adjust]** pane to make lightweight edits to your image.

   ![](assets/chlimage_1-292.png)

After saving the edits to a Camera Raw image, a new rendition `AdjustedPreview.jpg` is generated for the image. For other image types except Camera Raw, the changes are reflected in all the renditions.

>[!NOTE]
>
>The Camera Raw library has limitations around the total pixels it can process at a time. Currently, it can process a maximum of 1073741824 (1024 x 1024 x 1024) pixels.
