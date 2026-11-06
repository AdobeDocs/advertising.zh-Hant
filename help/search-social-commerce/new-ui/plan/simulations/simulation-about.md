---
title: 關於模擬
description: 瞭解產品組合模擬。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
TQID: 'https://experienceleague.adobe.com/9B4gKrZnnUmgj0LzxwM2CIkJsIO9Pe9R8RDR4mAmIwo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%
---
# 關於模擬

*Beta功能*

模擬報表顯示預估邊際成本與目標值、成本、點按次數，以及不同支出（成本）層次的產品組合所預期的目標值，以及對應的每日預算或其他目標。 您可以選擇性[自訂檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)，以檢視其他流量量度、模擬設定，以及僅特定模擬型別（[!UICONTROL Weekly]或[!UICONTROL Custom]）。

<!--
 Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## 模擬型別

* 每週自動模擬

* 自訂、使用者產生的模擬

### 每週自動模擬

搜尋、Social和Commerce每週都會使用目前的產品組合設定自動執行模擬報表。 每週自動模擬僅適用於投資組合為[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)的期間。

您可以從[!UICONTROL Portfolios]檢視](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations)中[下載所選執行日期最多100個投資組合的每週模擬，或從[!UICONTROL Simulations]檢視](simulation-download.md)中[下載個別模擬。

#### 每週下載的模擬

您可以將每週的模擬下載為個別活頁簿，或將它們合併到一個活頁簿中。 每個模擬的報表包含20個步驟層次中每個層次的目標，以及目標中的預計成本、點選次數、加權收入（目標值）和轉換量度（根據對應目標）。 模擬會計算前20個沒有限制的資料列，以及剩餘的具有限制的資料列。

#### 熒幕上每週模擬詳細資料

熒幕上的模擬詳細資訊會顯示產品組合層級的視覺化與表格式深入分析。 針對依促銷活動、廣告群組、競標單位或裝置區分的資料，請[改為下載模擬](simulation-download.md)。

##### 圖表檢視

圖形檢視會針對20個支出層級中的每一個顯示支出目標的預期目標值或其他指定量度([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->)。 圖表會識別目標中點，您可以選擇變更目標中點，以檢視使用該值的預測資料。 將游標放在圖形中的任何點上，即可檢視該點的資料。

您可以檢視具有限制、無限制或兩者兼有的資料。 當您檢視含有限制的資料時，檢視會識別圖形上方的那些限制。

##### 表格檢視

表格檢視會顯示20個支出層次中每個層次的目標支出。 它也會包含每個支出層次之投資組合目標中的對應估計成本、目標值的邊際成本、點按數、目標值和轉換量度。 此表格會識別目標中點，您可以選擇變更目標中點，以檢視使用該值的預測資料。

您可以檢視具有限制、無限制或兩者兼有的資料。 當您檢視含有限制的資料時，檢視會識別圖形上方的那些限制。

##### 模擬設定

檢視會在圖形或表格下方顯示唯讀的模擬設定。

##### Portfolio設定

若要檢視適用投資組合的唯讀設定，請按一下右上角的&#x200B;**[!UICONTROL Portfolio Settings]**。

### 自訂、使用者產生的模擬

您可以使用目前的產品組合設定，或使用自訂產品組合設定（無論是否套用競標單位層級限制），為單一[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)產品組合建立自訂模擬報告，以檢視這些設定所產生的結果，而不會實際變更它們。 例如，您可以建立自訂模擬，以檢視使用不同支出策略或學習預算的效果，而不考慮投資組合中競標單位的現用限制。 您可以在產品組合、行銷活動、競標單位和裝置層級檢視預估效能。

#### 下載的自訂模擬

您可以將自訂模擬下載為個別活頁簿，或將它們合併到一個活頁簿中。 每個模擬的報表都包含您指定之每個實體層次（產品組合、行銷活動、廣告群組、競標單位）的一個工作表（當該層次有資料可用時）。 當您指定裝置層級資料時，每個工作表都會包含[!UICONTROL Device]欄。 每個工作表都包含每個適用實體的一列，當您請求裝置層級資料時，每個步驟都會包含裝置型別（例如，每個行銷活動各一列）。 每一列的資料包括目標中的預計邊際成本對收入、成本、點按數、加權收入（目標值）、裝置型別和轉換量度（根據對應目標）。 產品組合層次工作表也包含步驟層次的目標，而實體層次工作表則包含廣告網路、帳戶、促銷活動及（若適用）廣告群組。  <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### 熒幕上的自訂模擬詳細資料

熒幕上的模擬詳細資訊會顯示產品組合層級的視覺化與表格式深入分析。 針對依促銷活動、廣告群組、競標單位或裝置區分的資料，請[改為下載模擬](simulation-download.md)。

#### 圖表檢視

圖形檢視會顯示模擬的指定花費層次（步驟）數目之花費目標的預期目標值或其他指定量度([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->)。 圖表可識別目標中點。 將游標放在圖形中的任何點上，即可檢視該點的資料。

當模擬計入限制時，檢視表會識別圖形上方的那些限制。

##### 表格檢視

表格檢視表會顯示每個指定數目的模擬花費層次（步驟）的目標支出。 它也會針對每個支出層級，顯示產品組合目標中的對應估計成本、目標值的邊際成本、點按數、目標值和轉換量度。 此表格可識別目標中點。

當模擬計入限制時，檢視表會識別圖形上方的那些限制。

##### 模擬設定

檢視會在圖形或表格下方顯示唯讀的模擬設定。

##### Portfolio設定

若要檢視適用投資組合的唯讀設定，請按一下右上角的&#x200B;**[!UICONTROL Portfolio Settings]**。

## [!UICONTROL Simulations]檢視

[!UICONTROL Simulations]檢視會列出每週模擬和自訂模擬。 管理員和其他使用者型別<!-- Verify which -->可以看到其他使用者建立的自訂模擬。 所有其他使用者只能看到他們建立的自訂模擬。

資料表格會顯示每個模擬的進度；每一列的[!UICONTROL Target Midpoint]；以及成本/曝光數/點選/目標值預測、實際值和準確度的欄。 您可以選擇新增其他自訂欄（包括提升度量度，例如實際目標值除以成本）。

### 可用動作 {#simulations-actions}

* [自訂檢視表](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)以包含其他量度，包括預估曝光數；實際成本、點按次數、曝光數和目標值；成本對目標的值；成本準確度、點按準確度、目標值準確度；以及預測與實際目標值與成本對目標值之間的差異（差異）。 您也可以包含大部分模擬設定和模擬型別（[!UICONTROL Custom]或[!UICONTROL Weekly]）的欄。

* [使用投資組合目前的設定作為預設值，為單一投資組合產生自訂模擬](simulation-create.md#simulation-create)。

* [使用現有的設定重新執行最多10個模擬](simulation-create.md#rerun-a-simulation-with-the-existing-settings)。 搜尋、Social和Commerce會略過狀態為[!UICONTROL Queued]或[!UICONTROL In Progress]的模擬。

* [在熒幕上檢視每週或自訂的模擬](simulation-view.md)。

* [每週下載最多10個自訂模擬](simulation-download.md)，作為單一[!DNL Microsoft Excel]活頁簿或ZIP檔案中的個別活頁簿。

* 使用[!UICONTROL Spend Planner]按鈕，開啟舊版支出建議工具，協助您識別產品組合間的最佳支出分配。

## 最佳實務

在下列情況下監視模擬報告：

* 在您啟動產品組合以透過對應的產品組合設定來預估可預期的效能之前，請至少使用兩週的資料。 如果模擬結果顯示效能低於您根據所包含行銷活動的歷史資料所預期的效能，請在啟動產品組合之前調查並解決問題。

* 在投資組合發生任何重大變更後（例如新增行銷活動或變更目標）。 如果您變更投資組合的模型開始日期、轉換量度的權重，或目標的點按值，則等到第二天17:00 PST之後再執行模擬，此時有更新的成本和收入模型可用。

* 定期監視轉換量度層級的效能趨勢。

>[!MORELIKETHIS]
>
>* [執行或重新執行模擬](simulation-create.md)
>* [檢視模擬詳細資料](simulation-view.md)
>* [下載模擬](simulation-download.md)
