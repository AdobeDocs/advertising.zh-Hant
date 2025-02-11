---
title: 關於Advertising Creative中的體驗
description: 瞭解如何設定個人化廣告體驗，並根據效能最佳化廣告元素。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 8f81cf8ffaec7ca30ee3bbfd45d3577e75d77faf
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# 關於Advertising Creative 2.0中的體驗

*已關閉的Beta*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0]為創意媒體櫃中的廣告提供兩種不同的廣告體驗結構<!-- can use a single library only -->：

* **決策樹目標定位的體驗：** [!DNL Creative]可讓您使用決策樹模型，在整個客戶歷程中設定個人化的廣告體驗。 您可以根據目標受眾自訂所有廣告元素 — 影像、標題、選件和登陸頁面。

  例如，您可以為位於特定Adobe Analytics受眾區段的芝加哥和紐約市使用者指定相同的創意組合，但將位於相同區段的芝加哥使用者傳送至與紐約使用者不同的登陸頁面。 您也可以為區段中除了芝加哥和紐約市以外任何地方居住的人指定不同的組合，並為不在區段中的其他人指定第三個組合。

  目標定位選項包括來自Adobe Audience Manager、Adobe Analytics和Advertising Cloud DSP的第一方對象區段中的檢視器；特定地理位置的檢視器，包括國家、州、美國境內的DMA、城市和郵遞區號；從DSP、發行者或合作夥伴傳遞特定索引鍵值配對（資料傳遞目標）的檢視器；具有[!DNL Creative]重新定位畫素和指定屬性值的檢視器；以及具有特定裝置型別、作業系統和瀏覽器的檢視器。

  您可以將創意套件組合指派給每個體驗，選擇性地自訂創意套件組合的最佳化和排程，以及變更每個套件組合中個別創意的預設登陸頁面和追蹤URL<!-- and any flexible attributes -->。

* **沒有決策樹定位的體驗：** [!DNL Creative]會最佳化廣告體驗的廣告元素，而不會縮小對象範圍。<!-- For first-party creatives, [!DNL Creative] serves the ads. -->您將為每個體驗指定開始和結束日期以及某些預設設定，但大部分工作流程並非直接在體驗內。 您可以在[!UICONTROL Tag Manager]內，針對體驗的每個廣告大小建立廣告標籤，然後新增創意、設定創意最佳化和排程，以及自訂登陸頁面和追蹤URL，而不是直接將創意新增至體驗。

## 廣告最佳化

<!-- MORE -->
[!DNL Creative]會根據效能最佳化任何體驗的廣告元素。 針對鎖定在特定對象的體驗，廣告可以根據目標對象集的個別廣告元素效能進行最佳化。 對於沒有特定對象目標的體驗，廣告元素會完全根據個別廣告元素的效能進行最佳化。

## 實作和管理體驗

建立即時體驗（包含所有必要的廣告元素）後，您可以[為整個體驗](experience-tag-export.md)產生JavaScript或iframe標籤，您可以選擇將標籤上傳至Adobe Advertising DSP中的行銷活動或實作協力廠商DSP中的廣告。 [!DNL Creative]會根據鎖定目標和廣告輪換選項以及可用的廣告詳細目錄，提供體驗的廣告。

## 您體驗的效能資料

當您在[!UICONTROL Experiences]檢視中啟用[!UICONTROL Metrics]選項時，每個體驗卡片或資料列都會指出所收到體驗的曝光次數與點按次數。

![量度選項](/help/creative/assets/metrics-option.png "量度選項")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

您可以從[!UICONTROL Creative] > [!UICONTROL Experiences]檢視中檢視任何體驗的詳細效能資料。 若要監視所有體驗的效能，請建立[!UICONTROL Custom Creative Report]。

<!--
You can [view detailed performance data for any experience](experience-performance-details.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## 體驗狀態 {#experience-statuses}

<!-- verify that these are all still the same -->

除了您手動設定的&#x200B;*已刪除、*&#x200B;之外，體驗的狀態是自動設定的。

*即時：*&#x200B;體驗包含所有必要的元素，因此您可以產生體驗標籤，以在DSP中實作廣告。<!-- A live experience may be scheduled to start in the future -->

*草稿：*&#x200B;體驗的所有分支均未指派創意，因此體驗不完整，您無法產生體驗標籤。

*處理中：*&#x200B;先前上線的體驗已經過編輯，但現在尚未完成。 您無法為其產生體驗標籤。 **注意：**&#x200B;如果您已經為體驗實作體驗標籤，則仍會提供先前上線的版本。 如果您稍後完成體驗（讓體驗再次上線），則會使用現有標籤實作提供新版本。

*已刪除：*&#x200B;體驗已從[!DNL Creative]中刪除，並且不再顯示在[!UICONTROL Experiences]檢視中。

>[!NOTE]
>
>您可以在DSP中變更廣告的狀態，而不影響[!DNL Creative]中的體驗狀態。

## [!UICONTROL Experiences]檢視

[!UICONTROL Experiences]檢視會顯示您所有鎖定目標和非鎖定目標的體驗。 您可以檢視指派的創意或創意組合的體驗名稱、狀態、開始和結束日期、數量和維度，以及體驗是否包含動態廣告。 當您在[!UICONTROL Experiences]檢視中啟用[!UICONTROL Metrics]選項時，每個體驗卡片或資料列都會指出所收到體驗的曝光次數與點按次數。

您可以建立和管理您的體驗，包括最佳化並將創意和創意組合指派給您的體驗。 您也可以建立和重新命名廣告體驗標籤，並匯出JavaScript和iframe格式的標籤，以在DSP上實作。 使用Advertising DSP的廣告商可選擇將標籤直接上傳至Advertising DSP促銷活動作為廣告。

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [建立體驗，但不鎖定目標](experience-create-no-targeting.md)
