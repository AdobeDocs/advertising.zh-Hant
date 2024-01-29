---
title: 檢視刊登版位預測報表
description: 檢視針對某個投放位置的特定鎖定目標策略所預測的曝光數、花費和最佳最高出價。
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 檢視刊登版位預測報表

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

刊登版位預測工具會顯示特定鎖定目標策略的預測曝光次數、花費及最佳最高競標數。 預測是根據位置可用的整體詳細目錄和可用的不重複使用者來計算。

>[!NOTE]
>
>* 僅具有程式化預留(PG)目標定位的刊登版位不會產生任何預測，因為可用性和支出是決定性的。

## 預測中的資訊

預測包含下列資訊：

* **[!UICONTROL Summary]：**

   * **[!UICONTROL Estimated CPM]：** 鎖定目標設定可預期達到的預計每千次曝光成本(eCPM)。

   * **[!UICONTROL Budget]：** 目標設定的估計預算。

   * **[!UICONTROL Impression]：** 鎖定目標設定的預估曝光次數。

* **[!UICONTROL Budget Yield Curve]：** 如果所有其他目標設定相同，則位置可在不同預算層級提供的預估曝光次數。

* **[!UICONTROL Max Bid Yield Curve]：** 當所有其他鎖定目標設定相同時，不同「最高出價」等級位置的預估支出。

* **[!UICONTROL Message]：** 提供有關預測輸出的資訊，包括無法產生預測的任何案例。 此外也會反白標示已檢閱但因資料缺乏而未在該情境中考慮的任何目標定位設定。

### 預算計算

* 對於未指派給套件的刊登版位，會使用刊登版位預算進行計算。 在飛行中，會計算相同的整體預算。

* 若是套件中的刊登版位，則會使用指派給刊登版位的預算進行計算。 在飛行期間，會計算分配給此位置的預算，並將其包含在訊息中。

* 對於已在傳輸中新增至套件的刊登版位，預算會根據刊登版位數量平均分配。 當位置上線時，會計算套件指派的預算。

## 需求

* 最低支出：每日$25或相等金額的當地貨幣（每個位置）。

* 最大支出：每日$15,000或相等金額的當地貨幣（每個位置）。

* 最低最高出價、最高出價：位置型別有最低最高出價（適用於預算良率曲線）和最高出價（適用於最高出價良率曲線）。 這些值在整體上為真，不考慮地區變異。 有時，這些值對於目標區域可能太高或太低。

* 歷史資料：如果有足夠的歷史資料，就可以使用位置預測。 以下是歷史資料可能不足時的範例：

   * 此位置會定位行銷活動的新區域。

   * 此位置會鎖定行銷活動的新詳細目錄交易。

   * 此版位使用新的行銷活動廣告型別。

     刊登版位通常是供應端平台所定義的多個廣告範本集合。 因此，即使刊登版位已存在很長時間，基礎廣告範本仍可能是新的，且預測工具將無法預測。

## 開啟刊登版位預測報表

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱，然後按一下 **[!UICONTROL Placements]**.

1. 在位置名稱旁，按一下  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. 找到 **[!UICONTROL Forecast]** 區段中的左側邊欄。 如有必要，請按一下 ![預測](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* 有時候，由於瀏覽器快取，預測可能無法使用。 如果發生此情況，請清除快取並重試。

>[!MORELIKETHIS]
>
>* [Campaign Management檢視中的效能報表型別](campaign-reports-about.md)
>* [檢視位置診斷報告](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
