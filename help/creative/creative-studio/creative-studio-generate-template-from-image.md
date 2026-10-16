---
title: 使用AI從影像產生廣告範本
description: 瞭解如何在Creative Studio中使用AI，將現有的靜態顯示廣告影像轉換為可編輯的廣告範本。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# 使用AI從影像產生廣告範本

*Beta功能*

在[!UICONTROL Creative Studio]中使用AI將現有的靜態顯示廣告影像轉換為可編輯的顯示廣告範本。 檢閱產生的範本、使用自然語言請求變更，並開啟範本編輯器以手動變更並儲存範本。

## 開始之前

您需要Creative資料庫中現有的靜態影像廣告。 此工作流程會從您的程式庫選取廣告；但不會直接在產生對話方塊中上傳新影像。

## 產生並檢閱範本 {#template-generate}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. （可選）從頁面頂端的廣告商清單中選取一個廣告商，以檢視該廣告商的資料庫。

1. 在&#x200B;**[!UICONTROL Use AI to Generate a New Display Ad Template]**&#x200B;方塊中，按一下&#x200B;**[!UICONTROL Generate]**。

1. 在&#x200B;**[!UICONTROL Generate New Ad Template]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL Generate from Existing Standard Ad Image]** （如果尚未選取）。

1. 從&#x200B;**[!UICONTROL Ad Library]**&#x200B;清單中選取包含影像廣告的資料庫。

1. 將游標停留在影像廣告卡上，然後按一下&#x200B;**[!UICONTROL Use this Standard Ad]**。

   使用選取的廣告寬度和高度，產生程式會自動開始。

1. 等待產生完成，然後檢閱範本預覽和&#x200B;**[!UICONTROL Layers]**&#x200B;面板（如果可用）。

   在使用範本之前，請檢查文字、影像和版面配置。 這裡顯示的圖層可供檢閱；請在範本編輯器中手動變更。

1. （選用）要求變更產生的範本：

   1. 在&#x200B;**[!UICONTROL Ask the AI for any changes]**&#x200B;欄位中，說明您想要的變更。 例如，輸入`Change the headline to "Limited Time Offer" and the button text to "Shop Now"`。

   1. 按一下&#x200B;**[!UICONTROL Regenerate]**。

   1. 檢閱更新的預覽。 視需要重複。

1. 當您準備好要繼續時，請按一下&#x200B;**[!UICONTROL Use this Ad Template]**。

   產生的範本會在顯示範本編輯器中開啟。

## 編輯並儲存範本 {#template-save}

1. 在範本編輯器中，檢閱產生的元素，並使用[範本編輯器控制項](creative-studio-manage-templates.md#template-controls)進行任何剩餘的變更。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 在&#x200B;**[!UICONTROL Update Template]**&#x200B;對話方塊中，輸入或更新&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**，並選擇性地新增標籤。

1. 按一下&#x200B;**[!UICONTROL Update]**&#x200B;儲存範本並返回&#x200B;**[!UICONTROL Templates]**&#x200B;檢視。

   若要儲存個別復本，請按一下&#x200B;**[!UICONTROL Save As New]**。

然後您可以使用範本來[產生廣告變化](creative-studio-manage-templates.md#ad-variations-generate)。

## 如果您無法產生範本 {#troubleshooting}

* **未列出任何媒體櫃或影像廣告：**&#x200B;請檢查選取的廣告商和&#x200B;**[!UICONTROL Ad Library]**。 如果媒體櫃沒有標準廣告影像，請選取包含現有靜態影像廣告的其他媒體櫃。

* **產生失敗或無法轉換影像：**&#x200B;檢閱顯示的訊息，按一下&#x200B;**[!UICONTROL Back to library]**，然後選取影像廣告再試一次。

>[!MORELIKETHIS]
>
>* [在Creative Studio中管理廣告範本](creative-studio-manage-templates.md)
>* [在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)