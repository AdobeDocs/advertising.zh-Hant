---
title: 關於DSP Planner工具
description: 瞭解規劃工具，以根據指定的預算與目標定位條件，預測連線電視(CTV)刊登位置的獨特觸及率。
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# 關於DSP Planner工具

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta功能*

在您開始花費存貨之前，規劃工具可協助您根據指定的預算與目標定位條件，預測連線電視(CTV)刊登地點的住戶層級獨特觸及率。 評估多個觸及計畫後，您可以實施最符合套件和位置中所需結果的計畫。

供需規劃工具會使用過去90天的歷史競標、曝光數和觸及率資料，來估計計畫設定的不重複觸及數、平均CPM、平均頻率和曝光數。

## 供需規劃員預測

每個預測都由觸及預算預測曲線組成，該曲線顯示使用計畫設定可達到的觸及量。 將游標移至視覺效果上方，以檢視預算較高的遞增觸及商機。

![供需規劃員預測](/help/dsp/assets/planner-forecast.png "供需規劃員預測")

預測輸出也包含 [!UICONTROL Inventory Breakdown] 區段會說明不同的發佈者如何貢獻獨特的觸及率，從而提供有價值的探索機會。

>[!NOTE]
>
>* 此 [!UICONTROL Inventory Breakdown] 區段僅顯示私人和的資料 [!UICONTROL On Demand] 詳細目錄。
>* 針對兩個發佈者顯示的預估唯一觸及範圍可能重疊。

## 供需規劃員檢視

在 [!UICONTROL Planner] 檢視，您可以檢視現有的CTV觸及計畫並建立新計畫。

您也可以編輯、複製、匯出、封存或重新產生任何計畫的預測。

## 常見問答

+++供需規劃工具支援哪些型別的存貨？

供需規劃工具支援所有型別的詳細目錄，包括程式化保證(PG)、私人市場(PMP)、 [!UICONTROL On Demand]和公開。 若要產生準確的預測，請納入過去七天內至少50,000次曝光的交易。

+++

+++為什麼我看到&quot;[!UICONTROL Unable to generate forecast]？」

此錯誤最常見的原因之一是預算不足或最高競標。 為了獲得最佳結果，請使用至少5000美元的預算。 如果 [!UICONTROL Connected TV] 媒體型別已選取，請輸入至少10美元的最高出價。

此外，請確定包含的發行者或交易為作用中，且有最近的曝光活動。

+++

+++我根據預測建立了刊登版位，但並未達到觸及預測所指示的獨特觸及量。 為什麼？

觸及預測只是一個估計，而實際結果可能會因為多種經常變化的因素而有所差異，例如季節性、競標競爭力以及供給與需求。 它不一定完全正確，但對於深入分析行銷活動策略（可能會推動最佳結果）而言，最有用。

+++

+++供需規劃員是否可以使用相同的輸入設定產生不同的預測結果？

供需規劃員會根據最新觀察資料產生預測，因此預測輸出可能會在不同時間有所差異，即使計畫設定維持相同。 考慮為相同計畫產生多個預測，並為每個計畫匯出結果。

+++

+++我可以儲存供需規劃員預測輸出嗎？

可以，您可以將預測匯出至 [!DNL Microsoft Excel] 試算表（按一下） **[!UICONTROL ...]** > **[!UICONTROL Export]** 在右上角。 試算表會使用兩個資料欄，擷取觸及預算曲線中顯示的資訊： [!UICONTROL Budget] 和 [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [關於DSP Planner工具](planner-about.md)
>* [建立連線電視連線計畫](planner-create.md)
>* [複製連線電視連線計畫](planner-duplicate.md)
>* [編輯連線電視連線計畫](planner-edit.md)
>* [匯出連線電視觸及計畫](planner-export.md)
>* [重新產生連線電視觸及計畫的預測](planner-forecast.md)
>* [封存連線電視觸及計畫](planner-archive.md)
>* [連線電視連線方案的設定](planner-settings.md)
