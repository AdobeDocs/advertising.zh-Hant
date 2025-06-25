---
title: 關於報表
description: 瞭解效能報表，包括可用的不同報表型別以及如何自動化報表。
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# 關於報表

績效報表可讓您在任意精細的層級追蹤和管理產品組合、廣告網路和廣告網路帳戶實體的績效。 大部分報表可完整顯示每個行銷管道中的廣告對整體轉換率的貢獻度。

每次執行報表時，報表的資料都會動態編譯。 您可以選擇從現有報表產生新報表。 可用的報告引數會因報告型別而異。 對於大多數報表，您可以選擇預覽前50行，而不是產生整個報表。 當您產生報告時，您可以在報告完成時傳送包含一或多個電子郵件地址下載連結的通知，收件者可以在[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md)中管理通知。

所有已完成的報告都可在[!UICONTROL Reports]檢視的[!UICONTROL Latest Reports]區段中取得，您可以在瀏覽器視窗中以表格格式檢視它們，或開啟或以檔案形式下載它們。

## 可用的報告類別

[!UICONTROL Reports]檢視中有以下報表類別。 您可能無法存取所有報表；可用的報表及其產生的資料取決於您的角色及客戶帳戶的設定方式。

| 報告類別 | 說明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [基本報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)適用於所有使用者，顯示產品組合、廣告網路帳戶、特定廣告網路帳戶、行銷活動、廣告群組、廣告、關鍵字、產品群組、標籤分類和標籤值、競標單位限制及網路限制的實際成本與點按資料。 它們是根據適用廣告網路計費的點按次數，並可選擇包含轉換資料或您建立的任何其他量度。 |
| [!UICONTROL Advanced Reports] | [進階報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)為您的廣告設定提供額外的insight，協助您識別將透過變更地理定位或網路設定而受益的位置。 它們也可協助您根據廣告商的內部轉換追蹤資料，驗證行銷活動和產品組合管理檢視和報告中的轉換資料。 |
| [!UICONTROL Assist Reports] | [協助報表](/help/search-social-commerce/reports/management/assist/assist-report-about.md)針對廣告商的所有關鍵字和廣告，提供轉換路徑的深入分析。 這些變數使用透過Adobe Advertising轉換追蹤服務擷取的資料，且只能為該服務的廣告商產生。 |
| [!UICONTROL Specialty Reports] | [專業報告](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md)是由廣告網路所收集的資料(而非Adobe Advertising追蹤)所組成。 |
| [!UICONTROL Model Accuracy Reports] | [模型正確性報表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)指出用於最佳化產品組合出價、行銷活動預算及出價策略目標的成本與收入模型正確性。 |

## 報告自動化

排程自訂報表以以下列其中一種或兩種方式自動產生：

* 使用[報告範本](/help/search-social-commerce/reports/automation/templates/template-about.md)每天或在一週或一個月中的特定日自動產生報告。

  您可以選擇設定使用範本之基本與進階報告的[FTP傳遞](/help/search-social-commerce/reports/automation/ftp-reports.md)。

* 使用[試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)，以每日績效資料重新整理自訂的試算表範本。

## 報告檢視

在[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]的[!UICONTROL Reports]檢視可讓您建立和管理報告、範本及試算表摘要。 檢視包含兩個標籤：

* **[!UICONTROL Latest Reports]**&#x200B;索引標籤會列出過去七天中要求的所有可用報表（手動刪除除外），並將最新報表預設顯示在頂端。 每個報表所顯示的資訊包括執行時程表（若適用）、產生或將產生資料的開始和結束日期以及報表狀態（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*&#x200B;或&#x200B;*[!UICONTROL Error]*）。

  每個報表旁的連結可讓您在網頁瀏覽器中檢視報表，或開啟報表或將其儲存為[!DNL Microsoft Excel]活頁簿(XLS)或定位點分隔值(TSV)檔案；某些報表型別也可以儲存為[!UICONTROL Excel]活頁簿，並針對每個適用行銷活動使用個別工作表。

  您還可以從此標籤建立新報告（可選擇用作範本）、根據現有報告的設定建立新報告、透過刪除報告來取消您可用的進行中報告，以及刪除您可用的任何已完成報告。 超過7天的報表會自動刪除。

* 「**[!UICONTROL Templates]**」索引標籤會列出所有可供您使用的已儲存基本和進階報表範本，包括與它們相關聯的任何排程的相關資訊。 根據預設，最新的範本位於頂端。

  您可以在此標籤中建立新範本、編輯任何您建立的範本（包括新增、變更或移除其排程）、從範本產生報表，以及刪除任何可供您使用的範本。

## 如何使用報表

| 用途 | 報告 |
| ---- | ---- |
| 效能監視 | <ul><li>[該[!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[該[!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[該[!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[該[!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[該[!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[該[!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| 效能疑難排解與趨勢分析 | <ul><li>[該[!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[該[!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[該[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[該[!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[該[!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md)和[該[!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>使用&quot;[!UICONTROL Compare with]&quot;功能比較兩個時間範圍的任何基本報表</li></ul> |
| 識別業務成長機會 | <ul><li>(僅具有Adobe Advertising轉換追蹤的廣告商) [ [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(僅具有Adobe Advertising轉換追蹤的廣告商) [ [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的廣告商) Adobe Analytics Analysis Workspace中的自訂報告</li></ul> |
| Analytics | <ul><li>(僅具有Adobe Advertising轉換追蹤的廣告商) [ [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的廣告商) Adobe Analytics Analysis Workspace中的自訂報告</li></ul> |

>[!MORELIKETHIS]
>
>* [用於報告的資料](data-used-for-reports.md)
>* [報告的初始設定工作](initial-setup.md)
>* [產生基本或進階報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [產生模型正確性報告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [產生專業報告](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [產生協助報告](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
