---
title: 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising]
description: 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising]

*廣告商DSP和[!DNL Advertising Search, Social, & Commerce]*

在將Adobe廣告與Adobe Analytics整合之前，請查看以下資訊。

## 中的報告Adobe廣告資料要求 [!DNL Analytics]

* 以下任一項：
   * Adobe Experience PlatformWeb SDK: `alloy.js`
   * Experience Cloud身份服務： `visitorAPI.js` 2.0版或更高版本
* 任何版本的Adobe Analytics(包括 [!DNL Prime]。 [!DNL Premium]或 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 版本2.1或更高版本

>[!TIP]
>
>要提高資料保真度，請使用每個庫的最新版本。

## 使用Adobe廣告共用分析段的要求

* Experience Cloud身份服務： `visitorAPI.js` 版本2.1或更高版本
* Adobe Analytics: `appMeasurement.js` 1.8版或更高版本

## 報告要求 [!DNL Analytics] Adobe廣告中的資料

向Adobe廣告實施團隊提供以下內容：

* 的 [!DNL Analytics] 報告套件ID，用於報告付費媒體活動和提供網站活動以優化和報告Adobe廣告
* 公司的Experience Cloud組織ID（組織ID）。

您可以在 [Adobe Experience Cloud調試器的「摘要」頁籤](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)。

![Experience Cloud Debugger摘要螢幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe廣告中的資料 {#lookback-a4adc}

因為 [!DNL Analytics] 資料被發送到Adobe廣告以進行報告和優化，資料受為Adobe廣告中的廣告商配置的屬性規則（包括印象和點擊回望窗口）的約束。

![廣告商級回望窗口設定在Adobe廣告中](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe廣告屬性按一下回望窗口：第一次按一下後的天數，在該天數內，按一下可歸屬於轉換。 預設情況下，此值為60天；最多90天
* Adobe廣告歸因印象回顧窗口：廣告印象後的天數，其中印象可歸因於轉換。 預設情況下，此值為14天；最多30天

   >[!NOTE]
   >
   > 「回望窗口」是針對Adobe廣告而非 [!DNL Analytics for Advertising]，報告。

的 [!DNL Analytics for Advertising] JavaScript使用這些設定來確定將瀏覽條目或點擊站點條目視為有效的時間。 有關如何確定視圖檢查和點擊檢查的詳細資訊，請參閱[Adobe分析使用的廣告ID](ids.md)&quot;

## Adobe廣告資料 [!DNL Analytics]

[!DNL Analytics] 在分析命中設定Adobe廣告ID(AMO ID)，但受廣告商的eVar持久性設定的影響，該設定既適用於點擊總覽又適用於視圖總覽。 持久性設定是在Adobe廣告後端配置的，您的Adobe帳戶團隊可以更改它。

* [!DNL Analytics for Advertising] eVar過期：預設情況下，AMO ID為60天

>[!NOTE]
>
>要將資料分段到不同的時間段，您可以 [設定自定義段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) 在Analysis Workspace有不同的後視窗。

## 支援的廣告環境

* 搜索
* 顯示
* 視頻
* 線上視頻
* 本機

請與您的Adobe客戶團隊聯繫，瞭解每個渠道中最新支援的廣告環境。

## 實施前要瞭解的事

* Adobe廣告實施團隊將建立整合。

* 此整合不會收取額外成本，伺服器調用也不會導致額外成本 [!DNL Analytics] 或Adobe廣告費。

* [!DNL Analytics for Advertising] 與ad伺服器無關：任何ad伺服器都可能出現查看或點擊操作，並在站點條目時生成正確的ID。

* 僅整合通過 [!DNL Analytics] Adobe廣告以優化後續付費媒體及廣告工作。 它沒有通過 [!DNL Analytics] 分段、計算度量和eVars以Adobe廣告以進行投標優化。

* Adobe廣告在 [!DNL Analytics] 根據用戶進入網站之前按一下或查看的上一個廣告， [按一下並查看全視回望窗口](#lookback-a4adc) 在Adobe廣告中配置。 如果站點訪問者在其配置檔案中具有兩種類型的站點條目交互，並且按一下處於回望期內，則訪問者的點擊ID將覆蓋站點報告的查看ID。

* [!DNL Analytics for Advertising] Adobe Analytics的轉換跟蹤使用可配置的跟蹤回望窗口（預設為60天）。 Adobe廣告報告反映了站點轉換和從此跟蹤回望窗口結束時的參與。

* 支援所有廣告類型。 但是，並非所有廣告環境都受支援。

   例如，由於CTV中不發生點擊，並且同一設備上不能進行轉換，因此無法跟蹤連接的TV(CTV)廣告。 但是，如果廣告在案頭環境中查看，則可能會跟蹤一些通過查看的站點條目資料。

* [!DNL Analytics] 轉換當前僅被跟蹤並被歸屬於同一設備上的訪問者。

* [!DNL Analytics for Advertising] 不支援應用程式內查看到轉換。

* 對於使用伺服器端轉發實現的廣告商，不支援直觀跟蹤 [!DNL Analytics]。

### 補充ID

為站點實施Experience Cloud身份服務後，將命中包含來自 [!DNL Analytics] 或Adobe廣告包含補充ID。

示例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為實現準確的資料整合，Adobe使用的所有廣告呼叫 [!DNL Analytics for Advertising] 傳遞內容或記錄目標度量的活動必須具有相應的 [!DNL Analytics] 擊到共用相同的補充ID。

在中進行故障排除時 [!DNL Analytics]，確保確認是否有補充ID [!DNL Analytics] 擊中。 在 [Adobe Experience Cloud調試器](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在「Adobe廣告」頁籤中將此ID作為 `sdid` 的下界。

>[!NOTE]
>
> 此實施與 [!DNL Analytics for Target] 整合。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [用於廣告分析的JavaScript代碼](/help/integrations/analytics/javascript.md)

