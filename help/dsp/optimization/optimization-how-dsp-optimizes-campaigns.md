---
title: DSP如何最佳化您的行銷活動
description: 瞭解DSP如何最佳化行銷活動中的套件。
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Advertising DSP如何最佳化您的行銷活動

此頁面概述由[!DNL Adobe AI]提供支援的DSP最佳化引擎如何最佳化行銷活動中的套件。 如需手動最佳化行銷活動的相關秘訣與技巧，請聯絡您的Adobe客戶團隊。<!-- add link to trading playbook if we add it to help -->

套件最佳化目標會在兩個層級運作：

* 對於每個套件：DSP會根據位置對選定KPI的效能，將預算分配給套件中的每個位置。

* 對於套件中的每個刊登版位/拍賣： DSP會計算每個刊登版位每個拍賣的即時經濟KPI值，然後使用此值來決定競標。

  >[!NOTE]
  >
  >經濟價值會根據刊登花費的程度而大幅加權。 如果刊登版位落後於其支出目標，則可購買較低品質的拍賣。 如果刊登版位輕鬆達成其花費目標，則焦點會移至品質較高的拍賣。

## 套件最佳化

DSP能以兩種基本方式將您的傳送最佳化，有20種變數可用來符合您特定的效能目標。 您可以選擇：

* 排定效能比率的優先順序

* 優先平衡成本效益與效能比

檢視[最佳化目標及使用方式](optimization-goals.md)，以判斷哪些最佳化目標可協助您達成KPI。

### 排定效能率優先順序的套裝程式

針對將效能率排定優先順序的最佳化目標，DSP會預測每個拍賣的效能，並一律以最高出價競標。 適用的最佳化目標範例包括[!UICONTROL Highest Viewability Rate]、[!UICONTROL Highest Clickthrough Rate]等。

此最佳化模式適用於以下情況：

* 您已經知道有效/可接受的CPM層級（例如歷史基準）。

* 如果您在縮放時遇到問題，您願意手動調整每個位置的[!UICONTROL Max Bid]。

* 您正在將規模優先於效率。

#### 步調邏輯 {#pacing-logic-performance}

* 如果支出如期進行，出價就會更具選擇性，因此您只能在預計有高績效率的拍賣上出價。

* 如果支出落後於節奏，出價就會減少選擇性，這樣您就可以在預計效能比較低的拍賣會上出價，以趕上節拍目標。

#### 結算價格/競標著色 {#clearing-price-performance}

在執行步調邏輯後，DSP會透過結算價格預測模型執行提議的競標。 如果預測指出出價可以以最低限度的成功率降低而降低，則根據預測會降低出價。

### 排定成本效益與效能比之間平衡優先順序的套件

針對某些最佳化目標，DSP會預測每個拍賣的效能，並自動調整競標價格，不會超過刊登的[!UICONTROL Max Bid]。 適用的最佳化目標範例包括[!UICONTROL Lowest CPM]、[!UICONTROL Lowest CPA]、[!UICONTROL Lowest Cost per View]、[!UICONTROL Lowest Cost per Click]等。

#### 步調邏輯 {#pacing-logic-balanced}

* 如果消費如期進行，DSP就會變得對價格比較敏感，降低出價金額，以透過步調計畫來權衡中標率。

* 如果同時平衡績效量度（除了[!UICONTROL Lowest CPM]以外的所有目標），則預測的KPI會混合到競標量中。 因此，您針對「每筆成本」預測效能更高的拍賣，出價更高。

* 如果支出落後於節奏，則DSP會降低價格敏感性，並會競標更高的金額（最高至[!UICONTROL Max Bid]），以透過節拍計畫來平衡中標率。

#### 結算價格/競標著色 {#clearing-price-balanced}

在執行步調邏輯後，DSP會透過結算價格預測模型執行提議的競標。 如果預測指出出價可以以最低限度的成功率降低而降低，則根據預測會降低出價。

## 位置最佳化

位置競標前篩選器是確保強大效能的最嚴格方式。 DSP會策略性地跨不同的廣告型別使用競標前篩選器，以達到每個套件中各個位置的效能目標。 您可以同時將競標前篩選器與套件層級最佳化搭配使用，或單獨使用。

>[!NOTE]
>
>可用的競標前篩選器會依廣告型別而異。 例如，對於標準顯示位置，您可以按點進率和可檢視度進行篩選，但不能按完成率進行篩選。

請參閱[位置層級出價前篩選條件及使用方式](optimization-pre-bid-filters.md)，判斷哪個出價前篩選條件可以協助您達成KPI。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [位置層級競標前篩選及使用方式](optimization-pre-bid-filters.md)
>* [疑難排解效能](/help/dsp/optimization/troubleshooting-performance.md)
