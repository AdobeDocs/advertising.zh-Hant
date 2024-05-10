---
title: 建立 [!DNL Excel] 試算表報表摘要的範本
description: 瞭解如何建立特別格式化的試算表範本。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 建立 [!DNL Excel] 試算表報表摘要的範本

*僅用於基本報表和模型準確度報表*

若要建立試算表摘要，您必須先建立特別格式化的 [!DNL Microsoft Excel] 使用一般報表範本的試算表範本。 您可以選擇自訂 [!DNL Excel] 試算表以包含其他欄和圖表。

1. 在 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**，使用產生所需的報表型別 [!UICONTROL Date Aggregation] 「」單位[!UICONTROL Daily]」以及您想要的所有其他資料引數，將報表儲存為範本。

   >[!NOTE]
   >
   > * 您可以為建立試算表摘要 [!UICONTROL Portfolio]， [!UICONTROL Search Engine]， [!UICONTROL Search Engine Account]， [!UICONTROL Campaign]， [!UICONTROL Ad Group]， [!UICONTROL Ad Variation]， [!UICONTROL Keyword]、和 [!UICONTROL Forecast Accuracy] 報表。 如果您使用 [!UICONTROL Ad Group Report]，限制廣告群組的數量，以更快獲得結果。
   > * 此 [!UICONTROL Date Range] 不會使用範本中定義的單位。 您稍後設定試算表摘要時，會定義重新整理資料的日期。

1. 報告產生後，請前往 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** 並將報表輸出的TSV或XLS版本匯出至檔案。

1. 在 [!DNL Excel]，建立報表的自訂範本：

   1. 在中開啟報表檔案 [!DNL Excel].

   1. 準備活頁簿：

      1. 刪除顯示報表引數的前幾列。 若為XLS檔案，也刪除&quot;[!UICONTROL Total]&quot;列。 您可以選擇刪除某些資料列，但保留a)具有原始順序中所有欄的資料標題列，以及b)至少一個資料列。 請勿手動新增任何資料。

         >[!NOTE]
         >
         > 最後一欄必須包含非零的值。

      2. 依開始日期遞增順序排序資料（從最舊到最近）。

      3. 將工作表頁標名稱從「[!UICONTROL Sheet1]「至」[!UICONTROL RAW].」

         此特定索引標簽名稱可讓資料重新整理。

      4. （選用）視需要在報表範本的欄右側新增自訂欄。

   1. （選擇性）在個別的工作表上建立樞紐分析表。 完成後，在樞紐分析表的任何儲存格中按一下滑鼠右鍵，然後選取 **[!UICONTROL Pivot Table Options]**，按一下 **[!UICONTROL Data]** 標籤，然後選取 **[!UICONTROL Refresh data when opening the file]**.

   1. 將檔案另存為 [!DNL Excel] .XLSX格式的試算表。

>[!MORELIKETHIS]
>
>* [關於試算表報表摘要](spreadsheet-feed-about.md)
>* [建立試算表報表摘要](spreadsheet-feed-create.md)
>* [編輯試算表報表摘要設定](spreadsheet-feed-edit.md)
>* [試算表報表摘要設定](spreadsheet-feed-settings.md)
>* [檢視或儲存試算表報表摘要檔案](spreadsheet-feed-view-or-save.md)
>* [手動重新整理試算表報表摘要](spreadsheet-feed-refresh.md)
>* [刪除試算表報表摘要](spreadsheet-feed-delete.md)
