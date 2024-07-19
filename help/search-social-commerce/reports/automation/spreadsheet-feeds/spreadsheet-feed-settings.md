---
title: 試算表報表摘要設定
description: 了解試算表摘要的設定。
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# 試算表報表摘要設定

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Feed Name] | 試算表摘要的名稱。 |
| [!UICONTROL Report Template] | 指定所需報表資料的報表範本；選取用來建立[!DNL Excel]範本的報表範本。 列出所有基本報表範本。<br><br><b>注意：</b>如果您變更用於報表的報表範本，或更新範本中的欄，則必須建立並上傳新的[!DNL Excel]範本。 |
| [!UICONTROL Excel Template] | 您以.XLSX格式建立的特殊格式化[!DNL Excel]範本，套用至報表範本中指定的資料。 輸入完整路徑和檔案名稱，或按一下<b>[!UICONTROL Browse]</b>在您的裝置或網路上尋找檔案，以指定要上傳的檔案。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW]標籤上現有資料重新整理的開始日期，以過去的天數表示。 請輸入最多90天的值；預設值為七(7)天。<br><br>例如，如果值為7，而今天是3月7日，則會重新整理[!UICONTROL RAW]標籤上從3月1日開始的現有資料（直到[!UICONTROL Back Fill Until]引數指定的結束日期）。 3月1日之前日期的現有資料列不會刪除，但不會重新整理。 |
| [!UICONTROL Back Fill Until] | 重新整理[!UICONTROL RAW]標籤上現有資料的結束日期，以過去的天數表示。 預設值為一(1)天。<br><br>例如，如果此值為1，而今天是3月7日，則[!UICONTROL RAW]標籤上的現有資料會重新整理到3月6日（並且從[!UICONTROL Back Fill From]引數指定的開始日期開始）。 如果此值為1，[!UICONTROL Back Fill Until]引數為7，而今天是3月7日，則[!UICONTROL RAW]標籤上的現有資料會從3月1日重新整理到3月6日。 在這兩個範例中，不會刪除3月6日之後的現有資料列，但不會重新整理。 |
| [!UICONTROL Email Recipients] | 在每次重新整理報表或每次執行報表（當範本包含排程）時傳送通知的電子郵件地址。 依預設，會輸入您使用者帳戶的地址。 若要指定多個地址，請用逗號、空格或新行加以區隔。 |
| [!UICONTROL Schedule Time] | 試算表摘要的重新整理時間：上午8:00或廣告商時區的10:00至23:00之間的任何時間。 新試算表摘要的預設值為10:00。<br><br><b>注意：</b>基於效能考量，您無法在產生其他報表時於09:00重新整理試算表摘要。 |
| [!UICONTROL Email Notification] | （指定電子郵件收件者時）要包含在任何指定地址的電子郵件通知中的內容：<ul><li><i>附加摘要</i>  — 以XLSX格式傳送已完成報表的復本。 如果檔案大於10 MB，則通知不包含附件。</li><li><i>僅通知</i> （預設值） — 僅傳送報告完成或失敗的通知，並附報告連結。</li></ul> |

>[!MORELIKETHIS]
>
>* [關於試算表報表摘要](spreadsheet-feed-about.md)
>* [建立試算表報表摘要](spreadsheet-feed-create.md)
>* [建立試算表報表摘要的 [!DNL Excel] 範本](spreadsheet-feed-create-excel-template.md)
>* [編輯試算表報表摘要設定](spreadsheet-feed-edit.md)
>* [檢視或儲存試算表報表摘要檔案](spreadsheet-feed-view-or-save.md)
>* [手動重新整理試算表報表摘要](spreadsheet-feed-refresh.md)
>* [刪除試算表報表摘要](spreadsheet-feed-delete.md)
