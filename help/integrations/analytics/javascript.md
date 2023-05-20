---
title: JavaScript代碼 [!DNL Analytics for Advertising]
description: JavaScript代碼 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 96b71e8c99ee30254b4bdc4ef0cb8af359f64c5e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# JavaScript代碼 [!DNL Analytics for Advertising]

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

*僅包含廣告的DSP廣告商*

對於廣DSP告， [!DNL Analytics for Advertising] 整合跟蹤查看和點擊瀏覽站點交互。 點擊訪問按您網頁上的標準Adobe Analytics代碼進行跟蹤；這樣 [!DNL Analytics] 代碼捕獲登錄頁URL中的AMO ID和EF ID參數，並在各自的保留eVar中跟蹤它們。 通過在網頁中部署JavaScript代碼段，可以跟蹤查看訪問。

在訪問站點的首頁視圖上，Adobe廣告JavaScript代碼將檢查訪問者先前是否看過或按一下過廣告。 如果用戶以前通過點擊方式輸入了站點或未看到廣告，則訪問者將被忽略。 如果訪問者在訪問期間看到廣告，並且未通過點擊進入站點 [按一下「回望」窗口](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Adobe廣告中設定，然後Adobe廣告JavaScript代碼a)使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 生成補充ID(`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 生成方法 `[!DNL StitchID]`。 任何一個ID都用於將Adobe廣告中的資料縫合到訪問者的Adobe Analytics熱門節目中。 Adobe Analytics隨後查詢Adobe廣告，以查找與廣告曝光相關聯的AMO ID和EF ID。 AMO ID和EF ID隨後被填充到它們各自的eVar中。 這些值在指定期間（預設為60天）內持續。

[!DNL Analytics] 發送站點流量度量（如頁面視圖、訪問和花費的時間）和 [!DNL Analytics] 使用EF ID作為鍵，將自定義或標準事件Adobe每小時廣告。 這些 [!DNL Analytics] 然後，通過Adobe廣告分配系統來將轉換連接到按一下和曝光歷史記錄。

>[!NOTE]
>
>Adobe廣告JavaScript跟蹤邏輯發生在Adobe側，因此對頁面載入時間幾乎沒有影響。
>
>相反，我們的邏輯 [!DNL DCM] 資料連接器 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360]),DSP在客戶端進行廣告。 客戶端縫合降低了頁面負載並增加了資料丟失的風險。 這是因為 [!DNL Analytics] JavaScript必須ping [!DNL DoubleClick] 等待 [!DNL DoubleClick] 將上次按一下/印象資料傳回 [!DNL Analytics]。 當 [!DNL DSP] 團隊設定 [!DNL DCM] 資料連接器，必須指定您願意延遲頁面的時間。

## 部署JavaScript代碼

JavaScript庫由兩行組成，它們允許 [!DNL Analytics] 和Adobe廣告來相互溝通。 如果 [!DNL Analytics for Advertising] 整合在Adobe廣告實施期間完成，那麼您應該已經收到了此代碼以及如何部署它的說明。

### 代碼

#### 使用Experience Cloud身份服務的實現 `visitorAPI.js` 代碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### 使用Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### 代碼放置位置

的 [!DNL Analytics for Advertising] JavaScript函式必須位於Experience CloudID服務之後，但必須位於分析應用程式測量代碼之前。 這確保補充ID(`SDID`)或 `[!DNL StitchID]` 包含在分析呼叫中。

![代碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證代碼部署

可以使用任何資料包嗅探器類型的工具(如 [!DNL Charles]。 [!DNL Fiddler]或 [!DNL Chrome Developer Tools])，通過比較將要Adobe廣告的請求和將要發送的請求之間的四個ID的值 [!DNL Analytics]，如下所述。

#### 如何確認代碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 頁籤。

1. 載入包含 [!DNL Analytics for Advertising] JavaScript。

1. 篩選 [!UICONTROL Network] 頁籤 `last` 並查看兩行：

   ![上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一行是對JavaScript庫的調用，標題為 `last-event-tag-latest.min.js`。
   * 第二行是將請求發送到Adobe廣告的呼叫。 開始如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您未看到Adobe廣告的呼叫，則它可能不是您訪問的第一頁。 為了測試目的，您可以刪除cookie，以便下次調用將是相應訪問的第一個頁面視圖：
   1. 在「應用程式」頁籤上，查找 `adcloud` cookie ，並驗證cookie是否包含 `_les_v` (上次訪問，其值為 `y` 以及30分鐘後過期的UTC時間戳。
      1. 刪除 `ad cloud` cookie並刷新頁面。


1. (使用Experience Cloud標識服務的實現 `visitorAPI.js` 代碼)篩選 `/b/ss` 查看分析命中。

   ![篩選於 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用該Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼)篩選 `/interact` 驗證到邊緣網路的請求負載是否包含 `advertisingStitchID`。

   ![篩選於 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩個命中的ID值。 除分析命中的報告套件ID（即緊接在後面的URL路徑）外，所有值都將位於查詢字串參數中 `/b/ss/`。

   | ID | 分析參數 | 邊緣網路 | Adobe廣告參數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | 斯 |  | `_les_sdid` |
   | 縫合ID | stitchId | `advertisingStitchID` 下 `_adcloud` 屬性 |  |
   | 分析報告套件 | 之後的值 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud訪問者ID | 中 |  | `_les_mid` |

   如果ID值匹配，則確認JavaScript實現。 Adobe廣告將發送 [!DNL Analytics] 伺服器任何按一下或查看跟蹤詳細資訊（如果存在）。

#### 如何確認代碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 首頁上。
1. 轉到 [!UICONTROL Network] 頁籤。
1. 在 [!UICONTROL Solutions Filter] 工具欄，按一下 [!UICONTROL Adobe Advertising] 和 [!UICONTROL Analytics]。
1. 在 [!UICONTROL Request URL – Hostname] 參數行，定位 `lasteventf-tm.everesttech.net`。
1. 在 [!UICONTROL Request – Parameters] 行，審核生成的信號，類似於「」中的步驟3[如何確認代碼 [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;
   * (使用Experience Cloud標識服務的實現 `visitorAPI.js` 代碼)確保 `Sdid` 參數匹配 `Supplemental Data ID` 在Adobe Analytics過濾器上。
   * (使用該Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼)確保 `advertisingStitchID` 參數匹配 `Sdid` 發送到Experience Platform邊緣網路。
   * 如果未生成代碼，則檢查以確保Adobe廣告cookie已在 [!UICONTROL Application] 頁籤。 刪除後，刷新頁面並重複該過程。

   ![審計 [!DNL Analytics for Advertising] JavaScript代碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)

