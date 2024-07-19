---
title: 產生 [!DNL Advertising Insight]
description: 瞭解如何建立 [!DNL Advertising Insight]。
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 產生[!DNL Advertising Insight]

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**。

2. 按一下您要產生的分析。

3. 指定分析設定：

   1. （部分報表；選用）指定深入分析的日期範圍。

   2. （最深入分析）選取要分析的投資組合。

      一般而言，包含有效行銷活動的所有最佳化和有效產品組合皆可使用。 如需深入分析，您可以篩選投資組合清單以包含&#x200B;**[!UICONTROL Only Optimized Portfolios]**。

      針對[!UICONTROL Day of Week]深入分析，只能使用具有足夠支出且過去兩天也支出到目標的產品組合。

   3. （僅限[!UICONTROL Event Path Beta]分析）執行下列動作：

      1. 選取&#x200B;**[!UICONTROL Operation]**： *[!UICONTROL Extract events]* （上傳[!UICONTROL Channel Assist Report]或[!UICONTROL Campaign Assist Report]，並將使用者事件分類為不同的群組以供分析）或&#x200B;*[!UICONTROL Analyze classified events]* （上傳事件群組並使用它們產生見解）。

      1. 按一下&#x200B;**[!UICONTROL Select]**&#x200B;以找到XLSX和ZIP （壓縮的XLSX）格式的檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

   4. （僅限[!UICONTROL Google Account Audit]分析）執行下列動作：

      1. 輸入&#x200B;**[!UICONTROL Advertiser Name]**&#x200B;和&#x200B;**[!UICONTROL Account Name]**。

      1. 選取&#x200B;**[!UICONTROL Account Currency]**、**[!UICONTROL File Format Region]** （*[!UICONTROL United States]*&#x200B;或&#x200B;*[!UICONTROL United Kingdom]*）以及&#x200B;**[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*、*[!UICONTROL French]*&#x200B;或&#x200B;*[!UICONTROL German]*）。

      1. 按一下&#x200B;**[!UICONTROL Select]**&#x200B;以尋找從[!DNL Google Ads]網頁使用者介面為帳戶下載的行銷活動、關鍵字和變更歷程記錄報告，以及從[!DNL Google Ads Editor]應用程式為帳戶下載的Bulksheet檔案。 然後按一下&#x200B;**[!UICONTROL Upload]**。

         所有檔案都必須是CSV、TSV、TXT或ZIP （壓縮的CSV、TSV或TXT）格式。

   5. （僅限[!UICONTROL Location Target Performance]分析；選擇性）若要每日彙總資料而非彙總資料，請選取&#x200B;*[!UICONTROL Daily]*&#x200B;的&#x200B;**[!UICONTROL Time Aggregation]**。

   6. （僅限[!UICONTROL Normalized Sim (Combined)]分析）執行下列動作：

      1. 在&#x200B;**[!UICONTROL Step]**&#x200B;欄位中，指定要包含在深入分析中的目標支出層級或步驟數。 此值可介於三(3)到100之間。

      1. 在&#x200B;**[!UICONTROL Type]**&#x200B;欄位中，選取模擬型別：

         * *[!UICONTROL Optimized Multi-portfolio]*：針對具有相同目標與貨幣的多個產品組合產生單一模擬。

         * *[!UICONTROL Individual Normalized]*：為每個選取的投資組合產生個別模擬。 產品組合可能有不同的目標和貨幣。

   7. （[!UICONTROL Portfolio Launch]僅限分析；選擇性）若要指定未來的啟動日期，請在&#x200B;**[!UICONTROL Optional Date]**&#x200B;欄位中指定日期。

   8. （僅限[!UICONTROL Quality Score]分析）選取適用的廣告網路。

   9. （僅限[!UICONTROL Query Cross Matching]分析）在&#x200B;**[!UICONTROL Google Accounts]**&#x200B;功能表中，選取帳戶。

4. 按一下&#x200B;**[!UICONTROL Generate Insight]**。

   當工作完成或失敗時，您會根據[為[!UICONTROL Advertising Insights]設定的通知設定](/help/search-social-commerce/notifications/notification-edit.md)接收通知。

>[!MORELIKETHIS]
>
>* [關於[!UICONTROL Advertising Insights]](insight-about.md)
>* [檢視或儲存 [!DNL Advertising Insight]](insight-view-save.md)
>* [刪除 [!DNL Advertising Insight]](insight-delete.md)
