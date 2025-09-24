---
title: 管理摘要範本
description: 瞭解如何管理摘要範本。
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 管理摘要範本

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

摘要範本會將摘要檔案中的欄位與Advertising Creative後端上的欄位進行對應。 動態HTML5廣告(而非靜態HTML5廣告)需要摘要範本才能建立動態廣告。

您可以使用具有多個廣告範本的摘要範本。

## 建立摘要範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Template]**。

1. 指定[摘要範本設定](#feed-template-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 編輯摘要範本

**注意：**&#x200B;您只能編輯您建立的摘要範本。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本列上並按一下&#x200B;**[!UICONTROL Duplicate]**。

1. 視需要編輯[摘要範本設定](#feed-template-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 檢視摘要範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本列上並按一下&#x200B;**[!UICONTROL View]**。

## 複製摘要範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本列上並按一下&#x200B;**[!UICONTROL Duplicate]**。

1. 在[!UICONTROL Duplicate Template]畫面中，輸入唯一的&#x200B;**[!UICONTROL Template Name]**。 如果要複製其他人建立的範本，請選取&#x200B;**[!UICONTROL Advertiser]**。 視需要選擇性地編輯其他[摘要範本設定](#feed-template-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 下載摘要範本

下載的摘要範本採用壓縮的Microsoft Excel試算表(XLSX)格式。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本列上並按一下&#x200B;**[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

## 摘要範本設定 {#feed-template-settings}

### [!UICONTROL General]設定

**[!UICONTROL Template Name]：**&#x200B;指定廣告商的唯一範本名稱。

**[!UICONTROL Advertiser]：**&#x200B;可以使用範本的廣告商。

**[!UICONTROL Description]：** （選用）對使用摘要範本的任何人有用的資訊。

### [!UICONTROL Field Mapping]設定

將摘要檔案中的每個欄位對應至Advertising Creative後端上的欄位。<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->至少一個摘要檔案欄位必須標示為&quot;[!UICONTROL Is Unique]&quot;。 若要新增欄位對應，請按一下&#x200B;**[!UICONTROL +]**。 若要移除最後一個欄位對應，請按一下&#x200B;**[!UICONTROL +]**。

**[!UICONTROL Field Name]：**&#x200B;摘要檔案中的欄位。

**[!UICONTROL Description]：** （選用）對使用摘要範本的任何人有用的資訊。

**[!UICONTROL Is Unique]：**&#x200B;指出欄位是唯一ID （索引鍵）。 每個摘要範本至少必須有一個欄位是唯一的。 若要選取此選項，請按一下按鈕將其向右移動。<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]：** Advertising Creative後端對應至摘要檔案中所指定[!UICONTROL Field Name]的欄位。

>[!MORELIKETHIS]
>
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理資產檔案](/help/creative/feeds/asset-manage.md)
>* [管理目錄](/help/creative/feeds/catalog-manage.md)
>* [追蹤目錄處理工作的狀態](/help/creative/feeds/job-status-track.md)
>* [管理動態廣告範本](/help/creative/ad-templates/ad-template-manage.md)
>* [將動態創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-dynamic.md)
