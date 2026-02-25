---
title: （新UI）檢視檢視產品組合績效詳細資料
description: 瞭解如何檢視產品組合績效詳細資料，包括產品組合層級和每個指派行銷活動的實際和預測量度。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: e786ffc8c9e331fffcc8b0f7cce4cb082baea6ac
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# （新UI）檢視產品組合績效詳細資料

*Beta功能*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

產品組合詳細資料檢視包含有關產品組合的下列資訊：

* 最多三個效能量度的實際和預測值。 報表包含投資組合的量度值總計以及依日期的量度劃分。<!-- Not for active portfolios only?  -->

* 使用中投資組合的模型準確性資料，顯示模型與預測的偏差程度。 此報表顯示整體每日或滾動七天成本準確度、點按準確度及目標值準確度。

  您可以按一下日期（預設）或按交易日期來檢視資料。   您也可以趨勢圖（預設）或表格形式來檢視資料。

* 目標支出與作用中投資組合的實際支出。 您也可以選擇納入投資組合的行銷活動預算總計。

* 廣告網路對使用中投資組合的成本、點選或[目標值](/help/search-social-commerce/glossary.md#o-p)預測的準確度。<!-- Verify -->

* 投資組合設定。

  您可以選擇開啟投資組合設定進行編輯。

## 開啟投資組合的效能詳細資料

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 按一下投資組合名稱。

1. （選擇性）從&#x200B;**[!UICONTROL Granularity]**&#x200B;功能表，變更介於&#x200B;*[!UICONTROL Daily]、*、*[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]之間的資料粒度。*

1. （選擇性）若要變更產品組合詳細資料的日期範圍，請按一下右上方的日期範圍、指定日期範圍，然後按一下&#x200B;**[!UICONTROL Apply]**。

## 自訂[!UICONTROL Portfolio Overview]索引標籤

* （選用）若要自訂[!UICONTROL Portfolio Performance]報表，請執行下列任一項作業：

   * 若要變更用於總計度量和詳細度量的效能度量，請按一下&#x200B;**[!UICONTROL Metrics]**&#x200B;並選取最多三個度量。

     預設量度為&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*&#x200B;和&#x200B;*[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * 如需詳細量度：

      * 將開關移動到&#x200B;**[!UICONTROL Display predictions]**&#x200B;旁以顯示或隱藏預測的量度值。

      * 在圖表檢視（![圖表檢視](/help/search-social-commerce/assets/chart-view.png "圖表檢視")）和表格檢視(![表格檢視](/help/search-social-commerce/assets/table-view.png "表格檢視"))之間切換。

      * （在圖表檢視中）若要檢視圖表上任何點的資料，請將游標停留在該點上。

* （選用）若要自訂[!UICONTROL Model accuracy]趨勢圖，請執行下列任一項作業：

   * 在圖表檢視（![圖表檢視](/help/search-social-commerce/assets/chart-view.png "圖表檢視")）和表格檢視(![表格檢視](/help/search-social-commerce/assets/table-view.png "表格檢視"))之間切換。

   * 依&#x200B;*[!UICONTROL Click Date]*&#x200B;與&#x200B;*[!UICONTROL Transaction Date]*&#x200B;切換檢視資料。

   * 在檢視&#x200B;*[!UICONTROL Daily Accuracy]*&#x200B;和&#x200B;*[!UICONTROL 7 Day Rolling Accuracy]*&#x200B;的相關資料之間切換。

     [!UICONTROL 7 Day Rolling Accuracy]是前七天預測的平均準確度，以百分比表示。 例如，2025年5月8日的值是2025年5月1日至5月7日期間的平均準確度。

   * （在圖表檢視中）若要檢視圖表上任何點的資料，請將游標停留在該點上。

* （選用）若要自訂[!UICONTROL Target vs actual spend]趨勢圖，請執行下列任一項作業：

   * 將開關移至&#x200B;**[!UICONTROL Display budget]**&#x200B;旁以顯示或隱藏每個日期的行銷活動總預算。

   * 若要檢視圖表上任何點的資料，請將游標停留在該點上。

* （選用）若要自訂[!UICONTROL Network Accuracy]趨勢圖，請執行下列任一項作業：

   * 將報告的量度變更為&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*&#x200B;或&#x200B;*[!UICONTROL Objective Value]*。

   * 若要檢視圖表上任何點的資料，請將游標停留在該點上。

1. 按一下&#x200B;**[!UICONTROL Download report]**。

## 列出產品組合中的行銷活動

* 按一下「**[!UICONTROL Campaigns]**」標籤。

## 列出投資組合中的廣告群組

* 若要檢視產品組合內行銷活動中的所有廣告群組，請按一下「**[!UICONTROL Campaigns]**」標籤，然後按一下行銷活動名稱。

## 列出投資組合中的關鍵字

* 若要檢視投資組合中的所有關鍵字，請按一下&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤。

* 若要檢視產品組合內廣告群組中的所有關鍵字，請按一下&#x200B;**[!UICONTROL Ad Groups]**&#x200B;標籤，然後按一下廣告群組名稱。

## 檢視和編輯投資組合設定

* 若要檢視或隱藏投資組合設定，請按一下&#x200B;**[!UICONTROL Portfolio Settings]**。

   * 若要編輯可見的投資組合設定，請按一下設定區段旁的![編輯](/help/search-social-commerce/assets/edit.png "編輯")，然後[編輯投資組合設定](portfolio-edit.md)。

如需產品組合設定的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

## 下載投資組合效能報表和投資組合元件清單

* 若要下載所有報表：

   1. 在工具列中按一下&#x200B;**[!UICONTROL Download report]**。

   1. 選取每個效能報表旁的核取方塊，並選取要納入的組合元件型別。

      對於某些效能報表，您可以選擇將資料下載為圖表或表格。

   1. 按一下&#x200B;**[!UICONTROL Download report]**。

* 若要下載包含特定資料型別的[!DNL model accuracy]報表：

   1. 在報表的工具列中，按一下&#x200B;**[!UICONTROL Download report]**。

   1. 選取要包含的每種資料型別旁的核取方塊，以及如何劃分資料（依競標單位及/或按一下磁碟區）。

   1. 按一下&#x200B;**[!UICONTROL Download report]**。

>[!MORELIKETHIS]
>
>* [（新UI）關於投資組合](portfolio-about.md)
>* [ （新使用者介面）編輯投資組合](portfolio-edit.md)
>* [ （新UI）在[!UICONTROL Portfolios]檢視中下載資料](portfolio-view-report.md)
