---
title: 依日期範圍篩選資料
description: 瞭解如何使用全域日期範圍篩選器。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 依日期範圍篩選資料

除了您已儲存特定日期範圍的預設和自訂檢視外，相同的全域日期範圍篩選器會套用至所有廣告商的大部分行銷活動資料檢視。 行銷活動管理檢視的系統預設日期範圍是「昨天」。

您的日期範圍設定會儲存至瀏覽器專用的Cookie，因此您每次使用相同的瀏覽器應用程式登入時，都會針對所有廣告商使用日期範圍篩選器的任何變更，直到您變更篩選器或刪除Cookie為止。 您使用的每個瀏覽器應用程式都會將日期範圍篩選設定儲存在不同的Cookie中。

當您儲存預設檢視或自訂檢視的特定日期範圍時，無論您使用何種瀏覽器應用程式，該範圍都會在您套用檢視時套用。

>[!NOTE]
>
>* 您可以檢視前13個月的資料，但任何現有的自訂檢視最多只能包含前180天的資料。
>* 若要檢視先前的資料，請前往 [[!UICONTROL Reports] 檢視](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 並執行基本報表。
>* 您也可以儲存的日期範圍 [預設檢視或自訂檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## 變更行銷活動檢視中的全域日期篩選器

1. 在「搜尋\>促銷活動\>促銷活動」中的任何資料表上方，按一下目前的日期範圍。

1. 在 **[!UICONTROL Date Range]** 欄位，指定範圍：

   * 針對預設範圍：從常用時間增量清單中選取，範圍介於 *[!UICONTROL Today]* 至 *[!UICONTROL Last 180 Days]*. 預設值為 *[!UICONTROL Yesterday]*.

   * 針對特定範圍：選取 **[!UICONTROL Custom Date Range]** ，然後指定開始日期和結束日期。

     以YYYY/MM/DD或YYYY-MM-DD格式輸入日期，或按一下 ![行事曆圖示](/help/search-social-commerce/assets/calendar.png "行事曆圖示") 在每個欄位旁邊，開啟行事曆並選取日期。

1. （選用）比較指定日期範圍的資料與第二個日期範圍的資料：

   1. 移動 **[!UICONTROL Comparison]** 滑桿至 *[!UICONTROL On]*.

      選取此選項時，會為每個一般資料欄新增兩個額外的欄。 例如，不要只包含&quot;[!UICONTROL Impressions]，」此表格包括「[!UICONTROL Impressions R1]，&quot; &quot;[!UICONTROL Impressions R2]，」和「[!UICONTROL Impressions Diff].」  如果您匯出資料，則相同的欄會拼寫為&quot;[!UICONTROL Impressions Range 1]，&quot; &quot;[!UICONTROL Impressions Range 2]，」和「[!UICONTROL Impressions Difference].」

   1. 指定第二個日期範圍。

   1. 在「\[」中選擇如何表示兩個所選日期範圍之間的資料差異&#x200B;_資料欄位_\] Difference」欄：

      * *[!UICONTROL Variance]* （預設）：以數值顯示差異。

      * *[!UICONTROL % Change]：*  以百分比顯示差異。

1. 按一下 **[!UICONTROL Apply]**.
