---
title: 試算表報表摘要設定
description: 了解試算表摘要的設定。
exl-id: 9a7e0a21-5db4-4829-a191-cacaa51f6cb6
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 試算表報表摘要設定

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Feed Name] | 試算表摘要的名稱。 |
| [!UICONTROL Report Template] | 指定所需報表資料的報表範本；選取您用來建立 [!DNL Excel] 範本。 列出所有基本報表範本。<br><br><b>注意：</b> 如果您變更用於報表的報表範本，或更新範本中的欄，則必須建立並上傳新的 [!DNL Excel] 範本。 |
| [!UICONTROL Excel Template] | 特別格式化的 [!DNL Excel] 您以.XLSX格式建立的範本，套用至報表範本中指定的資料。 輸入完整路徑和檔案名稱，或按一下「 」，指定要上傳的檔案 <b>[!UICONTROL Browse]</b> 在您的裝置或網路上尋找檔案。 |
| [!UICONTROL Back Fill From] | 上現有資料的開始日期 [!UICONTROL RAW] 標籤會重新整理，以過去的天數表示。 請輸入最多90天的值；預設值為七(7)天。<br><br>例如，如果值為7，而今天為3月7日，則上的現有資料 [!UICONTROL RAW] 從3月1日開始的標籤會重新整理（直到指定的結束日期為止） [!UICONTROL Back Fill Until] 引數)。 3月1日之前日期的現有資料列不會刪除，但不會重新整理。 |
| [!UICONTROL Back Fill Until] | 上現有資料的結束日期 [!UICONTROL RAW] 標籤會重新整理，以過去的天數表示。 預設值為一(1)天。<br><br>例如，如果此值為1，而今天是3月7日，則上的現有資料 [!UICONTROL RAW] 索引標籤會重新整理到3月6日(並且從 [!UICONTROL Back Fill From] 引數)。 如果此值為1，則 [!UICONTROL Back Fill Until] 引數為7，而今天是3月7日，則現有資料位於 [!UICONTROL RAW] 索引標籤從3月1日到3月6日重新整理。 在這兩個範例中，不會刪除3月6日之後的現有資料列，但不會重新整理。 |
| [!UICONTROL Email Recipients] | 在每次重新整理報表或每次執行報表（當範本包含排程）時傳送通知的電子郵件地址。 依預設，會輸入您使用者帳戶的地址。 若要指定多個地址，請用逗號、空格或新行加以區隔。 |
| [!UICONTROL Schedule Time] | 試算表摘要的重新整理時間：上午8:00或廣告商時區的10:00至23:00之間的任何時間。 新試算表摘要的預設值為10:00。<br><br><b>注意：</b> 基於效能考量，您無法在產生其他報表的09:00重新整理試算表摘要。 |
| [!UICONTROL Email Notification] | （指定電子郵件收件者時）要包含在任何指定地址的電子郵件通知中的內容：<ul><li><i>附加摘要</i>  — 以XLSX格式傳送已完成報表的復本。 如果檔案大於10 MB，則通知不包含附件。</li><li><i>僅通知</i> （預設） — 僅傳送報告完成或失敗的通知，並附有報告連結。</li></ul> |

>[!MORELIKETHIS]
>
>* [關於試算表報表摘要](spreadsheet-feed-about.md)
>* [建立試算表報表摘要](spreadsheet-feed-create.md)
>* [建立 [!DNL Excel] 試算表報表摘要的範本](spreadsheet-feed-create-excel-template.md)
>* [編輯試算表報表摘要設定](spreadsheet-feed-edit.md)
>* [檢視或儲存試算表報表摘要檔案](spreadsheet-feed-view-or-save.md)
>* [手動重新整理試算表報表摘要](spreadsheet-feed-refresh.md)
>* [刪除試算表報表摘要](spreadsheet-feed-delete.md)
