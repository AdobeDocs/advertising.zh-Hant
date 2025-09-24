---
title: 動態廣告的工作流程
description: 瞭解管理動態廣告的工作流程。
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 動態廣告的工作流程

1. 根據可用的資產[為您的動態廣告](/help/creative/ad-templates/ad-template-manage.md)建立廣告範本

1. 設定廣告元素：

   * (適用於單一靜態HTML5廣告)收集並[上傳廣告的影像資產](/help/creative/feeds/asset-manage.md)。

   * (適用於動態HTML5廣告)建立廣告元素的目錄：

      1. 以Microsoft Excel試算表(XLSX)格式建立摘要檔案，每個廣告變化一列。 在每一列中加入影像名稱或Adobe Experience Manager參考。 單獨收集關聯的影像資產。

      1. [上傳摘要檔案和影像資產](/help/creative/feeds/asset-manage.md)。

      1. [建立摘要範本](/help/creative/feeds/feed-template-manage.md)以將摘要檔案（試算表）中的欄位對應到Advertising Creative後端中的欄位。

      1. [從指定的摘要檔案和指定的摘要範本建立目錄](/help/creative/feeds/catalog-manage.md#feed-catalog-create)，然後[處理目錄](/help/creative/feeds/catalog-manage.md#feed-catalog-process)以檢視可從中建立的廣告變化。

         您只能將每個摘要檔案用於一個目錄。

         您可以在[ > ](/help/creative/feeds/job-status-track.md) > [!UICONTROL Creative]索引標籤上[!UICONTROL Feeds]追蹤目錄處理工作[!UICONTROL Job Status]的狀態。

1. [為創意程式庫建立動態創意內容](/help/creative/creative-libraries/creative-add-dynamic.md)。 對於動態HTML5廣告，請使用指定的廣告範本和指定的目錄。

1. [建立動態廣告組合](/help/creative/creative-libraries/bundle-manage.md)，您可以一次將全部附加到廣告體驗。

1. 使用[建立動態廣告體驗（具有鎖定目標](/help/creative/experiences/experience-create-targeting.md)或[，而不具有鎖定目標](/help/creative/experiences/experience-create-no-targeting.md)），並[將其組合指派給您的動態廣告體驗](/help/creative/experiences/experience-assign-creative-bundles.md)。

1. [產生並實作廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)，以便在您的DSP中將其當成廣告來執行。

   若要在Adobe Advertising DSP中將廣告體驗作為廣告使用，請將廣告體驗標籤上傳至Advertising DSP行銷活動。 若要在其他DSP中將廣告體驗作為廣告使用，請在該DSP中實作廣告體驗標籤。
