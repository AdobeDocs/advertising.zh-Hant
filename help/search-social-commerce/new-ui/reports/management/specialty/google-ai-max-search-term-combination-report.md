---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: 瞭解[!UICONTROL Google AI Max Search Term Combination Report]。
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*僅適用於[!DNL Google Ads]個已啟用AI最大行銷活動的帳戶*

[!UICONTROL Google AI Max Search Term Combination Report]顯示特定搜尋查詢如何對應至AI產生的標題和動態登陸頁面，以及如何對應至指定帳戶內啟用[!DNL Google Ads AI Max]的行銷活動中廣告的轉換動作。 報表包含兩張工作表：

* [!UICONTROL AI Max Search Term]工作表：根據搜尋網路內的搜尋，特定廣告組合和登入頁面的效能。 此工作表包含曝光數、點按數和成本資料，以及在報告設定中指定的任何選用[!DNL Google Ads]追蹤的轉換量度。 依預設，每個在指定資料範圍內至少獲得一次印象的搜尋辭彙、標題和登陸頁面組合，資料都包含一列。 依預設，這些列會依促銷活動以遞增順序排列，然後依您選取的另一個欄排列。

  使用此工作表來分析每個查詢產生的廣告元素的意圖和效能，以便您可以建立健全的負面關鍵字清單。

* &#x200B;<!-- [!UICONTROL Search Term x Conversion Action] sheet? -->[!UICONTROL AI Max Search Term #1]工作表：依每個搜尋字詞和相符型別的轉換動作，追蹤[!DNL Google Ads]轉換資料。 每一列包含轉換動作、轉換次數、轉換值，以及在報表設定中指定的任何其他選擇性[!DNL Google Ads]追蹤轉換量度。 依預設，資料會針對指定資料範圍內的每個搜尋字詞和轉換動作組合包含一列。 這些列的順序與第一頁上的列相同。

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  使用此工作表來瞭解每個搜尋字詞如何帶來轉換，依轉換動作細分。

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## 預設欄

如需所有預設和自訂欄的說明，請參閱[專業報告的報告欄](specialty-report-columns.md)。

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] （即使您未明確包含，也會自動包含在[!UICONTROL AI Max Search Term #1]工作表中）
* [!UICONTROL Conversions] （即使您未明確包含，也會自動包含在[!UICONTROL AI Max Search Term #1]工作表中）
* [!UICONTROL Conversions Value] （即使您未明確包含，也會自動包含在[!UICONTROL AI Max Search Term #1]工作表中）

>[!MORELIKETHIS]
>
>* [關於專業報告](specialty-report-about.md)
>* [管理排程報告](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [專業報告設定](specialty-report-settings.md)
>* [專業報告的報告欄](specialty-report-columns.md)
