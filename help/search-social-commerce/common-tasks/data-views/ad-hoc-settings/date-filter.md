---
title: 依日期範圍篩選資料
description: 瞭解如何使用全域日期範圍篩選器。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 依日期範圍篩選資料

<!-- The same in new UI and legacy CM views -->

除了您已儲存特定日期範圍的預設和自訂檢視外，相同的全域日期範圍篩選器會套用至所有廣告商的大部分資料檢視。 行銷活動管理檢視的系統預設日期範圍是「昨天」。

您的日期範圍設定會儲存至瀏覽器專用的Cookie，因此您每次使用相同的瀏覽器應用程式登入時，都會針對所有廣告商使用日期範圍篩選器的任何變更，直到您變更篩選器或刪除Cookie為止。 您使用的每個瀏覽器應用程式都會將日期範圍篩選設定儲存在不同的Cookie中。

當您儲存預設檢視或自訂檢視的特定日期範圍時，無論您使用何種瀏覽器應用程式，該範圍都會在您套用檢視時套用。

>[!NOTE]
>
>* 您可以檢視前13個月的資料，但任何現有的自訂檢視最多只能包含前180天的資料。
>* 若要檢視先前的資料，請移至[[!UICONTROL Reports]檢視](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)並執行基本報表。
>* 您也可以儲存[預設檢視或自訂檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)的日期範圍。

## 變更行銷活動檢視中的全域日期篩選器

1. 在「搜尋\>促銷活動\>促銷活動」中的任何資料表上方，按一下目前的日期範圍。

1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;欄位中，指定範圍：

   * 預設範圍：從一般時間增量清單中選取，範圍從&#x200B;*[!UICONTROL Today]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 預設值為&#x200B;*[!UICONTROL Yesterday]*。

   * 針對特定範圍：選取&#x200B;**[!UICONTROL Custom Date Range]** ，然後指定開始日期和結束日期。

     以MM/DD/YYYY或MM-DD-YYYY格式輸入日期，或按一下每個欄位旁的![行事曆圖示](/help/search-social-commerce/assets/calendar.png "行事曆圖示")以開啟行事曆並選取日期。

1. （選用）比較指定日期範圍的資料與第二個日期範圍的資料：

   1. 將&#x200B;**[!UICONTROL Comparison]**&#x200B;滑桿移動到「開啟」位置。

      選取此選項時，會為每個一般資料欄新增兩個額外的欄。 例如，此表格不只包含&quot;[!UICONTROL Impressions]&quot;的一欄，而包含&quot;[!UICONTROL Impressions R1]&quot;、&quot;[!UICONTROL Impressions R2]&quot;及&quot;[!UICONTROL Impressions Diff]&quot;的欄。  如果您匯出資料，則相同的欄會拼寫為&quot;[!UICONTROL Impressions Range 1]&quot;&quot;&quot;[!UICONTROL Impressions Range 2]&quot;和&quot;[!UICONTROL Impressions Difference]&quot;。

   1. 指定第二個日期範圍。

   1. 在「\[_資料欄位_\] Difference」欄，選擇如何表示兩個選取的日期範圍之間的資料差異：

      * *[!UICONTROL Variance]* （預設）：將差異顯示為數值。

      * *[!UICONTROL % Change]：*&#x200B;以百分比顯示差異。

1. 按一下&#x200B;**[!UICONTROL Apply]**。
