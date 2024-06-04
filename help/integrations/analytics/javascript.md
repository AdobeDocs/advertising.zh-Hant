---
title: JavaScript程式碼 [!DNL Analytics for Advertising]
description: JavaScript程式碼 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# JavaScript程式碼 [!DNL Analytics for Advertising]

*僅使用Advertising DSP的廣告商*

若為Advertising DSP，則 [!DNL Analytics for Advertising] 整合會追蹤瀏覽和點進網站互動。 點進造訪會由您網頁上的標準Adobe Analytics程式碼加以追蹤； [!DNL Analytics] 程式碼會擷取登陸頁面URL中的AMO ID和EF ID引數，並在其各自的保留中追蹤 [!DNL eVars]. 您可以在網頁中部署JavaScript程式碼片段，以追蹤瀏覽次數。

在造訪網站的第一個頁面檢視上，Adobe Advertising的JavaScript程式碼會檢查訪客是否先前檢視或點選過廣告。 如果使用者先前曾透過點進進入網站，或尚未看到廣告，則會忽略該訪客。 如果訪客看過廣告，且未在期間透過點進進入網站 [按一下回顧視窗](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Adobe Advertising中設定，則Adobe AdvertisingJavaScript程式碼a)會使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 產生補充ID (`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 產生方法 `[!DNL StitchID]`. 其中一個ID可用來將Adobe Advertising中的資料拼接至訪客的Adobe Analytics點選。 Adobe Analytics接著會查詢Adobe Advertising與廣告曝光度相關聯的AMO ID和EF ID。 接著，AMO ID和EF ID會填入其各自的資料中 [!DNL eVars]. 這些值會在指定的期間（預設為60天）內持續存在。

[!DNL Analytics] 傳送網站流量量度（例如頁面檢視、造訪和逗留時間）和 [!DNL Analytics] 自訂或標準事件，每小時Adobe Advertising一次，使用EF ID作為索引鍵。 這些 [!DNL Analytics] 然後透過Adobe Advertising歸因系統執行的量度，將轉換連結到點選和曝光歷史記錄。

>[!NOTE]
>
>Adobe AdvertisingJavaScript追蹤邏輯發生在Adobe端，因此幾乎對頁面載入時間沒有影響。
>
>相反的，邏輯 [!DNL DCM] 資料聯結器至 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360])時，若變更為Advertising DSP，則發生在使用者端。 使用者端拚接會減緩頁面載入速度，並增加資料遺失的風險。 發生此狀況是因為 [!DNL Analytics] JavaScript必須ping [!DNL DoubleClick] 並等待 [!DNL DoubleClick] 將最後點選/曝光資料傳回至 [!DNL Analytics]. 當 [!DNL DSP] 團隊設定 [!DNL DCM] 資料聯結器，您必須指定您願意延遲頁面多久。

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## 部署JavaScript程式碼

JavaScript程式庫由兩行組成，允許 [!DNL Analytics] 和Adobe Advertising互相通訊。 如果 [!DNL Analytics for Advertising] 整合已在Adobe Advertising實作期間完成，則您應已收到此程式碼，及其部署說明。

### 代碼

#### 使用Experience CloudIdentity服務的實作 `visitorAPI.js` 程式碼

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### 使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`程式碼

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### 放置程式碼的位置

此 [!DNL Analytics for Advertising] JavaScript函式必須在Experience CloudID服務之後，Analytics App Measurement程式碼之前。 這可確保補充ID (`SDID`)或 `[!DNL StitchID]` 包含在您的Analytics呼叫中。

![程式碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包Sniffer型別的工具(例如 [!DNL Charles]， [!DNL Fiddler]，或 [!DNL Chrome Developer Tools])，比較即將前往請求和即將前往的請求之間的四個ID值Adobe Advertising [!DNL Analytics]，如下所述。

#### 如何使用確認程式碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 標籤。

1. 載入包含 [!DNL Analytics for Advertising] JavaScript。

1. 篩選 [!UICONTROL Network] 定位方式 `last` 並檢閱兩列：

   ![在上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一列是對JavaScript程式庫的呼叫，標題為 `last-event-tag-latest.min.js`.
   * 第二列是將請求傳送至Adobe Advertising的呼叫。 其開頭如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     如果您沒有看到對Adobe Advertising的呼叫，則該呼叫可能不是您造訪的第一個頁面檢視。 出於測試目的，您可以移除Cookie，讓下次呼叫是相應造訪的第一個頁面檢視：

   1. 在應用程式標籤上，找到 `adcloud` Cookie，並確認Cookie包含 `_les_v` （上次造訪）的值為 `y` 以及30分鐘後過期的UTC紀元時間戳記。
      1. 刪除 `adcloud` cookie並重新整理頁面。

1. (使用Experience Cloud Identity Service的實作 `visitorAPI.js` 代碼)篩選於 `/b/ss` 以檢視Analytics點選。

   ![篩選於 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼)篩選於 `/interact` 驗證傳送至Edge Network的要求裝載是否包含 `advertisingStitchID`.

   ![篩選於 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩個點選之間的ID值。 所有值都應位於查詢字串引數中，但Analytics點選中的報表套裝ID （即緊接在後面的URL路徑）除外 `/b/ss/`.

   | ID | Analytics引數 | Edge Network | Adobe Advertising引數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `advertisingStitchID` 在 `_adcloud` 屬性 |  |
   | Analytics報表套裝 | 之後的值 `/b/ss/` | | `_les_rsid` |
   | Experience Cloud訪客ID | mid |  | `_les_mid` |

   如果ID值相符，則會確認JavaScript實施。 Adobe Advertising傳送 [!DNL Analytics] 伺服器任何點進或檢視的追蹤詳細資訊（如果存在）。

#### 如何使用確認程式碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) ，請在您的首頁上。
1. 前往 [!UICONTROL Network] 標籤。
1. 在 [!UICONTROL Solutions Filter] 工具列，按一下 [!UICONTROL Adobe Advertising] 和 [!UICONTROL Analytics].
1. 在 [!UICONTROL Request URL - Hostname] 引數列，找出 `lasteventf-tm.everesttech.net`.
1. 在 [!UICONTROL Request - Parameters] 列，稽核產生的訊號，類似於中的步驟3 」[如何使用確認程式碼 [!DNL Chrome Developer Tools]](#validate-js-chrome).」
   * (使用Experience Cloud Identity Service的實作 `visitorAPI.js` 代碼)確認 `Sdid` 引數符合 `Supplemental Data ID` 在Adobe Analytics篩選中。
   * (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼)確認 `advertisingStitchID` 引數符合 `Sdid` 已傳送至Experience PlatformEdge Network。
   * 如果程式碼未產生，則檢查以確認Adobe AdvertisingCookie已在中移除 [!UICONTROL Application] 標籤。 移除後，請重新整理頁面並重複此程式。

   ![稽核 [!DNL Analytics for Advertising] 中的JavaScript程式碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising]](prerequisites.md)
