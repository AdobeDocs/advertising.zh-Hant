---
title: 為Adobe Target的Adobe廣告配置A/BTest
description: 瞭解如何在中設定A/Btest [!DNL Target] 為DSP你 [!DNL Search, Social, & Commerce] 廣告。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# 配置Adobe Target的A/BTest，用於DSP廣告 [!DNL Advertising Search, Social, & Commerce] 廣告

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*僅包含廣告的DSP廣告商*

Adobe廣告和Adobe Target使營銷人員更容易通過付費媒體和現場消息傳遞個性化和互聯的體驗。 通過在產品之間共用信號，您可以：

* 通過將客戶的廣告暴露從市場活動與其現場體驗DSP相關聯，降低站點漏洞率。

* 通過使用Adobe Audience Manager曝光資料和點擊式目標受眾來鏡像廣告消息的現場體驗，建立A/B測試。

* 測量統一消息傳遞對現場目標提升的影響，在Adobe Analytics以簡單的可視化方式 [!DNL Target]。

請參閱以下各節瞭解先決條件以及設定點擊和查看跟蹤、實現和之間的信號共用DSP的說明 [!DNL Target] 設定A/Btest活動， [!DNL Analytics] Analysis Workspace查看test資料。

如有其他問題，請聯繫adcloud_support@adobe.com。

## 先決條件

此使用情形需要以下產品和整合：

* [!DNL Target]

* [[!DNL Analytics] 廣告](/help/integrations/analytics/overview.md) 整合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 為 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合

* Audience Manager（僅用於直觀測試）

## 步驟1:設定「點擊」框架 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![點擊式框架](/help/integrations/assets/target-ct-framework.png)

將宏添DSP加到點擊式URL（當用戶按一下廣告並到達登錄頁時顯示的URL）時，會通過DSP包括 `${TM_PLACEMENT_ID}` 的子菜單。 此宏捕獲字母數字放置鍵，而不捕獲數字放置ID。

![附加到登錄頁URL的點擊式URL](/help/integrations/assets/target-ct-url.jpg)

### (DSP僅)將DSP宏添加到按一下URLS

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash通話或Google市場活動經理360中，手動更新每個廣告的點擊URL，以包括捕獲AMO ID變數所需的宏。 AMO ID變數用於向Adobe Analytics發送按一下資料並共用A/B測試的放置鍵。 有關說明，請參閱以下頁：

* [追加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)

* [追加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

聯繫您的Adobe客戶小組和廣告解決方案組(aac-advertising-solutions-group@adobe.com)以檢索所需的放置密鑰並完成設定，並確保每個點擊URL都填充了放置密鑰。

## 步驟2:使用Audience Manager設定查看框架 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![透視框架](/help/integrations/assets/targetr-vt-framework.png)

通過在廣告標籤和放置設定中添加Audience Manager印象事件像素，可以為其他查看測試機會建立test段。

1. 在廣告標籤和放置設定中實施Audience Manager印象事DSP件像素。

   有關說明，請參見「」[從廣告活動中收集媒體曝光數DSP據](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;

   確保添加 [DSP宏](/help/dsp/campaign-management/macros.md) 捕獲希望印象事件像素回傳的所有資料，包括 `${TM_PLACEMENT_ID_NUM}` 的子菜單。

   >[!NOTE]
   >
   >按一下跟蹤URL包括 `${TM_PLACEMENT_ID}` 用於字母數字放置鍵的宏，而不是 `${TM_PLACEMENT_ID_NUM}` 的子菜單。

1. 根據印象資料配DSP置Audience Manager段：

   1. 轉到 **Audience Manager** > **受眾資料** > **信號**，然後選擇 **搜索** 的下界。

   1. 輸入 **鍵** 和 **值** 確定段用戶分組的級別的信號。 使用 [支援的密鑰](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) 與添加到Audience Manager印象事件像素的宏對應的值。

      例如，要將用戶分組到特定位置，請使用 `d_placement` 按鈕 對於該值，請使用宏捕獲的實際數字放置ID(如上面的螢幕抓圖中的2501853DSP) `${TM_PLACEMENT_ID_NUM}`。 <!-- Explain where to find the placement ID, other than in a custom report. -->

      如果「總計數」欄位顯示鍵值對的用戶計數，這表示像素已正確放置且資料正在流動，則可以繼續下一步。
   ![搜索信號](/help/integrations/assets/target-am-signals.png)

1. [建立基於規則的特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 用於在Audience Manager中建立段。

   1. 說出特徵，以便在test活動中很容易識別。 將特性儲存在您喜歡的資料夾中。

   1. 從 **資料源** 下拉菜單，選擇 **Ad Cloud**。

   1. 在表達式生成器中，添加 `d_event` 鍵欄位和 `imp` 的 **值** 欄位，選擇 **添加規則**，然後保存這個特徵。

   ![基於規則的特徵截圖](/help/integrations/assets/target-am-trait.png)

1. 在Audience Manager中設定test段：

   1. 在頁面頂部，轉到 **受眾資料** > **性狀** 並搜索全性狀名。 選中特徵名稱旁邊的複選框，然後按一下 **建立段**。

   1. 命名段，選擇 `Ad Cloud` 的 **資料源**，然後保存段。

      Audience Manager會自動將該段拆分為一個控制組和一個test組，前者接收標準登錄頁體驗，後者接收個性化的現場體驗。
   ![test段的螢幕快照](/help/integrations/assets/target-am-segment.png)

## 第3步：在目標中設定「A/BTest」活動

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

以下說明突出顯示與使用案例DSP有關的資訊。 有關完整說明，請參見「」[建立A/BTest](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)。

1. [登錄Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. 從 **活動** 清單，按一下 **建立活動** > **A/BTest**。

   ![建立A/BTest活動](/help/integrations/assets/target-create-ab.png)

1. 在 **輸入活動URL***欄位，輸入test的登錄頁URL。

   ![輸入活動URL欄位](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >可以使用多個URL來test通過查看的站點條目。 有關詳細資訊，請參閱「」[多頁活動](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)&quot; 通過建立 [站點條目報告](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) 分析。

1. 在 **目標** 欄位，輸入test的成功度量。

   >[!NOTE]
   >
   >確保 [!DNL Analytics] 在中作為資料源啟用 [!DNL Target]，並選擇正確的報告套件。

1. 設定 **優先順序** 至 `High` 或 `999` 當test段中的用戶收到不正確的現場體驗時防止衝突。

1. 在 **報告設定**，選擇 **公司名稱** 和 **報表套件** 已連接到你的DSP帳戶。

   有關其他報告提示，請參閱[報告最佳做法和故障排除](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)&quot;

1. 在 **日期範圍** 欄位中，輸入相應的起始和終止日期以進行test。

1. 將受眾添加到活動：

   1. 選擇 [先前在Audience Manager中建立的段，以test通過觀眾查看](#view-through-framework)。

      ![向活動添加受眾](/help/integrations/assets/target-create-ab-audiences.png)

   1. 選擇 **網站頁** > **登錄頁** > **查詢**，並在中DSP輸入放置鍵 **值** 欄位，用於使用「目標」查詢字串參數進行按一下訪問。

      ![目標按一下受眾的螢幕快照](/help/integrations/assets/target-click-audience.jpg)

1. 對於 **流量分配方法**&#x200B;選中 **手動（預設）** 然後把觀眾分成50/50

1. 保存活動。

1. 使用 [!DNL Target] [視覺體驗作曲家](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 對A/Btest登錄頁模板進行設計更改。

   * 經驗A:不要編輯，因為它是預設/控制登錄頁體驗，沒有個性化。

   * 經驗B:使用 [!DNL Target] 介面，根據test中包括的資產（如標題、副本、按鈕位置和創意）自定義登錄頁模板。
   >[!NOTE]
   >
   >例如，創意test使用案例，請與Adobe客戶團隊聯繫。

## 第4步：設定 [!DNL Analytics for Target] Analysis Workspace [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是一種跨解決方案整合，它讓廣告商能夠建立 [!DNL Target] 基於 [!DNL Analytics] 轉換度量和受眾段，然後使用 [!DNL Analytics] 作為報告源。 該活動的所有報告和細分都基於 [!DNL Analytics] 資料收集。

有關 [!DNL Analytics for Target]，包括指向實施說明的連結，請參見「[Adobe Analytics為Adobe Target(A4T)的報告來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)。

### 設定 [!DNL Analytics for Target] 面板

在Analysis Workspace，配置 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活動和經驗。 請記住以下有關報告的重要指針和資訊。

#### 度量

* 在工作區中建立特定於Adobe廣告活動、包或為其運行test的位置的面板。 使用摘要可視化在與目標Adobe效能相同的報告中顯示test廣告度量。

* 優先使用現場指標（如訪問和轉換）來衡量效能。

* 瞭解Adobe廣告（如印象、點擊量和成本）中的聚合媒體度量無法與目標度量相匹配。

#### Dimension

以下維與 [!DNL Analytics for Target]:

* **目標活動**:A/BTest的名稱

* **目標體驗**:活動中使用的登錄頁體驗的名稱

* **目標活動** > **經驗**:同一行中的活動名稱和體驗名稱

### 疑難解答分析 [!DNL Target] 資料

在Analysis Workspace，如果您注意到活動和體驗資料很少或沒有填充，請執行以下操作：

* 驗證是否將同一補充資料ID(SDID)用於目標和分析。 可以使用 [Adobe Experience Cloud調試器](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在該活動吸引用戶的登錄頁上。

[Adobe調試器中的補充資料ID(SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登錄頁上，驗證a)Adobe調試器中「Solutions> Target」下顯示的主機名與b)中顯示的跟蹤伺服器是否匹配。 [!DNL Target] （在「目標和設定」>「報告設定」下）。

   [!DNL Analytics For Target] 需要 [!DNL Analytics] 跟蹤伺服器從發送呼叫 [!DNL Target] 到 [!DNL Modstats] 用於分析的資料收集伺服器。<!-- just "to Analytics?"-->

[Adobe調試器中的主機名值](/help/integrations/assets/target-troubleshooting-hostname.png)

[跟蹤目標中的伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將目標與分析整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace設定目標報告。
* [A/BTest概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 介紹A/Btest活動，可與廣告一起使DSP用。
* [體驗和優惠](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 解釋 [!DNL Target] 工具，確定test用戶所接觸DSP的現場內容。
* [信號、特徵和段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定義一些Audience Manager工具，這些工具可幫DSP助進行查看測試。
* [廣告分析概述](/help/integrations/analytics/overview.md)  — 引入Analytics for Advertising，它允許您跟蹤Analytics實例中的點擊式和查看式站點交互。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
