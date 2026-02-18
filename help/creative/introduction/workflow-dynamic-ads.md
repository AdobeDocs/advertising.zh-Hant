---
title: 動態廣告的工作流程
description: 瞭解管理動態廣告的工作流程。
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# 動態廣告的工作流程

*具有建立動態廣告許可權的使用者*

您可以透過下列兩種方式之一設定動態廣告：

* 工作流程1：將動態廣告新增至創意程式庫時，請直接在動態廣告設定中上傳廣告範本和廣告變數目錄。 您可以下載現有的摘要範本以建立目錄。

  當同一人可以提供所有資訊（摘要範本除外）來建立廣告時，請使用此工作流程。 上傳的檔案仍可供日後使用。

* 工作流程2：在個別檢視中設定廣告範本和廣告變化目錄，然後使用已可取得的廣告範本和目錄，個別將動態廣告新增至創意內容。

  當不同的人員將完成不同的任務或您一次只想完成一個任務時，請使用此工作流程。

## 工作流程1

>[!PREREQUISITES]
>
>* 廣告範本：顯示廣告範本(包含HTML5檔案的ZIP檔案)或視訊廣告範本（包含.scene檔案的ZIP檔案）
>* CSV、TSV或Microsoft Excel試算表(XLSX)格式的產品目錄

1. [為創意程式庫建立動態創意內容](/help/creative/creative-libraries/creative-add-dynamic.md)。 對於動態HTML5和影片廣告，請上傳或選取現有的廣告範本和目錄。

1. 針對廣告體驗使用動態創意內容：

   1. [建立動態廣告組合](/help/creative/creative-libraries/bundle-manage.md)，您可以一次將全部附加到廣告體驗。

   1. 建立具有鎖定目標[或](/help/creative/experiences/experience-create-targeting.md)的動態廣告體驗[而不鎖定目標](/help/creative/experiences/experience-create-no-targeting.md)，並[將創意組合指派給體驗](/help/creative/experiences/experience-assign-creative-bundles.md)。

   1. [產生並實作廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)，以便在您的DSP中將其當成廣告來執行。

      若要在Adobe Advertising DSP中將廣告體驗作為廣告使用，請將廣告體驗標籤上傳至Advertising DSP行銷活動。 若要在其他DSP中將廣告體驗作為廣告使用，請在該DSP中實作廣告體驗標籤。

## 工作流程2

1. [根據可用的資產，為您的動態廣告](/help/creative/ad-templates/ad-template-manage.md)建立廣告範本。 廣告範本必須是ZIP格式並包含：<!-- Need to add more specs for templates -->

* 顯示創意：具有所需廣告格式的HTML5檔案，以及具有廣告屬性(.tdf)的檔案(僅限動態HTML5廣告)

* 視訊創意：具有所需廣告格式的.scene檔案和具有廣告屬性(.tdf)的檔案

1. 設定廣告元素：

   * (適用於單一靜態HTML5廣告)收集並[上傳廣告的影像資產](/help/creative/feeds/asset-manage.md)。

   * (適用於動態HTML5和影片廣告)建立廣告元素的目錄：

      1. 以Microsoft Excel試算表(XLSX)格式建立摘要檔案，每個廣告變化一列。 在每一列中加入影像或視訊名稱。 分別收集關聯的影像和視訊資產。

      1. [上傳摘要檔案和資產](/help/creative/feeds/asset-manage.md)。

      1. [建立摘要範本](/help/creative/feeds/feed-template-manage.md)以將摘要檔案（試算表）中的欄位對應到Advertising Creative後端中的欄位。 您可以選擇下載主摘要範本並填入與零售業<!-- and what is the creative template?-->相關的欄位。

      1. [從指定的摘要檔案和指定的摘要範本建立目錄](/help/creative/feeds/catalog-manage.md#feed-catalog-create)，然後[處理目錄](/help/creative/feeds/catalog-manage.md#feed-catalog-process)以檢視可從中建立的廣告變化。

         您只能將每個摘要檔案用於一個目錄。

         您可以在[ > ](/help/creative/feeds/job-status-track.md) > [!UICONTROL Creative]索引標籤上[!UICONTROL Feeds]追蹤目錄處理工作[!UICONTROL Job Status]的狀態。

1. [為創意程式庫建立動態創意內容](/help/creative/creative-libraries/creative-add-dynamic.md)。 對於動態HTML5廣告，請使用指定的廣告範本和指定的目錄。

1. 針對廣告體驗使用動態創意內容：

   1. [建立動態廣告組合](/help/creative/creative-libraries/bundle-manage.md)，您可以一次將全部附加到廣告體驗。

   1. 建立具有鎖定目標[或](/help/creative/experiences/experience-create-targeting.md)的動態廣告體驗[而不鎖定目標](/help/creative/experiences/experience-create-no-targeting.md)，並[將創意組合指派給體驗](/help/creative/experiences/experience-assign-creative-bundles.md)。

   1. [產生並實作廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)，以便在您的DSP中將其當成廣告來執行。

      若要在Adobe Advertising DSP中將廣告體驗作為廣告使用，請將廣告體驗標籤上傳至Advertising DSP行銷活動。 若要在其他DSP中將廣告體驗作為廣告使用，請在該DSP中實作廣告體驗標籤。
