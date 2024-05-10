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

Advertising DSP與整合 [!DNL LiveRamp] 可讓您將對象擴充至所有個人的已知裝置，而不只是您的品牌已追蹤的裝置。 此整合也提供所有裝置的頻率限定和歸因測量。

使用支援的以人物為基礎的裝置圖表時，您可以：

* 跨管道和裝置比對受眾，將廣告傳送給個人和家庭，而非裝置。
* 透過瞭解並限定跨個人的頻率來平衡廣告曝光。
* 測試跨管道或裝置公開與轉換對象的策略。

## 的優點 [!DNL LiveRamp] 裝置圖表

* 提供確定性資料集區，包括離線客戶資料

* 在Cookie ID和行動裝置ID之間提供均勻的涵蓋範圍

* 包括主要來自美國的資料

* 免費提供頻率限定和歸因測量

* 價格為$0.35 CPM的延長曝光次數(僅透過使用 [!DNL LiveRamp] 裝置圖表，而不是在目標受眾區段內找到的裝置上)

  費率會反映在您的帳戶費率卡上。

## 以人物為基礎的頻率管理

以人物為基礎的頻率管理可讓您在人員層級（而非裝置層級）指定真正的媒體曝光控制的頻率上限。

### 啟用以人物為基礎的頻率管理

* **行銷活動：** 建立新行銷活動時，您可以指定 [!UICONTROL Cross-Device Level] 設定。 啟用&quot;[!UICONTROL Same Device]「 -> 」[!UICONTROL People]、」並選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置目標定位，以及行銷活動、封裝和位置層級的人員型頻率管理。 頻率上限適用於個人所有已知裝置。

如需詳細資訊，請參閱 [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

儲存行銷活動後，就無法變更其 [!UICONTROL Cross Device Level] 設定。

* **封裝：**  您可以選擇在封裝層級設定額外的頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

* **版位：** 您可以選擇在版位層級設定額外的頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

## 以人物為基礎的鎖定目標

以人物為基礎的鎖定目標可讓您在桌上型電腦和行動裝置上尋找客戶。

### 啟用以人物為基礎的鎖定目標

* **行銷活動：** 建立新行銷活動時，您可以指定 [!UICONTROL Cross-Device Level] 設定。 啟用&quot;[!UICONTROL Same Device]「 -> 」[!UICONTROL People]、」並選取裝置圖表。 指定的裝置圖表會用於位置層級的跨裝置目標定位和以人物為基礎的頻率管理。

如需詳細資訊，請參閱 [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **版位：** 當您使用指定的裝置圖表選取行銷活動中某個位置的對象目標時， [!UICONTROL Cross-Device Targeting] 選項可讓您將目標定位擴充至所有人的所有已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段中的裝置。

### 設定以人物為基礎的鎖定目標報告

您可以在自訂報表中包含下列量度：

* **延伸曝光次數：** (在 [!UICONTROL Build Your Report] 區段在 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics])運用裝置圖表提供的遞增曝光量（未在原始受眾區段中找到）。 此量度也可用來計算與使用協力廠商裝置圖表相關的適用費用。

  若要判斷特定時段內延長曝光的成本，請執行包含 [!UICONTROL Extended Impressions] 欄，然後將延伸曝光總數乘以$0.00035 （$0.35/1000曝光數）。

  彙總成本也包含在 [!UICONTROL Billable Other Net Spend] 欄（下） [!UICONTROL Metrics] > [!UICONTROL Spend])，不過該量度也包含您可能已新增的其他行銷活動費用。

* **裝置圖表：** (在 [!UICONTROL Build Your Report] 區段在 [!UICONTROL Dimensions] > [!UICONTROL Campaign])為特定行銷活動、封裝或位置選取的裝置圖表。

## 以人物為基礎的歸因測量

*僅具有Adobe Advertising轉換追蹤的廣告商*

使用以人物為基礎的歸因，您可以將發生在不同裝置上的轉換歸因於發生媒體曝光的裝置。 以人物為基礎的歸因測量，可在DSP中使用， [!DNL Adobe Advertising Creative]、和 [!DNL Adobe Advertising Search, Social, & Commerce] 已在其網站上實施Adobe Advertising轉換畫素的廣告商。

### 啟用以人物為基礎的歸因測量

如果您想要啟用跨裝置歸因測量，請聯絡您的Adobe客戶團隊。

### 設定跨裝置轉換歸因的轉換報表

#### 轉換報表設定

啟用裝置圖表進行歸因測量時， [!UICONTROL Conversion] 報告包含 [!UICONTROL Cross-Device Breakout] 設定，可讓您針對每個轉換量度包含最多三個個別的欄，包括：

* &lt;*轉換*>[!UICONTROL (tp)]：包括總轉換次數（總人數），其中包含相同裝置轉換次數和跨裝置轉換次數（如果適用）。 在報表中， 」[!UICONTROL (tp)]&quot;會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(tp))。

* &lt;*轉換*>[!UICONTROL (sd)]：（選用）僅包含已在轉換路徑中追蹤單一裝置的轉換。 在報表中， 」[!UICONTROL (sd)]&quot;會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(sd))。

* &lt;*轉換*>[!UICONTROL (xd)]：（選用）僅包含已在轉換路徑中追蹤多個裝置的轉換。 在報表中， 」[!UICONTROL (xd)]&quot;會附加至轉換路徑中的轉換量度名稱、規則型別和轉換型別(例如「Responses(le)(tl)(xd))。

#### 如何解讀轉換報表

排序跨裝置轉換總數百分比([!UICONTROL (xd)]/[!UICONTROL (tl)])從高到低，以瞭解帶動高於平均數跨裝置轉換的因素。 您可以利用這一點來通知您的創意或目標定位策略，以便比對訊息和管道投資與使用者行為。

* 套件 — 檢視哪些套件帶來最多總轉換，以及哪些套件擁有高百分比的跨裝置轉換。 這有助於您瞭解應該將焦點放在何處。

* 刊登版位 — 比較刊登版位效能和歸因（例如，行動裝置網頁廣告可能會促進桌上型電腦的轉換）。 如果沒有用於歸因的裝置圖表，您可能會錯過行動網站版位對案頭轉換的影響，或者，如果大多數使用者在案頭而不是行動網站上轉換，該影響可能會被掩蓋。

* 廣告 — 探索哪些廣告可帶來較高的轉換率，並量化其價值以及在Web瀏覽器和行動應用程式環境中的影響。

* 網站 — 跨網站最佳化，而非完全手動排除網站。 如果網站進行跨裝置轉換，您就能檢視在哪些裝置上發生這種行為。

* 交易 — 透過驗證哪些庫存交易提供跨裝置轉換，然後決定您是否應擴大目標定位以在這些交易中包含更多裝置和管道，來改善手動最佳化。

>[!MORELIKETHIS]
>
>* [報表設定](/help/dsp/reports/report-settings.md)
>* [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
