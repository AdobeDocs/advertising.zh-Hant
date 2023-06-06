---
title: 試算表報表摘要設定
description: 了解試算表摘要的設定。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 試算表報表摘要設定

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Feed Name] | 試算表摘要的名稱。 |
| [!UICONTROL Report Template] | 指定所需報表資料的報表範本；選取您用來建立 [!DNL Excel] 範本。 所有基本報表範本都會列出。<br><br><b>注意：</b> 如果您變更用於報表的報表範本，或更新範本中的欄，則必須建立並上傳新的 [!DNL Excel] 範本。 |
| [!UICONTROL Excel Template] | 特別格式化的 [!DNL Excel] 您以.XLSX格式建立的範本，套用至報表範本中指定的資料。 輸入完整路徑和檔案名稱，或按一下「 」，指定要上傳的檔案 <b>[!UICONTROL Browse]</b> 以找出裝置或網路上的檔案。 |
| [!UICONTROL Back Fill From] | 上現有資料的開始日期 [!UICONTROL RAW] 索引標籤會重新整理，以過去的天數表示。 輸入最多90天的值；預設值為七(7)天。<br><br>例如，如果值為7，而今天是3月7日，則上的現有資料 [!UICONTROL RAW] 從3月1日開始的標籤會重新整理(直到指定的結束日期 [!UICONTROL Back Fill Until] 引數)。 不會刪除3月1日之前日期的現有資料列，但不會重新整理。 |
| [!UICONTROL Back Fill Until] | 上現有資料的結束日期 [!UICONTROL RAW] 索引標籤會重新整理，以過去的天數表示。 預設值為一(1)天。<br><br>例如，如果此值為1，而今天是3月7日，則上的現有資料 [!UICONTROL RAW] 索引標籤會重新整理到3月6日(並且從 [!UICONTROL Back Fill From] 引數)。 如果此值為1，則 [!UICONTROL Back Fill Until] 引數為7，而今天是3月7日，則現有資料位於 [!UICONTROL RAW] 索引標籤會從3月1日重新整理至3月6日。 在這兩個範例中，不會刪除3月6日之後日期的現有資料列，但不會重新整理。 |
| [!UICONTROL Email Recipients] | 在每次重新整理報告時或在每次執行報告時範本包含排程時，傳送通知的電子郵件地址。 依預設，會輸入您使用者帳戶的地址。 若要指定多個地址，請以逗號、空格或新行來區隔。 |
| [!UICONTROL Schedule Time] | 重新整理試算表摘要的時間：08:00或在廣告商時區的10:00到23:00之間的任何小時。 新試算表摘要的預設值為10:00。<br><br><b>注意：</b> 基於效能考量，您無法在產生其他報表的09:00重新整理試算表摘要。 |
| [!UICONTROL Email Notification] | （指定電子郵件收件者時）傳送至任何指定地址的電子郵件通知中要包含的內容：<ul><li><i>附加摘要</i>  — 以XLSX格式傳送已完成報表的復本。 如果檔案大於10 MB，則通知不包含附件。</li><li><i>僅通知</i> （預設） — 僅傳送報告完成或失敗的通知，並附有指向報告的連結。</li></ul> |

>[!MORELIKETHIS]
>
>* [關於試算表報表摘要](spreadsheet-feed-about.md)
>* [建立試算表報表摘要](spreadsheet-feed-create.md)
>* [建立 [!DNL Excel] 試算表報表摘要的範本](spreadsheet-feed-create-excel-template.md)
>* [編輯試算表報表摘要設定](spreadsheet-feed-edit.md)
>* [檢視或儲存試算表報表摘要檔案](spreadsheet-feed-view-or-save.md)
>* [手動重新整理試算表報表摘要](spreadsheet-feed-refresh.md)
>* [刪除試算表報表摘要](spreadsheet-feed-delete.md)

