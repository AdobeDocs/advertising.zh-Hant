---
title: 關於Adobe Advertising Creative
description: 瞭解 [!DNL Creative]。
feature: Creative Introduction
source-git-commit: 1ab83cfe82bde4a7b1a32cf3773cdce4738af497
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 關於Adobe Advertising Creative 2.0

*已關閉的Beta*

<!-- verify all and rewrite to include new stuff -->

Advertising Creative是Adobe Advertising的一部分，它是一個自助服務平台，用於自動化即時、個人化的廣告體驗，並可以選擇在創意元素級別最佳化您的廣告。

## 可重複使用創作的自訂創意程式庫

您的Creative資料庫可讓您管理將在廣告體驗中使用的創意內容。 您可以建立多個資料庫，每個資料庫都有個別創意和創意群組（稱為&#x200B;*組合*）。 您將為廣告體驗新增創意組合。

## 規則型體驗

透過[!DNL Creative]，您可以使用規則型決策樹模型來建構劇本 — 展開根據您對受眾的瞭解而即時自訂的編排廣告字串，並追蹤客戶（即使客戶移至不同的網站）<!-- verify if that's true without Adobe CDP -->。 例如，故事可以根據客戶行為、地理位置、人口統計、重新定位、客戶歷程中的位置等而變更。

<!-- Add when available:

## [!DNL Adobe] content and data integrations

[!DNL Creative] has direct integrations with Adobe Experience Manager, allowing you to easily upload the [!DNL Adobe] assets that your design team creates and use them for real-time storyboarding and editing of ad experiences.

You also can use your first-party audience segments from Adobe Audience Manager and Adobe Analytics &mdash; as well as audience segments you create in Advertising Cloud DSP
or retargeting pixels you create using [!DNL Creative] &mdash; as targets for specific creatives in an ad experience.
-->

### 體驗作為廣告的實作

建立體驗後，您可以產生體驗的JavaScript或iframe標籤，並在Advertising DSP或任何其他DSP中將標籤實作為協力廠商廣告。<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level Retargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### 廣告元素的最佳化

您可以選擇允許[!DNL Creative]使用Adobe Sensei提供支援的最佳化加權廣告輪換，根據效能（無論您是否定義特定對象目標）將任何體驗的廣告元素最佳化。

## 重新定位畫素

您可以建立重新目標畫素，以作為廣告體驗中創意內容的目標。 目標只會向具有指定屬性的使用者顯示廣告，這些使用者先前曾造訪過特定網頁。

## 曝光數、點選數和轉換追蹤

[!DNL Creative]會自動追蹤從體驗提供之廣告的所有曝光次數與點按次數。 您也可以選擇將協力廠商曝光追蹤和點選追蹤URL新增至Creative Libraries中的創意內容，以及體驗中的自訂追蹤URL。

[!DNL Creative]也會追蹤從您的廣告體驗中建立的已提供廣告的轉換。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## 績效報表

您可以在「創意>體驗」中檢視詳細的體驗層級效能報表。

您也可以在「報表>自訂報表」中建立自訂Creative報表，以監控您體驗中的體驗層級效能。 如果您在DSP行銷活動中使用您的[!DNL Creative]體驗作為廣告，則這些廣告的效能資料可在其他自訂報表中使用，就像您的其他DSP廣告的資料一樣。<!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

您可以選擇將自訂報表傳送至指定的[報表目的地](/help/dsp/reports/report-destinations/report-destination-about.md)。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)
>* [關於Advertising Creative中的體驗](/help/creative/experiences/experience-about.md)
