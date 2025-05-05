---
title: ' [!DNL Analytics for Advertising]的JavaScript程式碼'
description: ' [!DNL Analytics for Advertising]的JavaScript程式碼'
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# [!DNL Analytics for Advertising]的JavaScript程式碼

*僅使用Advertising DSP的廣告商*

若為Advertising DSP，[!DNL Analytics for Advertising]整合會追蹤瀏覽和點進網站互動。 點進造訪會由您網頁上的標準Adobe Analytics程式碼追蹤；[!DNL Analytics]程式碼會擷取登陸頁面URL中的AMO ID和EF ID引數，並在其各自的保留[!DNL eVars]中追蹤。 您可以在網頁中部署JavaScript程式碼片段，以追蹤瀏覽次數。

在造訪網站的第一個頁面檢視上，Adobe AdvertisingJavaScript程式碼會檢查訪客是否先前檢視或按一下廣告。 如果使用者先前曾透過點進進入網站，或尚未看到廣告，則會忽略該訪客。 如果訪客在Adobe Advertising內設定的[點按回顧期間](/help/integrations/analytics/prerequisites.md#lookback-a4adc)內看到廣告且未透過點進進入網站，則Adobe AdvertisingJavaScript程式碼a)會使用[Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)產生補充ID (`SDID`)，或b)會使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID`方法產生`[!DNL StitchID]`。 其中一個ID可用來將Adobe Advertising中的資料拼接至訪客的Adobe Analytics點選。 Adobe Analytics接著會查詢Adobe Advertising與廣告曝光度相關聯的AMO ID和EF ID。 AMO ID和EF ID會填入各自的[!DNL eVars]中。 這些值會在指定的期間（預設為60天）內持續存在。

[!DNL Analytics]會使用EF ID做為索引鍵，將網站流量量度（例如頁面檢視、造訪和逗留時間）和任何[!DNL Analytics]個自訂或標準事件每小時Adobe Advertising一次。 這[!DNL Analytics]個量度接著會透過Adobe Advertising歸因系統執行，以將轉換連線到點按和曝光歷史記錄。

>[!NOTE]
>
>Adobe AdvertisingJavaScript追蹤邏輯發生在Adobe端，因此幾乎對頁面載入時間沒有影響。
>
>相反地，適用於Advertising DSP的[!DNL DCM]資料聯結器[!DNL Analytics] （使用[!DNL Google Campaign Manager 360]）的邏輯在使用者端發生。 使用者端拚接會減緩頁面載入速度，並增加資料遺失的風險。 發生此狀況是因為[!DNL Analytics] JavaScript必須Ping [!DNL DoubleClick]，並等待[!DNL DoubleClick]傳回上次點按/曝光資料給[!DNL Analytics]。 當您的[!DNL DSP]團隊設定[!DNL DCM]資料聯結器時，您必須指定您願意延遲頁面的時間。

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

JavaScript程式庫由兩行組成，允許[!DNL Analytics]和Adobe Advertising互相通訊。 如果[!DNL Analytics for Advertising]整合是在Adobe Advertising實作期間完成，則您應該已經收到此程式碼，以及部署它的說明。

### 代碼

#### 使用Experience Cloud識別服務`visitorAPI.js`程式碼的實作

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### 使用Experience Platform[!DNL Web SDK] `alloy.js`程式碼的實作

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### 放置程式碼的位置

[!DNL Analytics for Advertising] JavaScript函式必須在Experience CloudID服務之後，但在您的Analytics App Measurement程式碼之前。 這可確保在您的Analytics呼叫中包含補充ID (`SDID`)或`[!DNL StitchID]`。

![程式碼位置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包Sniffer型別的工具（例如[!DNL Charles]、[!DNL Fiddler]或[!DNL Chrome Developer Tools]）執行驗證，方法是比較將要Adobe Advertising的要求與將要[!DNL Analytics]的要求之間的四個ID值，如下所述。

#### 如何使用[!DNL Chrome Developer Tools]確認代碼 {#validate-js-chrome}

1. 開啟[!DNL Chrome Developer Tools]並按一下&#x200B;**網路**&#x200B;標籤。

1. 載入包含[!DNL Analytics for Advertising] JavaScript的網站頁面。

1. 依`last`篩選[!UICONTROL Network]索引標籤並檢閱兩列：

   ![在上一個](/help/integrations/assets/a4adc-code-validation-filter-last.png)篩選

   * 第一列是對JavaScript資料庫的呼叫，標題為`last-event-tag-latest.min.js`。
   * 第二列是將請求傳送至Adobe Advertising的呼叫。 其開頭如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     如果您沒有看到對Adobe Advertising的呼叫，則該呼叫可能不是您造訪的第一個頁面檢視。 出於測試目的，您可以移除Cookie，讓下次呼叫是相應造訪的第一個頁面檢視：

   1. 在[應用程式]索引標籤上，尋找`adcloud` Cookie，並確認該Cookie包含值為`y`的`_les_v` （上次造訪）以及30分鐘後過期的UTC epoch時間戳記。
      1. 刪除`adcloud` Cookie並重新整理頁面。

1. (使用Experience Cloud識別服務`visitorAPI.js`程式碼的實作)篩選`/b/ss`以檢視Analytics點選。

   ![正在篩選`/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用Experience Platform[!DNL Web SDK] `alloy.js`程式碼的實作)篩選`/interact`，以確認傳送至Edge Network的要求裝載包含`advertisingStitchID`。

   ![正在篩選`/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩個點選之間的ID值。 除了Analytics點選中的報表套裝ID （緊接在`/b/ss/`之後的URL路徑）以外，所有值都應位於查詢字串引數中。

   | ID | Analytics引數 | Edge Network | Adobe Advertising引數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `_adcloud`屬性下的`advertisingStitchID` |  |
   | Analytics報表套裝 | `/b/ss/`之後的值 | | `_les_rsid` |
   | Experience Cloud訪客ID | mid |  | `_les_mid` |

   如果ID值相符，則會確認JavaScript實施。 Adobe Advertising會將任何點進或檢視的追蹤詳細資訊（如果存在）傳送給[!DNL Analytics]伺服器。

#### 如何使用[!DNL Adobe Experience Cloud Debugger]確認代碼

1. 開啟首頁上的[[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=zh-Hant)。
1. 前往[!UICONTROL Network]標籤。
1. 在[!UICONTROL Solutions Filter]工具列中按一下[!UICONTROL Adobe Advertising]和[!UICONTROL Analytics]。
1. 在[!UICONTROL Request URL - Hostname]引數列中，找出`lasteventf-tm.everesttech.net`。
1. 在[!UICONTROL Request - Parameters]列中，稽核產生的訊號，類似於&quot;[如何使用 [!DNL Chrome Developer Tools]](#validate-js-chrome)確認程式碼&quot;中的步驟3。
   * (使用Experience Cloud識別服務`visitorAPI.js`程式碼的實作)確認`Sdid`引數符合Adobe Analytics篩選器中的`Supplemental Data ID`。
   * (使用Experience Platform[!DNL Web SDK] `alloy.js`程式碼的實作)確定`advertisingStitchID`引數的值與傳送給Experience PlatformEdge Network的`Sdid`相符。
   * 如果程式碼未產生，則檢查以確認Adobe AdvertisingCookie已在[!UICONTROL Application]索引標籤中移除。 移除後，請重新整理頁面並重複此程式。

   ![在[!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)中稽核[!DNL Analytics for Advertising] JavaScript程式碼

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)
