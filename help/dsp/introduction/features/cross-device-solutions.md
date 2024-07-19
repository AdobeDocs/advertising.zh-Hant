---
title: 跨裝置解決方案
description: 進一步瞭解跨裝置功能。
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# 跨裝置解決方案

Advertising DSP與[!DNL LiveRamp]的整合可讓您將對象擴充至所有個人的已知裝置，而不只是您的品牌已追蹤的裝置。 此整合也提供所有裝置的頻率限定和歸因測量。

使用支援的以人物為基礎的裝置圖表時，您可以：

* 跨管道和裝置比對受眾，將廣告傳送給個人和家庭，而非裝置。
* 透過瞭解並限定跨個人的頻率來平衡廣告曝光。
* 測試跨管道或裝置公開與轉換對象的策略。

## [!DNL LiveRamp]裝置圖表的優點

* 提供確定性資料集區，包括離線客戶資料

* 在Cookie ID和行動裝置ID之間提供均勻的涵蓋範圍

* 包括主要來自美國的資料

* 免費提供頻率限定和歸因測量

* 延長的曝光次數定價為$0.35 CPM （僅使用[!DNL LiveRamp]裝置圖表傳送的曝光次數，而非目標受眾區段內找到的裝置）

  費率會反映在您的帳戶費率卡上。

## 以人物為基礎的頻率管理

以人物為基礎的頻率管理可讓您在人員層級（而非裝置層級）指定真正的媒體曝光控制的頻率上限。

### 啟用以人物為基礎的頻率管理

* **行銷活動：**&#x200B;當您建立新的行銷活動時，可以指定[!UICONTROL Cross-Device Level]設定。 啟用「[!UICONTROL Same Device]」 — >「[!UICONTROL People]」，然後選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置目標定位，以及行銷活動、封裝和位置層級的人員型頻率管理。 頻率上限適用於個人所有已知裝置。

如需詳細資訊，請參閱[促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

儲存行銷活動後，就無法變更其[!UICONTROL Cross Device Level]設定。

* **封裝：**&#x200B;您可以選擇在封裝層級設定額外的頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

* **位置：**&#x200B;您可以選擇在位置層級設定額外的頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

## 以人物為基礎的鎖定目標

以人物為基礎的鎖定目標可讓您在桌上型電腦和行動裝置上尋找客戶。

### 啟用以人物為基礎的鎖定目標

* **行銷活動：**&#x200B;當您建立新的行銷活動時，可以指定[!UICONTROL Cross-Device Level]設定。 啟用「[!UICONTROL Same Device]」 — >「[!UICONTROL People]」，然後選取裝置圖表。 指定的裝置圖表會用於位置層級的跨裝置目標定位和以人物為基礎的頻率管理。

如需詳細資訊，請參閱[促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

* **刊登版位：**&#x200B;當您針對具有指定裝置圖表的促銷活動中的刊登版位選取對象目標時，[!UICONTROL Cross-Device Targeting]選項可讓您擴充目標至個人所有已知裝置（根據促銷活動設定中指定的裝置圖），甚至不在指定區段中的裝置。

### 設定以人物為基礎的鎖定目標報告

您可以在自訂報表中包含下列量度：

* **延伸曝光次數：** （在[!UICONTROL Metrics] > [!UICONTROL Std. Metrics]下的[!UICONTROL Build Your Report]區段中）運用裝置圖表傳送的增量曝光次數（未在原始受眾區段中找到）。 此量度也可用來計算與使用協力廠商裝置圖表相關的適用費用。

  若要判斷特定時段內延伸曝光的成本，請執行包含[!UICONTROL Extended Impressions]欄的自訂報表，然後將延伸曝光總數乘以$0.00035 （$0.35/1000曝光數）。

  彙總成本也包含在[!UICONTROL Billable Other Net Spend]欄（[!UICONTROL Metrics] > [!UICONTROL Spend]下）中，但該量度也包含您可能已新增的其他行銷活動費用。

* **裝置圖表：** （在[!UICONTROL Dimensions] > [!UICONTROL Campaign]下的[!UICONTROL Build Your Report]區段中）為特定行銷活動、封裝或位置選取的裝置圖表。

## 以人物為基礎的歸因測量

*僅追蹤Adobe Advertising轉換的廣告商*

使用以人物為基礎的歸因，您可以將發生在不同裝置上的轉換歸因於發生媒體曝光的裝置。 以人物為基礎的歸因測量，適用於在其網站上實作Adobe Advertising轉換畫素的廣告商，可跨DSP、[!DNL Adobe Advertising Creative]和[!DNL Adobe Advertising Search, Social, & Commerce]使用。

### 啟用以人物為基礎的歸因測量

如果您想要啟用跨裝置歸因測量，請聯絡您的Adobe客戶團隊。

### 設定跨裝置轉換歸因的轉換報表

#### 轉換報表設定

當裝置圖表啟用歸因測量時，[!UICONTROL Conversion]報表會包含[!UICONTROL Cross-Device Breakout]設定，此設定可讓您針對每個轉換量度包含最多三個個別的欄，包括：

* &lt;*轉換*>[!UICONTROL (tp)]：包含轉換總數（總人數），其中包含相同裝置轉換和跨裝置轉換（如果適用）。 在報表中，「[!UICONTROL (tp)]」會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(tp)」)。

* &lt;*轉換*>[!UICONTROL (sd)]： （選擇性）只包含在轉換路徑中只追蹤單一裝置的轉換。 在報表中，「[!UICONTROL (sd)]」會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(sd)」)。

* &lt;*轉換*>[!UICONTROL (xd)]： （選擇性）只包含在轉換路徑中追蹤多個裝置的轉換。 在報表中，「[!UICONTROL (xd)]」會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(xd)」)。

#### 如何解讀轉換報表

將跨裝置([!UICONTROL (xd)]/[!UICONTROL (tl)])總轉換率從高到低的百分比排序，以瞭解導致跨裝置轉換率高於平均值的因素。 您可以利用這一點來通知您的創意或目標定位策略，以便比對訊息和管道投資與使用者行為。

* 套件 — 檢視哪些套件帶來最多總轉換，以及哪些套件擁有高百分比的跨裝置轉換。 這有助於您瞭解應該將焦點放在何處。

* 刊登版位 — 比較刊登版位效能和歸因（例如，行動裝置網頁廣告可能會促進桌上型電腦的轉換）。 如果沒有用於歸因的裝置圖表，您可能會錯過行動網站版位對案頭轉換的影響，或者，如果大多數使用者在案頭而不是行動網站上轉換，該影響可能會被掩蓋。

* 廣告 — 探索哪些廣告可帶來較高的轉換率，並量化其價值以及在Web瀏覽器和行動應用程式環境中的影響。

* 網站 — 跨網站最佳化，而非完全手動排除網站。 如果網站進行跨裝置轉換，您就能檢視在哪些裝置上發生這種行為。

* 交易 — 透過驗證哪些庫存交易提供跨裝置轉換，然後決定您是否應擴大目標定位以在這些交易中包含更多裝置和管道，來改善手動最佳化。

>[!MORELIKETHIS]
>
>* [報告設定](/help/dsp/reports/report-settings.md)
>* [行銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
