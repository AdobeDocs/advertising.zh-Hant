---
title: 產生 [!DNL Advertising Insight]
description: 瞭解如何建立 [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 產生 [!DNL Advertising Insight]

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. 按一下您要產生的分析。

3. 指定分析設定：

   1. （部分報表；選用）指定深入分析的日期範圍。

   2. （最深入分析）選取要分析的投資組合。

      一般而言，包含有效行銷活動的所有最佳化和有效產品組合皆可使用。 如需深入分析，您可以篩選投資組合清單以包含 **[!UICONTROL Only Optimized Portfolios]**.

      的 [!UICONTROL Day of Week] 只有具備足夠支出以及在過去兩天也支出到目標的產品組合才有深入分析。

   3. ([!UICONTROL Event Path Beta] 僅限分析)執行下列動作：

      1. 選取 **[!UICONTROL Operation]**： *[!UICONTROL Extract events]* (上傳 [!UICONTROL Channel Assist Report] 或 [!UICONTROL Campaign Assist Report] 並將使用者事件分類為不同的群組，以供分析)或 *[!UICONTROL Analyze classified events]* （上傳事件群組並使用它們產生深入分析）。

      1. 按一下 **[!UICONTROL Select]** 若要找到XLSX和ZIP （壓縮XLSX）格式的檔案，然後按一下 **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] 僅限分析)執行下列動作：

      1. 輸入 **[!UICONTROL Advertiser Name]** 和 **[!UICONTROL Account Name]**.

      1. 選取 **[!UICONTROL Account Currency]**， **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* 或 *[!UICONTROL United Kingdom]*)，以及 **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*， *[!UICONTROL French]*，或 *[!UICONTROL German]*)。

      1. 按一下 **[!UICONTROL Select]** 若要尋找促銷活動、關鍵字，以及變更從下載的帳戶歷史記錄報告 [!DNL Google Ads] 網頁使用者介面和為帳戶下載的Bulksheet檔案 [!DNL Google Ads Editor] 應用程式。 然後按一下 **[!UICONTROL Upload]**.

         所有檔案都必須是CSV、TSV、TXT或ZIP （壓縮的CSV、TSV或TXT）格式。

   5. ([!UICONTROL Location Target Performance] 僅限分析；選用)若要每日彙總資料，而非作為摘要，請選取 **[!UICONTROL Time Aggregation]** 之 *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] 僅限分析)執行下列動作：

      1. 在 **[!UICONTROL Step]** 欄位中，指定要在分析中包含的目標支出層級或步驟數。 此值可介於三(3)到100之間。

      1. 在 **[!UICONTROL Type]** 欄位中，選取模擬型別：

         * *[!UICONTROL Optimized Multi-portfolio]*：針對具有相同目標和貨幣的多個產品組合產生單一模擬。

         * *[!UICONTROL Individual Normalized]*：為每個選取的投資組合產生個別模擬。 產品組合可能有不同的目標和貨幣。

   7. ([!UICONTROL Portfolio Launch] 僅限分析；選用)若要指定未來的啟動日期，請在 **[!UICONTROL Optional Date]** 欄位。

   8. ([!UICONTROL Quality Score] 僅限分析)選取適用的廣告網路。

   9. ([!UICONTROL Query Cross Matching] 僅限分析) **[!UICONTROL Google Accounts]** 功能表，選取帳戶。

4. 按一下 **[!UICONTROL Generate Insight]**.

   當工作完成或失敗時，您會根據您的 [已設定的通知設定](/help/search-social-commerce/notifications/notification-edit.md) 的 [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Advertising Insights]](insight-about.md)
>* [檢視或儲存 [!DNL Advertising Insight]](insight-view-save.md)
>* [刪除 [!DNL Advertising Insight]](insight-delete.md)
