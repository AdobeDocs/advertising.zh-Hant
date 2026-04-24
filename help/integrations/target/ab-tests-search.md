---
title: 在Adobe Target中設定Adobe Advertising Search、Social和Commerce廣告的A/B測試
description: 瞭解如何在 [!DNL Target] 中為搜尋、社交和Commerce中的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 廣告設定A/B測試。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
TQID: https://experienceleague.adobe.com/eu1dRdsQlJX4IlHLTUDyJ69r0txFvFUdzUiXpSAlpU8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 0%

---

# 在Adobe Target中設定Advertising Search、Social和Commerce廣告的A/B測試

*僅使用Advertising Search、Social和Commerce的廣告商*

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

Adobe Advertising和Adobe Target可讓您輕鬆為數位廣告流量[!DNL Google Ads]和[!DNL Microsoft Advertising]設定登陸頁面體驗A/B測試，以：

* 改善轉換率(CVR)和贏取效率測量（例如CPA、CPL和CAC）。

* 提供與廣告相關的更個人化的登陸頁面體驗（例如，比對登陸頁面的影像/影片創意、復本、關鍵字或其他廣告訊號）。

您也可以結合Advertising[&#128279;](/help/integrations/analytics/overview.md)的原生[[!DNL Analytics] 與整合至Adobe Analytics的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)整合報表維度的[!DNL Analytics] ，以透過[!DNL Analytics]量度和成功事件測量及視覺化您的測試資料。

請參閱下列各節以瞭解先決條件、在[!DNL Target]中設定A/B測試的指示（來自Search、Social和Commerce中的廣告點進流量），以及如何在[!DNL Analytics]中測量和視覺化測試的秘訣。

## 先決條件

### 必要產品

* 搜尋、社交和Commerce
* [!DNL Target]

### 建議的產品和整合

* [!DNL Analytics]

* 用於Advertising[&#128279;](/help/integrations/analytics/overview.md)整合的[!DNL Analytics] <!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 用於 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)整合

## Step 1: Create an A/B test activity in [!DNL Target] for Search, Social, &amp; Commerce

The following instructions highlight information pertaining to the Search, Social, &amp; Commerce use case.

1. [Sign in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

   1. In the **[!UICONTROL Goal]** field, enter the success metric for the test.

      >[!NOTE]
      >
      >Make sure that [!DNL Analytics] is enabled as a data source within [!DNL Target], and that the correct report suite is selected.

   1. Set the **[!UICONTROL Priority]** to `High` or `999` to prevent conflicts when users in the test segment receive an incorrect on-site experience.


   1. Within **[!UICONTROL Reporting Settings]**, select the **[!UICONTROL Company Name]** and **[!UICONTROL Report Suite]** connected to your Search, Social, &amp; Commerce account.

      For additional reporting tips, see &quot;[Reporting best practices and troubleshooting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In the **[!UICONTROL Date Range]** field, enter the appropriate start and end dates for the test.

   1. Select **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In the **[!UICONTROL Value]** field, enter the [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], or [!UICONTROL Network Ad ID] for the relevant ad network entity in Search, Social, &amp; Commerce. This allows you to use the [!DNL Target] query string parameters for click-through audiences for the entity.

      You can find the ID by [adding the relevant ID column to the entity view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view")

      Work with your Adobe Account Team if you need assistance.

   1. For the **[!UICONTROL Traffic Allocation Method]**, select **[!UICONTROL Manual (Default)]** and split the audience 50/50.

   1. Save the activity.

1. Use [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) to make design changes to the A/B test landing page template.

   * Experience A: Don&#39;t edit because it&#39;s the default/control landing page experience without personalization.

   * Experience B: Use the [!DNL Target] user interface to customize the landing page template based on the assets included in the test (such as headlines, copy, button placement, and creatives).

   >[!NOTE]
   >
   >For example creative test use cases, contact your Adobe Account Team.

## Step 2: Set up your [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) is a cross-solution integration that lets advertisers create [!DNL Target] activities based on [!DNL Analytics] conversion metrics and audience segments and then measure the results using [!DNL Analytics] as the reporting source. 該活動的所有報表和區段都以[!DNL Analytics]資料收集為基礎。

如需[!DNL Analytics for Target]的詳細資訊，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的報告來源&quot;。

### 設定[!DNL Analytics for Target]面板

在Analysis Workspace中，設定[!DNL Analytics for Target panel]以分析您的[!DNL Target]活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立面板，專用於執行測試的Adobe Advertising帳戶、行銷活動或廣告群組<!-- only applicable entities? -->。 使用摘要視覺效果，在與[!DNL Target]測試效能相同的報表中顯示Adobe Advertising量度。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與[!DNL Target]量度比對。

#### 維度

下列維度與[!DNL Analytics for Target]有關：

* **目標活動**： A/B測試的名稱

* **目標體驗**：活動中使用的登陸頁面體驗名稱

* **Target活動** > **體驗**：活動名稱和體驗名稱在同一列

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
* [A/B測試概覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 說明A/B測試活動，您可以將其用於搜尋、社交和Commerce廣告。
* [總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) — 介紹[!DNL Analytics for Advertising]，它可讓您在Analytics執行個體中追蹤點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定Advertising DSP廣告的A/B測試](ab-tests-dsp.md)
