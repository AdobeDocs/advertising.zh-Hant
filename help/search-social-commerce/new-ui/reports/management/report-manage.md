---
title: 管理排程報告
description: 瞭解如何管理排程報告。
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# 管理排程報告

績效報表可讓您在任意精細的層級追蹤和管理產品組合、廣告網路和廣告網路帳戶實體的績效。 大部分報表可完整顯示每個行銷管道中的廣告對整體轉換率的貢獻度。

每次執行報表時，報表的資料都會動態編譯。 您可以選擇從現有報表產生新報表。 可用的報告引數會因報告型別而異。 對於大多數報表，您可以選擇預覽前50行，而不是產生整個報表。 當您產生報告時，您可以在報告完成時傳送包含一或多個電子郵件地址下載連結的通知，收件者可以在[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)中[管理通知。

所有已完成的報告都可在[!UICONTROL Reports]檢視的[!UICONTROL Latest Reports]區段中取得，您可以在瀏覽器視窗中以表格格式檢視它們，或開啟或以檔案形式下載它們。

## 可用的報告類別

[!UICONTROL Reports]檢視中有以下報表類別。 您可能無法存取所有報表；可用的報表及其產生的資料取決於您的角色及客戶帳戶的設定方式。

| 報告類別 | 說明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [基本報告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)適用於所有使用者，顯示產品組合、廣告網路帳戶、特定廣告網路帳戶、行銷活動、廣告群組、廣告、關鍵字、產品群組、標籤分類和標籤值、競標單位限制及網路限制的實際成本與點按資料。 它們是根據適用廣告網路計費的點按次數，並可選擇包含轉換資料或您建立的任何其他量度。 |
| [!UICONTROL Advanced Reports] | [進階報告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)為您的廣告設定提供額外的insight，協助您識別將透過變更地理定位或網路設定而受益的位置。 它們也可協助您根據廣告商的內部轉換追蹤資料，驗證行銷活動和產品組合管理檢視和報告中的轉換資料。 |
| [!UICONTROL Assist Reports] | [協助報表](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md)針對廣告商的所有關鍵字和廣告，提供轉換路徑的深入分析。 這些變數使用透過Adobe Advertising轉換追蹤服務擷取的資料，且只能為該服務的廣告商產生。 |
| [!UICONTROL Specialty Reports] | [專業報告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md)是由廣告網路所收集的資料（而非Adobe Advertising追蹤）所組成。 |
| [!UICONTROL Model Accuracy Reports] | [模型正確性報表](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md)指出用於最佳化產品組合出價、行銷活動預算及出價策略目標的成本與收入模型正確性。 |

## 報告自動化

排程自訂報表以以下列其中一種或兩種方式自動產生：

* 使用[報告範本](/help/search-social-commerce/reports/automation/templates/template-about.md)每天或在一週或一個月中的特定日自動產生報告。

  您可以選擇設定使用範本之基本與進階報告的[FTP傳遞](/help/search-social-commerce/new-ui/reports/ftp-reports.md)。

* 使用[試算表摘要](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)，以每日績效資料重新整理自訂的試算表範本。

## [!UICONTROL Scheduled Reports]檢視

[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]檢視可讓您建立和管理報告和報告範本：

* **[!UICONTROL Latest Reports]**&#x200B;索引標籤會列出所有可供您<!-- Doesn't seem to be true: that were requested in the last seven days -->使用的報告，手動刪除的報告除外，最新的報告預設會顯示在頂端。 每個報表所顯示的資訊包括執行時程表（若適用）、產生或將產生資料的開始和結束日期、建立報表的人員，以及報表狀態（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*&#x200B;或&#x200B;*[!UICONTROL Error]*）。

  每個報表旁的連結可讓您開啟報表，或將報表儲存為[!DNL Microsoft Excel]活頁簿(XLS)、定位點分隔值(TSV)檔案或逗號分隔值(CSV)檔案。 某些報表型別也可以儲存為[!UICONTROL Excel]活頁簿，每個適用行銷活動各有個別的工作表。

  您還可以從此標籤建立新報告（可選擇用作範本）、根據現有報告的設定或使用報告範本建立新報告、透過刪除報告來取消您可用的進行中報告，以及刪除您可用的任何已完成報告。

* 「**[!UICONTROL Templates]**」索引標籤會列出所有可供您使用的已儲存基本和進階報表範本，包括與它們相關聯的任何排程的相關資訊。 根據預設，最新的範本位於頂端。

  您可以在此標籤中建立新範本、編輯任何您建立的範本（包括新增、變更或移除其排程）、從範本產生報表，以及刪除任何可供您使用的範本。

## 如何使用報表

| 用途 | 報告 |
| ---- | ---- |
| 效能監視 | <ul><li>[該[!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[該[!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[該[!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[該[!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[該[!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[該[!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| 效能疑難排解與趨勢分析 | <ul><li>[該[!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[該[!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[該[!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[該[!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[該[!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md)和[該[!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>使用&quot;[!UICONTROL Compare with]&quot;功能比較兩個時間範圍的任何基本報表</li></ul> |
| 識別業務成長機會 | <ul><li>（僅具有Adobe Advertising轉換追蹤的廣告商） [ [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>（僅具有Adobe Advertising轉換追蹤的廣告商） [ [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>（具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的廣告商） Adobe Analytics Analysis Workspace中的自訂報告</li></ul> |
| Analytics | <ul><li>（僅具有Adobe Advertising轉換追蹤的廣告商） [ [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>（具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的廣告商） Adobe Analytics Analysis Workspace中的自訂報告</li></ul> |

## 產生報表

### 產生新報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**。

1. 按一下&#x200B;**[!UICONTROL Create Report]**，按一下左側面板中的報表類別，然後選取報表型別。<!-- Add link to list of report categories and report types --> 按一下&#x200B;**[!UICONTROL Proceed]**。

1. （選擇性）在[!UICONTROL Create Report]視窗中，變更[基本與進階報告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[協助報告](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[模型正確性報告](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)與[專業報告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)的預設報告設定：

   1. （選擇性）輸入報表和範本的自訂名稱（若您將報表另存為範本）。

   1. （選擇性）若要將報表設定儲存為範本，請啟用&#x200B;**[!UICONTROL Save as template]**&#x200B;設定。

   1. （選擇性）選取相同報表類別中的不同報表&#x200B;**[!UICONTROL Type]**。

   1. （選擇性）在「**[!UICONTROL Basic Settings]**」標籤上，選取要使用的現有報表範本，或變更報表的預設基本設定。

   1. （選用）按一下&#x200B;**[!UICONTROL Columns]**&#x200B;標籤，然後變更報表中的預設欄，包括欄順序。

      依預設，報表中的所有貨幣資料都會以美元格式顯示（例如1,000.00）。 若要以正確的貨幣格式顯示值（但不含CSV和TSV格式的任何貨幣符號），請新增&quot;[!UICONTROL Currency]&quot;欄至報表。 如果報表包含不同貨幣的帳戶資料，則任何&quot;[!UICONTROL Total]&quot;貨幣值為欄中所有數字的總和，無論貨幣為何。

   1. （部分報表型別，選用）按一下「**[!UICONTROL Filters & Attribution]**」或「**[!UICONTROL Filters]**」標籤，然後新增資料篩選、（部分報表型別）將報表結果限製為僅包含特定標籤分類，並變更預設歸因規則和轉換歸因設定。

   1. （選用）按一下&#x200B;**[!UICONTROL Scheduling]**&#x200B;標籤，然後變更預設排程與傳送選項。

1. 按一下&#x200B;**[!UICONTROL Create]**。

如果您未指定報表排程，則會立即執行報表；否則，會根據指定的排程執行。 報告名稱已新增至[[!UICONTROL Latest Reports]檢視](/help/search-social-commerce/reports/report-about.md)。 如果您將報表儲存為範本，則也會將其新增至[[!UICONTROL Templates]檢視](/help/search-social-commerce/reports/report-about.md)。 報告完成後，檔案即可開啟或儲存；範本可立即使用。

如果您輸入任何電子郵件地址來通知，每個收件者都會在報告工作完成或失敗時收到通知，此通知是根據使用者針對報告所設定的[通知設定](/help/search-social-commerce/notifications/notification-edit.md)而定。

### 從現有報表產生報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，這會開啟至&#x200B;**[!UICONTROL Latest Reports]**&#x200B;索引標籤。

1. 執行下列任一項作業：

   * 將游標停留在報表列上，然後按一下&#x200B;**...** > **[!UICONTROL Duplicate]**。

   * 選取報告旁的核取方塊。 在大量動作工具列中按一下[複製](/help/search-social-commerce/assets/duplicate.png "複製")。

1. 編輯報告設定（如有必要）。

1. 按一下&#x200B;**[!UICONTROL Create]**。

### 從現有範本產生報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 執行下列任一項作業：

   * 將游標停留在範本列上，然後按一下&#x200B;**...** > **[!UICONTROL Duplicate]**。

   * 選取現有範本旁的核取方塊。 在大量動作工具列中按一下[複製](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**。

1. （可選）重新命名範本，並視需要編輯報表設定。

   按一下&#x200B;**[!UICONTROL Next]**&#x200B;在設定區段之間移動。

1. 啟用&#x200B;**[!UICONTROL Save as Template]**&#x200B;設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 預覽或儲存報告

您可以在網頁瀏覽器中預覽報表，或開啟報表資料或將報表資料儲存為[!DNL Microsoft Excel]活頁簿、定位字元分隔值(TSV)檔案、逗號分隔值(CSV)檔案或（某些報表型別）[!DNL Microsoft Excel]索引標籤式活頁簿。

>[!NOTE]
>
>Adobe帳戶團隊成員和某些管理員使用者可以檢視廣告商和機構使用者建立的報告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，這會開啟至&#x200B;**[!UICONTROL Latest Reports]**&#x200B;索引標籤。

1. 執行下列任一項作業：

   * （若要在網頁瀏覽器中檢視報表），請執行下列其中一項作業：

      * 將游標停留在範本列上，然後按一下&#x200B;**...** > **[!UICONTROL Preview]**。

      * 選取現有範本旁的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Preview]**。

   * （若要開啟或儲存檔案中的報表資料）在報表名稱旁的[!UICONTROL Export]欄中，按一下格式的名稱，然後依照瀏覽器的正常程式開啟或儲存檔案：

      * **[!UICONTROL XLS]：**&#x200B;針對單一工作表（XLSX格式）的[!DNL Excel]活頁簿。 此報表包括一個位於頂端且以引數標示的工作表，每個元件會有一列在元件資料可用時報告。 沒有資料的列會省略。

        基本報表包含每個數值欄的總數。

      * TSV檔案的&#x200B;**[!UICONTROL TSV]：**。 報表包括引數，以及報表中每個元件的資料列。

      * **[!UICONTROL CSV]：**&#x200B;用於CSV檔案。 報表包括引數，以及報表中每個元件的資料列。

## 刪除報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，這會開啟至&#x200B;**[!UICONTROL Latest Reports]**&#x200B;索引標籤。

1. 執行下列任一項作業：

   * （若要刪除單一報表）：

      1. 將游標停留在報表列上，然後按一下&#x200B;**...** > **[!UICONTROL Run]**。

      1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

   * （若要刪除一或多個報表）：

      1. 選取要刪除的每個報告旁的核取方塊。

      1. 在大量動作工具列中按一下[刪除](/help/search-social-commerce/assets/delete-new.png "刪除") **[!UICONTROL Delete]**。

      1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
