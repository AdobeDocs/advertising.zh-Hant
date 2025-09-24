---
title: 管理資產檔案
description: 瞭解如何上傳和管理廣告商的資產檔案。
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# 管理資產檔案

動態HTML5廣告需要Microsoft Excel試算表(XLSX)格式的摘要檔案，以及在試算表中參照的影像資產(Adobe Experience Manager資產參照除外)。 靜態HTML5廣告的每個廣告只需要一個影像資產。

>[!NOTE]
>
> 您只能將每個摘要檔案用於一個目錄。

## 檔案需求

* 動態HTML5廣告：

   * Microsoft Excel試算表(XLSX)格式的摘要檔案，每個廣告變化有一個標題列和一個資料列。 在每一列中包含影像名稱或Adobe Experience Manager參考。<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

     對於您要上傳的影像，請使用格式`images/image_name` （例如`images/300x250_acme_logo.png`.）<!-- Verify.  Also need to include the spec for how to reference images in AEM -->參考影像

   * JPEG、JPG或PNG格式的相關影像資產。<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. -->檢視[支援的創意大小](/help/creative/creative-libraries/creative-sizes.md)。

  您可以上傳單一XLSX檔案、單一影像檔案，或包含任何XLSX和影像檔案組合的單一ZIP檔案。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 靜態HTML5廣告：

   * JPG、JPEG或PNG格式中每個廣告一個影像資產。

     您可以在ZIP檔案中上傳單一影像或多個影像。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## 上傳資產檔案

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Assets]**」標籤。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Asset]**。

1. 設定資產檔案：

   1. 選取可存取資產檔案的廣告商。

   1. 以下列其中一種方式指定資產檔案：

      * 將裝置或網路上的檔案拖放至方塊中。

      * 按一下&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

所有ZIP檔案都會自動解壓縮。 上傳試算表檔案時，該檔案會列在[!UICONTROL Feeds]子標籤上。 上傳影像檔時，影像檔會列在[!UICONTROL Images]子標籤上。

## 下載資產檔案

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Assets]**」標籤。

1. 將游標停留在資產列上，然後按一下&#x200B;**[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

## 刪除資產檔案

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Assets]**」標籤。

1. 將游標停留在資產列上，然後按一下&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理摘要範本](/help/creative/feeds/feed-template-manage.md)
>* [管理目錄](/help/creative/feeds/catalog-manage.md)
>* [管理動態廣告範本](/help/creative/ad-templates/ad-template-manage.md)
>* [將動態創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-dynamic.md)
