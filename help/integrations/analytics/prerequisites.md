---
title: 實施的先決條件和重要資訊 [!DNL Analytics for Advertising]
description: 實施的先決條件和重要資訊 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 實施的先決條件和重要資訊 [!DNL Analytics for Advertising]

*擁有廣告DSP和[!DNL Advertising Search, Social, & Commerce]*

在整合 Adobe Systems Advertising 與 Adobe Analytics 之前，請檢閱下列資訊。

## 在中報告Adobe Systems廣告數據的要求 [!DNL Analytics]

* 以下任一操作：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud Identity Service： `visitorAPI.js` 版本 2.0 或更高版本
* 任何版本的 Adobe Analytics （包括 [!DNL Prime]、 [!DNL Premium]或 [!DNL Ultimate]）
* Adobe Analytics： `appMeasurement.js` 2.1 版或更高版本
* （廣告DSP客戶）部署 [在您的網页中以追踪視圖瀏覽的廣告DSP JavaScript段](javascript.md) 。

>[!TIP]
>
>若要提高數據保真度，請使用每個資料庫的最新版本。

## 與 Adobe Systems Advertising 共用Analytics區段的需求

* Experience Cloud Identity Service： `visitorAPI.js` 版本 2.1 或更高版本
* Adobe Analytics： `appMeasurement.js` 版本 1.8 或更高版本

## Adobe Systems廣告中報告 [!DNL Analytics] 數據的要求

向Adobe Systems廣告實施 團隊提供以下內容：

* 該 [!DNL Analytics] 報告套裝 ID用于付費媒體 活動上的報告以及饋送網站活動，以便在Adobe Systems廣告中進行優化和報告
* 公司的Experience Cloud組織ID（組織ID）。

您可以在 Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 的摘要標籤中找到這兩個 ID[。

![Experience Cloud偵錯器摘要螢幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe Systems廣告中的數據 {#lookback-a4adc}

由於數據會發送到Adobe Systems廣告進行報告和優化，因此 [!DNL Analytics] 數據受歸因規則的約束，包括印象和點擊回顧窗口，這些規則是為Adobe Systems廣告中的廣告商配置的。

![Adobe Systems Advertising 中廣告商層級回顧窗口設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Systems廣告歸因點擊回顧期間：首次點擊發生后，可將點擊歸因於轉換的天數。 默認情況下，此值為 60 天;上限為90天
* Adobe Systems廣告歸因 印象回顧期間：發生廣告印象後，印象可歸因於轉換的天數。 默認情況下，此值為14天;上限為30天

  >[!NOTE]
  >
  > 印象回顧期間特定於Adobe Systems廣告，而不是 [!DNL Analytics for Advertising]報告。

[!DNL Analytics for Advertising] JavaScript使用這些設置來確定將網站的視圖輸入或點擊輸入視為有效的回溯時間。有關如何確定視圖次數和點進次數的更多資訊，請參閱“[Adobe Systems Analytics](ids.md)使用的廣告 ID”。

## Adobe Systems廣告數據 [!DNL Analytics]

[!DNL Analytics] 在Analytics 點擊內設定Adobe Systems廣告 ID （AMO ID），但須遵守廣告商 [!DNL eVar] 的持續性設定，該設定適用於點進和視圖進。 持久性設置是在 Adobe Systems 廣告後端配置的，Adobe Systems 帳戶團隊可以更改它。

* [!DNL Analytics for Advertising][!DNL eVar]過期時間： AMO ID 預設為 60 天

>[!NOTE]
>
>要區段不同時間範圍的數據，您可以在 [Analysis Workspace 中設置具有不同回溯期的自定義区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) 。

## 支援的廣告環境

* 搜索
* 顯示
* 影片
* 在線影片
* 已連接的TV
* 本地

請連絡您的Adobe Systems客戶團隊，以了解各通道支援的最新廣告環境。

## 實作前須知

* Adobe Systems廣告實施 團隊會設定整合。

* 不會為此集成支付額外費用，伺服器調用也不會產生額外 [!DNL Analytics] 或Adobe Systems廣告費用。

* [!DNL Analytics for Advertising] 與廣告伺服器無關：任何廣告伺服器都可能發生視圖或點進，並且進入網站時會生成正確的 ID。

* 集成僅 [!DNL Analytics] 將標準和自定義事件傳遞到 Adobe Systems 廣告，以便競標優化後續付費媒體和廣告工作。 它不會傳遞 [!DNL Analytics] 區段、計算量度和 [!DNL eVars] Adobe Systems 廣告以進行競標優化。

* Adobe Systems Advertising 會根據用戶進入網站之前點擊或查看的最後一個廣告，根據Adobe Systems廣告中配置的[點擊和視圖回溯視窗](#lookback-a4adc)，在 Advertising [!DNL Analytics] 中創建永久 ID。如果網站訪客在其設定檔内同時具有兩種類型的網站進入互動，並且點擊在回顧期内，則訪客的點進 ID 將覆蓋網站報告的視圖 ID。

* [!DNL Analytics for Advertising] 轉換 Adobe Analytics 中的追蹤使用可設定的追蹤回顧期間 （依預設為 60 天）。 Adobe Systems廣告報表會反映網站轉換和追蹤回顧期間結束前的參與數據。

* 支持所有廣告類型。 但是，並非所有廣告環境都受支援。

* [!DNL Analytics] 目前只會追踪轉換，並僅歸於同裝置的訪客。

* [!DNL Analytics for Advertising] 不支持應用內視圖轉換。

* 使用 伺服器端 [!DNL Analytics]轉送實施的廣告主不支持檢視追踪。

### 補充ID

在網站上實作 Experience Cloud Identity Service 後，若點擊包含廣告數據或廣告Adobe Systems [!DNL Analytics] 即會包含補充 ID。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了準確集成數據，活動用於傳遞內容或記錄目標量度的所有Adobe Systems廣告呼叫 [!DNL Analytics for Advertising] 都必須具有共享相同補充 ID 的相應 [!DNL Analytics] 點擊。

在 中進行 [!DNL Analytics]疑難解答時，請確認點擊中有 [!DNL Analytics] 補充ID。 在 Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 中[，您可以在 Adobe Systems Advertising 標籤看到此 ID 做為`sdid`參數。

>[!NOTE]
>
> 此實施的工作方式與 [!DNL Analytics for Target] 整合類似。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [廣告Analytics JavaScript Code](/help/integrations/analytics/javascript.md)
