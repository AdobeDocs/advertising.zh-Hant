---
title: 在Adobe Target中設定Adobe Advertising DSP廣告的A/B測試
description: 瞭解如何在 [!DNL Target] 中為您的DSP廣告設定A/B測試。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
TQID: https://experienceleague.adobe.com/xETpACcZbZqfFjS58mS-k-kXhm0BT79W0aHz2bdKDGs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1645
ht-degree: 0%

---

# 在Adobe Target中為Advertising DSP廣告設定A/B測試

*僅使用Advertising DSP的廣告商*

Adobe Advertising和Adobe Target可讓行銷人員更輕鬆地透過付費媒體和站上訊息提供個人化和連線的體驗。 透過在產品之間共用訊號，您可以：

* Decrease site fall-through rates by linking customers’ ad exposure from DSP campaigns to their on-site experiences.

* Establish A/B testing by mirroring on-site experiences with advertising messaging using Adobe Audience Manager exposure data and click-to-feed [!DNL Target] audiences.

* Measure the impact of unified messaging on an on-site objective lift with simple visualizations in Adobe Analytics for [!DNL Target].

See the following sections for the prerequisites and for instructions to set up click-through and view-through tracking, implement signal sharing between DSP and [!DNL Target] and set up an A/B test activity, and set up [!DNL Analytics] Analysis Workspace to view the test data.

If you have additional questions, contact your Adobe Account Team.

## 先決條件

This use case requires the following products and integrations:

* [!DNL Target]

* [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (required for view-through testing only)

## Step 1: Set up the Click-through Framework {#click-through-framework}

![Click-through framework](/help/integrations/assets/target-ct-framework.png)

When you add DSP macros to a click-through URL (the URL displayed when a user clicks an ad and reaches the landing page), DSP automatically captures the placement key by including `${TM_PLACEMENT_ID}` in the click-through URL. This macro captures the alphanumeric placement key and not the numeric placement ID.

![Click-through URL appended to the landing page URL](/help/integrations/assets/target-ct-url.jpg)

### (DSP only) Add DSP macros to your click-through URLs

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Within [!DNL Flashtalking] or Google Campaign Manager 360, manually update the click-through URL for each ad to include the macros required to capture AMO ID variables. The AMO ID variables are used to send click data to Adobe Analytics and to share placement keys for A/B testing. See the following pages for instructions:

* [Append [!DNL Analytics for Advertising] macros to [!DNL Flashtalking] ad tags](/help/integrations/analytics/macros-flashtalking.md). **注意：**&#x200B;如果您的組織與[!DNL Flashtalking]有直接的合作關係，而且您根據[!DNL Flashtalking]支援檔案（位於[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)）中的`s_kwcid`與`ef_id`追蹤引數，則不需要執行此程式。

* [Append [!DNL Analytics for Advertising] macros to [!DNL Google Campaign Manager 360] ad tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Contact your Adobe Account Team to retrieve the required placement key and finalize the setup, and to make sure that each click-through URL is populated with the placement key.

## Step 2: Set up the view-through framework using Audience Manager {#view-through-framework}

![View-through framework](/help/integrations/assets/targetr-vt-framework.png)

By adding an Audience Manager impression event pixel in your ad tags and placement settings, you can create a test segment for additional view-through testing opportunities.

1. Implement an Audience Manager impression event pixel in your ad tags and DSP placement settings.

   For instructions, see &quot;[Collect media exposure data from Advertising DSP campaigns](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Make sure you add [DSP macros](/help/dsp/campaign-management/macros.md) to capture all data you want the impression event pixel to pass back, including `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

   >[!NOTE]
   >
   >Click-tracking URLs include the `${TM_PLACEMENT_ID}` macro for the alphanumeric placement key, instead of `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

1. Configure an Audience Manager segment from the DSP impression data:

   1. Verify that segment data is available:

      1. [Search for the signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) for the [key-value pair](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) that determines at what level the segment users are grouped.

         Use a [supported key](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) with a value that corresponds to a macro that you added to the Audience Manager impression event pixel.

         For example, to group users for a particular placement, use the `d_placement` key. For the value, use an actual numeric placement ID (such as 2501853) that&#39;s captured by the DSP macro `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         If the search results show user counts for the key-value pair, which indicates that the pixel was placed correctly and data is flowing, then continue to the next step.

   1. [Create a rule-based trait](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) for segment creation in Audience Manager.

      * Name the trait so that it’s easily identifiable within test activities. Store the trait in whichever folder you prefer.

      * Select `Ad Cloud` as the **[!UICONTROL Data Source]**.

      * For the trait expression, use `d_event` as the **[!UICONTROL Key]** and `imp` as the **[!UICONTROL Value]**.

   1. [Set up a test segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) for the new trait in Audience Manager, selecting `Ad Cloud` as the **[!UICONTROL Data Source]**.

      Audience Manager automatically splits the segment into a control group that receives the standard landing page experience and a test group that received a personalized onsite experience.

## Step 3: Set up an A/B test activity in [!DNL Target] for DSP

The following instructions highlight information pertaining to the DSP use case.

1. [Sign in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

      >[!NOTE]
      >
      >You can use multiple URLs to test view-through site entry. For more information, see &quot;[Multipage Activity](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; 您可以在Analytics中建立[網站專案報告](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports)，依頁面URL輕鬆識別熱門專案。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;欄位中輸入測試的成功量度。

      >[!NOTE]
      >
      >請確定[!DNL Analytics]已在[!DNL Target]內啟用為資料來源，且已選取正確的報表套裝。

   1. 將&#x200B;**[!UICONTROL Priority]**&#x200B;設為`High`或`999`，以防止測試區段中的使用者收到錯誤的站台體驗時發生衝突。

   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;內，選取連線至您DSP帳戶的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      如需其他報告秘訣，請參閱「[報告最佳實務和疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)」。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;欄位中，輸入適當的測試開始與結束日期。

   1. 將對象新增至活動：

      1. 選擇您先前在Audience Manager中建立的[區段，以測試閱覽對象](#view-through-framework)。

      1. 選取「**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**」，然後在「**[!UICONTROL Value]**」欄位中輸入DSP位置索引鍵，以使用點進對象的Target查詢字串引數。

   1. 針對&#x200B;**[!UICONTROL Traffic Allocation Method]**，選取&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;並以50/50分割對象。

   1. 儲存活動。

1. 使用[Target視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)，對A/B測試登入頁面範本進行設計變更。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用[!DNL Target]使用者介面，根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。

   >[!NOTE]
   >
   >例如創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟4：在[!DNL Analytics]中設定您的[!DNL Analytics for Target] Analysis Workspace

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商根據[!DNL Analytics]轉換量度和受眾區段來建立[!DNL Target]個活動，然後使用[!DNL Analytics]做為報表來源來測量結果。 該活動的所有報表和區段都以[!DNL Analytics]資料收集為基礎。

如需[!DNL Analytics for Target]的詳細資訊，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的報告來源&quot;。

### 設定[!DNL Analytics for Target]面板

在Analysis Workspace中，設定[!DNL Analytics for Target panel]以分析您的[!DNL Target]活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立面板，專用於執行測試的Adobe Advertising行銷活動、套件或位置。 使用摘要視覺效果，在與[!DNL Target]測試效能相同的報表中顯示Adobe Advertising量度。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與[!DNL Target]量度比對。

#### 維度

下列維度與[!DNL Analytics for Target]有關：

* **[!UICONTROL Target Activities]**： A/B測試的名稱

* **[!UICONTROL Target Experiences]**：活動中使用的登入頁面體驗名稱

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**：活動名稱和體驗名稱在同一列

### 疑難排解[!DNL Target]資料的Analytics

在Analysis Workspace中，如果您發現活動和體驗資料很少或未填入，則請執行以下操作：

* 確認相同的[!UICONTROL Supplemental Data ID] (SDID)同時用於[!DNL Target]和[!DNL Analytics]。 您可以在行銷活動驅動使用者的登陸頁面上使用[Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)，以驗證SDID值。

  [Adobe Debugger中的補充資料ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同登入頁面上，確認a) [!UICONTROL Solutions] > [!UICONTROL Target]底下之Adobe Debugger中顯示的[!UICONTROL Hostname]符合b)活動（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]底下） [!DNL Target]中顯示的[!UICONTROL Tracking Server]。

  [!DNL Analytics For Target]需要從[!DNL Target]傳送追蹤伺服器至Analytics之[!DNL Modstats]資料收集伺服器的呼叫中的[!DNL Analytics]追蹤伺服器。<!-- just "to Analytics?"-->

  [Adobe Debugger中的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace中設定[!DNL Target]報告。
* [A/B測試總覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 說明可搭配DSP廣告使用的A/B測試活動。
* [體驗與選件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) — 說明[!DNL Target]用來判斷DSP測試使用者公開之站上內容的工具。
* [訊號、特徵和區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) — 定義有助於進行DSP閱覽測試的一些Audience Manager工具。
* [總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) — 介紹[!DNL Analytics for Advertising]，它可讓您在Analytics執行個體中追蹤點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定Advertising Search、Social和Commerce廣告的A/B測試](ab-tests-search.md)
