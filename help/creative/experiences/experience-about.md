---
title: 關於Advertising Creative中的體驗
description: 瞭解如何設定個人化廣告體驗，並根據效能最佳化廣告元素。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 75d774a53521f1035c9f3a4f17b523ed1b68fec8
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 關於Advertising Creative 2.0中的體驗

*已關閉的Beta*

[!DNL Advertising Creative 2.0]在單一創意資料庫中為廣告提供兩種不同的廣告體驗結構。

* **決策樹目標定位的體驗：** [!DNL Creative]可讓您使用決策樹模型，在整個客戶歷程中設定個人化的廣告體驗。 您可以根據目標受眾自訂所有廣告元素 — 影像、標題、選件和登陸頁面。

  例如，您可以為位在特定Adobe Analytics受眾區段的芝加哥和紐約市人，指定相同的創意組合，但將芝加哥人傳送至與紐約人不同的登陸頁面。 您也可以為區段中除了芝加哥和紐約市以外任何地方居住的人指定不同的組合，並為不在區段中的其他人指定第三個組合。

  目標定位選項包括：

   * Adobe Audience Manager、Adobe Analytics和Advertising Cloud DSP的第一方受眾區段

   * 特定地理位置，包括國家、州、美國境內的DMA、城市和郵遞區號

   * 從DSP、發佈者或合作夥伴(例如SKU=01234567890123或Cart=empty)傳遞特定索引鍵值配對（資料傳遞目標）的檢視器

   * [!DNL Creative]正在重新定位畫素和指定的屬性值

   * 特定裝置型別、作業系統和瀏覽器

  在決策樹中建立目標對象分支後，您可以透過將創意套件組合指派給分支，將目標對象與潛在創意配對。 對於每個體驗，您可以自訂創意組合的最佳化和排程，並變更每個組合中個別創意的預設登陸頁面和追蹤URL<!-- later: and any flexible attributes -->。

* **沒有決策樹定位的體驗：** [!DNL Creative]會最佳化廣告體驗的廣告元素，而不會縮小對象範圍。 您可以為每個體驗指定開始和結束日期以及某些預設設定，但大部分工作流程並非直接在體驗內。 不要將創意內容直接加入體驗，請使用[!UICONTROL Tag Manager]為體驗的每個廣告大小建立廣告標籤，然後新增創意內容、設定創意最佳化和排程，以及自訂登入頁面和追蹤URL<!-- later: and any flexible attributes -->。

>[!NOTE]
>
> 由於這兩種體驗型別的工作流程不同，因此您無法將非目標體驗變更為目標體驗，也無法將目標體驗變更為非目標體驗。

## 廣告服務與最佳化

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative]會根據指定的目標定位（適用時）、排程、廣告輪換和最佳化目標選項，以及可用的廣告詳細目錄，提供第一方廣告並觸發體驗的第三方廣告。

* **排程：** （選擇性）排程特定創意在指定的連續時段內執行。

* **廣告旋轉：**&#x200B;根據相對權重手動旋轉創意，或根據指定的最佳化目標採用演演算法。

* **最佳化目標：**&#x200B;針對最佳點進率或現有[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)最佳化廣告元素

  [!DNL Creative]會透過為體驗中表現最佳的資產提供曝光比重，來最佳化廣告體驗。 針對鎖定在特定對象的體驗，廣告可以根據目標對象集的個別廣告元素效能進行最佳化。 對於沒有特定對象目標的體驗，廣告元素會僅根據個別廣告元素的效能進行最佳化。

例如，您可以將Creative 1排程在前兩週執行，以最佳化點進率，並將Creative 2排程在接下來的兩週執行，以最佳化指定的自訂目標。

## 實作和管理體驗

建立即時體驗（包含所有必要的廣告元素）後，您可以[為整個體驗](experience-tag-export.md)產生JavaScript或iframe標籤。 您可以將體驗標籤作為廣告上傳至Adobe Advertising DSP中的行銷活動，或將其實作協力廠商DSP中的廣告。

>[!NOTE]
>
>階層式鎖定目標行為可能因DSP而異。 Advertising DSP會套用廣告層級鎖定目標到版位層級鎖定目標。

## 您體驗的效能資料

下列為可用的效能資料：

* 當您在「[!UICONTROL Creative] > [!UICONTROL Experiences]」檢視中啟用「[!UICONTROL Metrics]」選項時，每個體驗卡片或資料列都會指出所收到體驗的曝光次數與點按次數。

  ![量度選項](/help/creative/assets/metrics-option.png "量度選項")

* 您可以從[!UICONTROL Experiences]檢視[檢視任何體驗](experience-performance-details.md)的詳細效能資料。

* 若要監視所有體驗的效能，請建立[自訂Creative報表](/help/creative/report-custom-creative.md)。

## 體驗狀態 {#experience-statuses}

除了您手動設定的&#x200B;*已刪除，*&#x200B;之外，體驗的狀態是自動設定的。

| 狀態 | 說明 |
| ------ | ----------- |
| [!UICONTROL Live] | 體驗包含所有必要的元素，因此您可以產生體驗標籤，以在DSP中實作廣告。 即時體驗可能已排程在未來開始。 |
| [!UICONTROL Draft] | 由於體驗的所有分支皆未指派創意，因此體驗並不完整，且您無法產生體驗標籤。 |
| [!UICONTROL Processing] | 先前已編輯過即時體驗，但現在未完成。 您無法為其產生體驗標籤。 **注意：**&#x200B;如果您已實作體驗的體驗標籤，則仍可提供先前的即時版本。 如果您稍後完成體驗（讓體驗再次上線），則可使用現有的標籤實作提供新版本。 |
| [!UICONTROL Deleted] | 體驗已從[!DNL Creative]中刪除，且不再顯示在[!UICONTROL Experiences]檢視中。 |

>[!NOTE]
>
>您可以在DSP中變更廣告的狀態，而不影響[!DNL Creative]中的體驗狀態。

## [!UICONTROL Experiences]檢視

[!UICONTROL Experiences]檢視會顯示您所有鎖定目標和非鎖定目標的體驗。 您可以檢視指派的創意或創意組合的體驗名稱、狀態、開始和結束日期、數量和維度，以及體驗是否包含動態廣告。 當您在[!UICONTROL Experiences]檢視中啟用[!UICONTROL Metrics]選項時，每個體驗卡片或資料列都會指出所收到體驗的曝光次數與點按次數。 當您處於卡片模式時，可以使用&lt;和>按鈕捲動包含多個創意的體驗中的創意。

您可以建立並管理您的體驗、建立及重新命名廣告體驗標籤，以及匯出JavaScript和iframe格式的標籤，以在DSP上實作。 使用Advertising DSP的廣告商可選擇將廣告標籤直接上傳至Advertising DSP行銷活動。

### 可用動作

以下是可用的主要動作。 如需完整清單，請參閱「創意內容>體驗」一章的目錄。

* [下載檢視中的資料](experience-download-view.md)

* [建立](/help/creative/experiences/experience-create-targeting.md)和[編輯](/help/creative/experiences/experience-edit-targeting.md)目標定位體驗

* [建立](/help/creative/experiences/experience-create-no-targeting.md)、[編輯](/help/creative/experiences/experience-edit-no-targeting.md)，以及[手動建立廣告標籤](/help/creative/experiences/experience-tag-create-manually.md)，讓體驗不必鎖定目標

* [複製](experience-clone.md)體驗

* [預覽](experience-preview.md)體驗

* [分享體驗的示範URL](experience-share-demo-url.md)

* [匯出體驗的廣告標籤](experience-tag-export.md)，包括選擇性直接將廣告標籤上傳至Advertising DSP行銷活動

* [刪除](experience-delete.md)體驗

>[!MORELIKETHIS]
>
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [建立體驗，但不鎖定目標](experience-create-no-targeting.md)
