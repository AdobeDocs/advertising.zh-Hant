---
title: 位置層級競標前篩選器及其使用方式
description: 參考可用的位置層級競標前篩選器，並瞭解其使用方式。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 位置層級競標前篩選器及其使用方式

| 競標前篩選 | 說明 | 使用此篩選器的時間 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 設定拍賣可能導致點進的機率的最小預測臨界值。 例如，如果您將臨界值設為0.1%，則只有在預測的點按機率大於或等於0.1%時，才會對拍賣競標。<br><br><b>注意：</b>篩選器是在最佳化目標之前套用。 因此，非常嚴格的篩選條件可以防止支出。 | 若您的點進率(CTR)具有最低KPI目標，且當CTR低於臨界值時您不想花費預算，請使用。 此篩選器可能相當具限制性，因此設定現實目標很重要。 根據位置的其他限制，目標為0.03-.07%通常是良好的起點。 您可以視需要在網站層級最佳化此專案，協助改善量度。<br><br>如果您的目標是要達到最小CTR和最佳CPM，則建議的設定是將[!UICONTROL Click Through Rate]篩選器與最佳化目標&quot;[!UICONTROL Lowest CPM]&quot;相結合。 如果您的目標是最大CPM，但沒有實際達成超額目標的好處，以及最小CTR，則將[!UICONTROL Click Through Rate]篩選器與最佳化目標&quot;[!UICONTROL Always Max Bid + Highest CTR]&quot;配對可能更合適。 |
| [!UICONTROL 100% Completion Rate] | 設定您對曝光競標之前必須符合的必要最低完成率。 | 當行銷活動的主要目標是完成率時，請使用此篩選器。 其他鎖定目標引數中的因數，但建議起始百分比為65%。 |
| [!UICONTROL Player Size - Adobe] | 使用DSP中的資料設定所需的最小播放器大小。 當符合[!UICONTROL Player Size]臨界值時，您就可以對曝光出價。 | 使用可確保您可使用DSP中的資料實現全集播放器詳細目錄。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用來自[!DNL Moat]或[!DNL Integral Ad Science] ([!DNL IAS])的資料，設定必要的播放器大小下限。 當符合[!UICONTROL Player Size]臨界值時，您就可以對曝光出價。 | 使用確保您使用平台範圍[!DNL Moat]或[!DNL IAS]資料傳遞全集播放器詳細目錄。<br><br><b>注意：</b>只有當行銷活動設定為使用[!DNL Moat]或[!DNL IAS]資料時，才使用此篩選器。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用DSP可檢視度數字和測量，設定必要的最低可檢視度百分比。 當符合指定的臨界值時，您就可以對曝光次數投標。<br><br><b>附註：</b><ul><li>如果促銷活動的[!UICONTROL Viewability Sensitivity]設定為「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]」，則促銷活動會使用[!DNL Media Rating Council] (MRC)可檢視度測量標準。 如果[!UICONTROL Viewability Sensitivity]設定為「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]」，則會將[!DNL GroupM]可檢視度測量標準用於此行銷活動。</li><li>Adobe測量定義與第三方定義不同，因此可能與第三方資料略有差異。</li></ul> | 最佳實務是將最佳化目標和任何競標前篩選設定與行銷活動的[!UICONTROL Viewability Sensitivity]設定進行比對。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [行銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最佳化目標及使用方式](optimization-goals.md)
