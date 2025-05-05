---
title: 實作 [!DNL Analytics for Advertising]的先決條件和關鍵資訊
description: 實作 [!DNL Analytics for Advertising]的先決條件和關鍵資訊
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 實作[!DNL Analytics for Advertising]的先決條件和關鍵資訊

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

在將Adobe Advertising與Adobe Analytics整合之前，請先檢閱下列資訊。

## 在[!DNL Analytics]中報告Adobe Advertising資料的需求

* 下列其中一項：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud識別服務： `visitorAPI.js`版本2.0或更新版本
* 任何版本的Adobe Analytics （包括[!DNL Prime]、[!DNL Premium]或[!DNL Ultimate]）
* Adobe Analytics： `appMeasurement.js`版本2.1或更新版本
* (Advertising DSP客戶)已在您的網頁中部署[Advertising DSP JavaScript程式碼片段](javascript.md)，以追蹤瀏覽次數。

>[!TIP]
>
>若要改善資料保真度，請使用每個程式庫的最新版本。

## 與Adobe Advertising共用Analytics區段的要求

* Experience Cloud識別服務： `visitorAPI.js` 2.1版或更新版本
* Adobe Analytics： `appMeasurement.js` 1.8版或更新版本

## 報告Adobe Advertising中[!DNL Analytics]資料的需求

向Adobe Advertising實作團隊提供下列專案：

* [!DNL Analytics]報告套裝ID，用於付費媒體活動的報告，以及饋送網站活動以最佳化及Adobe Advertising中的報告
* 公司的Experience Cloud組織ID （組織ID）。

您可以在Adobe Experience Cloud Debugger[&#128279;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)的摘要標籤上找到這兩個ID。

![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

## Adobe Advertising中的[!DNL Analytics]資料 {#lookback-a4adc}

由於[!DNL Analytics]資料已傳送至Adobe Advertising以進行報告和最佳化，因此資料受限於為Adobe Advertising中的廣告商設定的歸因規則，包括曝光和點按回顧期間。

![Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)中的廣告商層級回顧視窗設定

* Adobe Advertising歸因點按回顧期間：首次點按發生後的天數，其中點按可歸因於轉換。 預設值為60天，最大值為90天
* Adobe Advertising歸因曝光回顧期間：廣告曝光發生後，該曝光會歸因於轉換的天數。 預設值為14天，最大值為30天

  >[!NOTE]
  >
  > 印象回顧期間是特定於Adobe Advertising，而非[!DNL Analytics for Advertising]報告。

[!DNL Analytics for Advertising] JavaScript會使用這些設定來判斷多久以前會將檢視專案或網站的點進專案視為有效。 如需如何決定閱覽和點進的詳細資訊，請參閱[Analytics使用的Adobe AdvertisingID](ids.md)。

## 在[!DNL Analytics]中Adobe Advertising資料

[!DNL Analytics]會根據廣告商的[!DNL eVar]持續性設定（適用於點進和檢視），在Analytics點選中設定Adobe AdvertisingID (AMO ID)。 持續性設定是在Adobe Advertising後端設定，您的Adobe帳戶團隊可以加以變更。

* [!DNL Analytics for Advertising] [!DNL eVar]到期日：AMO ID預設為60天

>[!NOTE]
>
>若要針對不同的時間範圍分段資料，您可以在Analysis Workspace中[設定具有不同回顧視窗的自訂區段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)。

## 支援的廣告環境

* 搜尋
* 顯示
* 影片
* 線上視訊
* 連線電視
* 原生

如需每個頻道中最新支援的廣告環境，請聯絡您的Adobe客戶團隊。

## 實作前須知

* Adobe Advertising實作團隊會設定整合。

* 此整合不需額外付費，伺服器呼叫也不會產生額外的[!DNL Analytics]或Adobe Advertising費用。

* [!DNL Analytics for Advertising]與廣告伺服器無關：任何廣告伺服器都可能發生瀏覽或點進，並在網站專案時產生適當的ID。

* 整合只會傳遞[!DNL Analytics]個標準和自訂事件來Adobe Advertising後續付費媒體與廣告工作的競標最佳化。 它不會傳遞[!DNL Analytics]區段、計算量度和[!DNL eVars]來Adobe Advertising競標最佳化。

* Adobe Advertising會根據Adobe Advertising中設定的[點按及檢視回顧期間](#lookback-a4adc)，根據使用者進入網站前最後點按或檢視的廣告，在[!DNL Analytics]內建立永久ID。 如果網站訪客的設定檔中同時具有兩種型別的網站專案互動，且點按在回顧期間內，則訪客的點進ID會覆寫網站報表的點進ID。

* Adobe Analytics中的[!DNL Analytics for Advertising]轉換追蹤使用可設定的追蹤回顧期間（預設為60天）。 Adobe Advertising報表會反映在此追蹤回顧期間結束時的網站轉換和參與。

* 支援所有廣告型別。<!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* 目前已追蹤[!DNL Analytics]次轉換，且僅將其歸因給相同裝置上的訪客。

* [!DNL Analytics for Advertising]不支援應用程式內閱覽轉換。

* 使用[!DNL Analytics]的伺服器端轉送實作的廣告商不支援瀏覽追蹤。

### 補充ID

為網站實作Experience Cloud識別服務後，包含來自[!DNL Analytics]或Adobe Advertising之資料的點選將包含補充ID。

範例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了進行精確的資料整合，[!DNL Analytics for Advertising]活動用來傳遞內容或記錄目標量度的所有Adobe Advertising呼叫必須具有共用相同補充ID的對應[!DNL Analytics]點選。

當您在[!DNL Analytics]中進行疑難排解時，請務必確認[!DNL Analytics]點選有補充ID存在。 在[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)中，您可以在「Adobe Advertising」標籤中看到此ID為`sdid`引數。

>[!NOTE]
>
> 此實作的運作方式與[!DNL Analytics for Target]整合類似。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* 適用於Advertising的Analytics的[JavaScript程式碼](/help/integrations/analytics/javascript.md)
