---
title: 建立試算表報表摘要的 [!DNL Excel] 範本
description: 瞭解如何建立特別格式化的試算表範本。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 為試算表報表摘要建立[!DNL Excel]範本

*僅適用基本報告和模型準確度報告*

若要建立試算表摘要，您必須先使用一般報表範本建立特別格式化的[!DNL Microsoft Excel]試算表範本。 您可以選擇自訂[!DNL Excel]試算表以包含其他欄和圖表。

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;中，使用「[!UICONTROL Daily]」的[!UICONTROL Date Aggregation]單位並搭配您想要的所有其他資料引數，產生所需的報表型別，並將報表儲存為範本。

   >[!NOTE]
   >
   > * 您可以建立[!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]和[!UICONTROL Forecast Accuracy]報表的試算表摘要。 如果您使用[!UICONTROL Ad Group Report]，請限制包含的廣告群組數目，以更快獲得結果。
   > * 未使用範本中定義的[!UICONTROL Date Range]單位。 您稍後設定試算表摘要時，會定義重新整理資料的日期。

1. 產生報表之後，請前往「**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**」，並將報表輸出的TSV或XLS版本匯出至檔案。

1. 在[!DNL Excel]中，建立報告的自訂範本：

   1. 在[!DNL Excel]中開啟報告檔案。

   1. 準備活頁簿：

      1. 刪除顯示報表引數的前幾列。 若為XLS檔案，請一併刪除&quot;[!UICONTROL Total]&quot;列。 您可以選擇刪除某些資料列，但保留a)具有原始順序中所有欄的資料標題列，以及b)至少一個資料列。 請勿手動新增任何資料。

         >[!NOTE]
         >
         > 最後一欄必須包含非零的值。

      2. 依開始日期遞增順序排序資料（從最舊到最近）。

      3. 將工作表標簽名稱從&quot;[!UICONTROL Sheet1]&quot;變更為&quot;[!UICONTROL RAW]&quot;。

         此特定索引標簽名稱可讓資料重新整理。

      4. （選用）視需要在報表範本的欄右側新增自訂欄。

   1. （選擇性）在個別的工作表上建立樞紐分析表。 完成後，在樞紐分析表的任何儲存格中按一下滑鼠右鍵，然後選取&#x200B;**[!UICONTROL Pivot Table Options]**，按一下&#x200B;**[!UICONTROL Data]**&#x200B;索引標籤，然後選取&#x200B;**[!UICONTROL Refresh data when opening the file]**。

   1. 將檔案儲存為.XLSX格式的[!DNL Excel]試算表。

>[!MORELIKETHIS]
>
>* [關於試算表報表摘要](spreadsheet-feed-about.md)
>* [建立試算表報表摘要](spreadsheet-feed-create.md)
>* [編輯試算表報表摘要設定](spreadsheet-feed-edit.md)
>* [試算表報表摘要設定](spreadsheet-feed-settings.md)
>* [檢視或儲存試算表報表摘要檔案](spreadsheet-feed-view-or-save.md)
>* [手動重新整理試算表報表摘要](spreadsheet-feed-refresh.md)
>* [刪除試算表報表摘要](spreadsheet-feed-delete.md)
