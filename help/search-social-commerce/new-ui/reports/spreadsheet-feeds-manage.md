---
title: （新UI）管理試算表報表摘要
description: 瞭解如何建立、設定、重新整理、檢視和刪除以自訂格式試算表提供每日效能資料的試算表報表摘要。
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# （新UI）管理試算表報表摘要

*僅適用基本報告和模型準確度報告*

<!-- Update link to notifications once available -->

試算表摘要以[!DNL Microsoft Excel] XLSX的自訂試算表格式提供所有基本報表和模型正確性報表的每日效能資料。 您可以使用從一般報表範本建立的特殊格式化[!DNL Excel]試算表範本，來設定試算表摘要。 每天，試算表都會在指定的時間自動以每天彙總的新原始資料重新整理。 原始資料會填入您已包含在試算表範本中的任何欄和圖表。 試算表摘要檔案可用後，或檔案產生失敗時，報表範本中的每個電子郵件收件者會根據使用者為報表[&#128279;](/help/search-social-commerce/notifications/notification-about.md)設定的通知設定來接收通知。

您可以將摘要設定為最多重新整理過去90天的資料，而所有先前的現有資料都會保留，繼續累積。

[!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds]檢視會列出您已建立的所有試算表摘要。 您可以從此檢視建立試算表摘要、手動重新整理摘要或刪除摘要。

## 可用動作

* [建立試算表報表摘要的 [!DNL Excel] 範本](#spreadsheet-feed-create-excel-template)

* [建立試算表報表摘要](#spreadsheet-feed-create)

* [編輯試算表報表摘要設定](#spreadsheet-feed-edit)

* [檢視或儲存試算表報表摘要檔案](#spreadsheet-feed-view-or-save)

* [手動重新整理試算表報表摘要](#spreadsheet-feed-refresh)

* [刪除試算表報表摘要](#spreadsheet-feed-delete)

## 為試算表報表摘要建立[!DNL Excel]範本 {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

若要建立試算表摘要，您必須先使用一般報表範本建立特別格式化的[!DNL Microsoft Excel]試算表範本。 您可以選擇自訂[!DNL Excel]試算表以包含其他欄和圖表。

1. 在&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;中，使用「[!UICONTROL Daily]」的[!UICONTROL Date Aggregation]單位以及您想要的所有其他資料引數產生所需的報表型別，並將報表儲存為範本。

   >[!NOTE]
   >
   > * 您可以建立[!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]和[!UICONTROL Forecast Accuracy]報表的試算表摘要。 如果您使用[!UICONTROL Ad Group Report]，請限制包含的廣告群組數目，以更快獲得結果。
   > * 未使用範本中定義的[!UICONTROL Date Range]單位。 您稍後設定試算表摘要時，會定義重新整理資料的日期。

1. 產生報表之後，請移至&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，並將報表輸出的TSV或XLS版本匯出至檔案。

1. 在[!DNL Excel]中，建立報告的自訂範本：

   1. 在[!DNL Excel]中開啟報告檔案。

   1. 準備活頁簿：

      1. 刪除顯示報表引數的前幾列。 若為XLS檔案，請一併刪除&quot;[!UICONTROL Total]&quot;列。 您可以選擇刪除某些資料列，但保留a)具有原始順序中所有欄的資料標題列，以及b)至少一個資料列。 請勿手動新增任何資料。

         >[!NOTE]
         >
         > 最後一欄必須包含非零的值。

      1. 依開始日期遞增順序排序資料（從最舊到最近）。

      1. 將工作表標簽名稱從&quot;[!UICONTROL Sheet1]&quot;變更為&quot;[!UICONTROL RAW]&quot;。

         此特定索引標簽名稱可讓資料重新整理。

      1. （選用）視需要在報表範本的欄右側新增自訂欄。

   1. （選擇性）在個別的工作表上建立樞紐分析表。 完成後，在樞紐分析表的任何儲存格中按一下滑鼠右鍵，然後選取&#x200B;**[!UICONTROL Pivot Table Options]**，按一下&#x200B;**[!UICONTROL Data]**&#x200B;索引標籤，然後選取&#x200B;**[!UICONTROL Refresh data when opening the file]**。

   1. 將檔案儲存為.XLSX格式的[!DNL Excel]試算表。

## 建立試算表報表摘要 {#spreadsheet-feed-create}

1. [建立 [!DNL Excel] 範本以填入報表資料](#spreadsheet-feed-create-excel-template)。

1. 建立試算表摘要：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

   1. 按一下右上角的&#x200B;**[!UICONTROL Create Spreadsheet]**。

   1. 在&#x200B;**[!UICONTROL Create Spreadsheet Feed]**&#x200B;對話方塊中，指定[試算表摘要設定](#spreadsheet-feed-settings)。

   1. 按一下&#x200B;**[!UICONTROL Submit]**。

   1. （選擇性）一旦摘要的[!UICONTROL Update Status]為&#x200B;*[!UICONTROL Finished]*，請按一下摘要旁的&#x200B;**[!UICONTROL XLSX]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

      >[!NOTE]
      >
      >如果之後刪除與摘要相關聯的報告範本，則也會刪除摘要。

      試算表摘要每天會在設定的[!UICONTROL Schedule Time]自動重新整理。 如果報表範本包含任何電子郵件收件者的地址，則這些地址會在重新整理試算表時收到通知。

## 編輯試算表報表摘要設定 {#spreadsheet-feed-edit}

>[!NOTE]
>
> 如果您編輯報表範本中的欄，或使用新的或更新後的報表範本，則必須相應地更新[!DNL Excel]範本並再次上傳。

1. （選用）若要更新用於試算表摘要的報表範本或[!DNL Excel]範本：

   * （選擇性）若要針對摘要使用不同或更新後的報表範本，請[為報表範本](#spreadsheet-feed-create-excel-template)建立新的 [!DNL Excel] 範本。

     您將在後續步驟中上傳報告範本和新的[!DNL Excel]檔案。

   * （選擇性）若要僅新增自訂欄至[!DNL Excel]範本，請在報表範本的欄右側插入欄，然後將檔案儲存為.XLSX格式的[!DNL Excel]試算表。 您需要在下一個步驟中上傳新的[!DNL Excel]檔案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 變更試算表摘要設定：

   1. 選取試算表摘要名稱旁的核取方塊。

   1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

   1. 在[!UICONTROL Create Spreadsheet Feed]<!-- sic -->對話方塊中，變更[試算表摘要設定](#spreadsheet-feed-settings)。

   1. 按一下&#x200B;**[!UICONTROL Submit]**。

   1. （選擇性）一旦摘要的[!UICONTROL Update Status]為&#x200B;*[!UICONTROL Finished]*，請按一下摘要旁的&#x200B;**[!UICONTROL XLSX]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

   >[!NOTE]
   >
   > 如果之後刪除與摘要相關聯的報告範本，則也會刪除摘要。

   在廣告商的時區，試算表摘要會在每天的08:00自動重新整理。 如果報表範本包含任何電子郵件收件者的地址，則這些地址會在重新整理試算表時收到通知。

## 試算表報表摘要設定 {#spreadsheet-feed-settings}

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Feed Name] | 試算表摘要的名稱。 |
| [!UICONTROL Report Template] | 指定所需報表資料的報表範本；選取用來建立[!DNL Excel]範本的報表範本。 所有基本報告範本都會列出。<br><br><b>注意：</b>如果您變更報告使用的報告範本，或更新範本中的欄，則必須建立並上傳新的[!DNL Excel]範本。 |
| [!UICONTROL Excel Template] | 您以.XLSX格式建立的特殊格式化[!DNL Excel]範本，套用至報表範本中指定的資料。 輸入完整路徑和檔案名稱，或按一下<b>[!UICONTROL Browse]</b>在您的裝置或網路上尋找檔案，以指定要上傳的檔案。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW]標籤上現有資料重新整理的開始日期，以過去的天數表示。 請輸入最多90天的值；預設值為七(7)天。<br><br>例如，如果值為7，而今天是3月7日，則會重新整理[!UICONTROL RAW]標籤上從3月1日開始的現有資料（直到[!UICONTROL Back Fill Until]引數指定的結束日期）。 3月1日之前日期的現有資料列不會刪除，但不會重新整理。 |
| [!UICONTROL Back Fill Until] | 重新整理[!UICONTROL RAW]標籤上現有資料的結束日期，以過去的天數表示。 預設值為一(1)天。<br><br>例如，如果此值為1，而今天是3月7日，則[!UICONTROL RAW]標籤上的現有資料會重新整理到3月6日（並且從[!UICONTROL Back Fill From]引數指定的開始日期開始）。 如果此值為1，[!UICONTROL Back Fill Until]引數為7，而今天是3月7日，則[!UICONTROL RAW]標籤上的現有資料會從3月1日重新整理到3月6日。 在這兩個範例中，不會刪除3月6日之後的現有資料列，但不會重新整理。 |
| [!UICONTROL Email Recipients] | 在每次重新整理報表或每次執行報表（當範本包含排程）時傳送通知的電子郵件地址。 依預設，會輸入您使用者帳戶的地址。 若要指定多個地址，請用逗號、空格或新行加以區隔。 |
| [!UICONTROL Schedule Time] | 重新整理試算表摘要的時間：在廣告商時區的08:00或介於10:00到23:00之間的任何時間。 新試算表摘要的預設值為10:00。<br><br><b>注意：</b>基於效能考量，您無法在產生其他報表時於09:00重新整理試算表摘要。 |
| [!UICONTROL Email Notification] | （指定電子郵件收件者時）要包含在任何指定地址的電子郵件通知中的內容：<ul><li><i>[!UICONTROL Attach feed]</i>  — 以XLSX格式傳送已完成報表的復本。 如果檔案大於10 MB，則通知不包含附件。</li><li><i>[!UICONTROL Notification Only]</i> （預設值） — 只傳送報告完成或失敗的通知，並附報告連結。</li></ul> |

## 檢視或儲存試算表報表摘要檔案 {#spreadsheet-feed-view-or-save}

您可以檢視任何產生的試算表摘要，或將其儲存至檔案。 試算表摘要檔案為[!DNL Microsoft Excel] XLSX格式。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 按一下摘要旁的&#x200B;**[!UICONTROL XLSX]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

## 手動重新整理試算表報表摘要 {#spreadsheet-feed-refresh}

>[!NOTE]
>
>試算表摘要會在當地時區的每天08:00自動重新整理。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 選取您要重新整理的每個摘要旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Run Spreadsheet]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

1. （選擇性）一旦摘要的[!UICONTROL Update Status]為&#x200B;*[!UICONTROL Finished]*，請按一下摘要旁的&#x200B;**[!UICONTROL XLSX]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

## 刪除試算表報表摘要 {#spreadsheet-feed-delete}

>[!NOTE]
>
>如果刪除與摘要相關的報表範本，則會自動刪除摘要。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 選取要刪除的每個摘要旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。
