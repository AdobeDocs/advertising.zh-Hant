---
title: 依日期範圍篩選資料
description: 瞭解如何使用全域日期範圍篩選器。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 968023d95217d4d17b1441ae717f3e472b31f7c4
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%
---
# 依日期範圍篩選資料

使用日期範圍篩選器來指定要顯示效能資料的期間。 在支援日期比較的檢視中，您也可以比較兩個期間的績效。

## （新UI）變更日期範圍 {#date-filter-new-ui}

1. 在頁首中，按一下日期範圍控制項與行事曆圖示。

1. 指定日期範圍：

   * 若要使用預設範圍，請從第一個行事曆上方的選單中選取選項，例如&#x200B;**[!UICONTROL Yesterday]**&#x200B;或&#x200B;**[!UICONTROL Last 7 Days]**。

   * 若要使用自訂範圍，請選取&#x200B;**[!UICONTROL Custom Date Range]**&#x200B;並在行事曆中選取開始和結束日期。 使用日曆箭頭在月份之間導覽。

1. 按一下&#x200B;**[!UICONTROL Apply]**。

## （新UI）比較兩個期間的資料 {#compare-periods-new-ui}

*只支援日期比較的檢視*

1. 在頁首中，按一下日期範圍控制項與行事曆圖示。

1. 開啟&#x200B;**[!UICONTROL Compare Periods]**。

   兩個日曆面板並排顯示。 第一個期間有藍色標籤，而比較期間有紫色標籤。

1. 在第一個面板中，指定日期範圍：

   * 若要使用預設範圍，請從第一個行事曆上方的選單中選取選項，例如&#x200B;**[!UICONTROL Yesterday]**&#x200B;或&#x200B;**[!UICONTROL Last 7 Days]**。

   * 若要使用自訂範圍，請選取&#x200B;**[!UICONTROL Custom Date Range]**&#x200B;並在行事曆中選取開始和結束日期。 使用日曆箭頭在月份之間導覽。

1. 在第二個面板中，選取比較預設集或按一下日曆中的開始日期。

   比較期間與第一個期間的天數相同。 檢閱兩個行事曆上完整的日期範圍。

1. 從&#x200B;**[!UICONTROL Comparison Format]**&#x200B;中，選取差異的顯示方式：

   * **[!UICONTROL As percentage]：**&#x200B;以百分比顯示差異。

   * **[!UICONTROL As variance]：**&#x200B;將差異顯示為數值。

1. 按一下&#x200B;**[!UICONTROL Apply]**。

   日期範圍控制項會顯示兩個完整的日期範圍及其期間標籤和顏色標籤。 每個可比較的量度會分組為兩個期間欄和一個&#x200B;**[!UICONTROL Change]**&#x200B;欄。 無法比較的欄位會保持為單一欄。 欄標題中的期間標籤可識別對應的日期範圍。

若要停止比較期間，請開啟日期範圍控制項，關閉&#x200B;**[!UICONTROL Compare Periods]**，然後按一下&#x200B;**[!UICONTROL Apply]**。 關閉比較會根據比較資料清除篩選器。

### 從欄功能表變更比較格式

1. 啟用日期比較後，請開啟&#x200B;**[!UICONTROL Change]**&#x200B;欄的欄標題功能表，或可比較量度的期間欄。

1. Select **[!UICONTROL As percentage]**&#x200B;或&#x200B;**[!UICONTROL As variance]**。

   選取範圍會套用至資料表格中的所有比較量度，而不僅僅是選取的欄。 日期範圍控制項會與選取專案同步，且格式會在目前廣告商的適用頁面之間共用，包括已儲存日期範圍的檢視。

   資料表成功重新整理後，會顯示一則確認訊息。 如果資料表格無法以選取的格式重新整理，則會出現錯誤訊息；請嘗試再次選取格式。

在支援的欄功能表中，排序和篩選選項仍然可用。

## （舊版UI）日期範圍設定

除了您已儲存特定日期範圍的預設和自訂檢視外，相同的全域日期範圍篩選器會套用至所有廣告商的大部分資料檢視。 行銷活動管理檢視的系統預設日期範圍是「昨天」。

您的日期範圍設定會儲存至瀏覽器專用的Cookie，因此您每次使用相同的瀏覽器應用程式登入時，都會針對所有廣告商使用日期範圍篩選器的任何變更，直到您變更篩選器或刪除Cookie為止。 您使用的每個瀏覽器應用程式都會將日期範圍篩選設定儲存在不同的Cookie中。

當您儲存預設檢視或自訂檢視的特定日期範圍時，無論您使用何種瀏覽器應用程式，該範圍都會在您套用檢視時套用。

>[!NOTE]
>
>* 您可以檢視前13個月的資料，但任何現有的自訂檢視最多只能包含前180天的資料。
>* 若要檢視先前的資料，請移至[[!UICONTROL Reports]檢視](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)並執行基本報表。
>* 您也可以儲存[預設檢視或自訂檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)的日期範圍。

## （舊版UI）變更行銷活動檢視中的全域日期篩選器

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
