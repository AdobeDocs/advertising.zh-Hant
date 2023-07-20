---
title: 最佳化目標及使用方式
description: 參考可用的最佳化目標並檢視何時使用它們。
feature: DSP Optimization
exl-id: ad684c99-7ae5-48eb-abfe-d48fd3d34cd0
source-git-commit: 2715dc78193f1f5239f0bc4689262df05c6770eb
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# 最佳化目標及使用方式

| 最佳化目標 | 說明 | 使用此目標的時機 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 透過套件層級最佳化，預算分配將優先處理點進率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理CTR。 提交的競標一律已設定 [!UICONTROL Max Bid]，但如果刊登版位花費良好，預測的CTR臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 如果您的固定CPM目標不需要超越，且CTR目標需要最大化，請使用此目標。 將最高出價設定為所需的CPM目標，DSP在嘗試花費完整預算的同時將達成最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 透過套件層級最佳化，預算分配將優先處理完成率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理「完成率」。 提交的出價一律為設定的「最高出價」，但如果刊登版位花費良好，預計完成率臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高完成率<br><br>廣告型別：僅限前段廣告<br><br><b>注意：</b> 如果您的固定CPM目標不需要超越，且完成率目標需要最大化，請使用此目標。 將最高出價設定為所需的CPM目標，DSP將在嘗試花費完整預算時實現最佳完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 透過套件層級最佳化，預算分配將優先處理參與率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理參與率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，預計參與率臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高參與率<br><br>廣告型別：僅限行動插播式廣告<br><br><b>注意：</b> 如果您的固定CPM目標不需要超越，且參與目標需要最大化，請使用此目標。 將最高出價設定為所需的CPM目標，DSP在嘗試花費完整預算的同時將達到最佳的參與率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | 透過套件層級最佳化，預算分配將優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可見率。 提交的出價一律為設定的「最高出價」，但如果刊登版位花費良好，預測的可檢視率臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可見率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律會使用位置層級的「最高出價」。<br><br>如果促銷活動的「可見度敏感度」設定設為「標準（觀看廣告50%達連續2秒鐘）」，則會對促銷活動使用媒體評等委員會(MRC)可見度測量標準。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊開啟持續50%持續時間）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應將行銷活動設定與最佳化目標和競標前篩選設定進行比對。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | 透過套件層級最佳化，預算分配將優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可見率。 提交的出價一律為設定的「最高出價」，但如果刊登版位花費良好，預測的可檢視率臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可見率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律會使用位置層級的「最高出價」。<br><br>如果促銷活動的「可見度敏感度」設定設為「標準（觀看廣告50%達連續2秒鐘）」，則會對促銷活動使用媒體評等委員會(MRC)可見度測量標準。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊開啟持續50%持續時間）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應將行銷活動設定與最佳化目標和競標前篩選設定進行比對。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | 透過套件層級最佳化，預算分配將優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可見率。 提交的出價一律為設定的「最高出價」，但如果刊登版位花費良好，預測的可檢視率臨界值將變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可見率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律會使用位置層級的「最高出價」。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最有效果。 只有在您已為行銷活動啟用IAS整合時，才使用此目標。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （僅適用於套件層級）預算配置會優先處理廣告支出回報率(ROAS)最高的刊登版位。<br><br>拍賣評估會優先處理ROAS。 如果達成支出目標，DSP將會在降低CPM與提高ROAS之間取得平衡。 | 行銷活動型別：績效<br><br>基準：最高收入<br><br>廣告型別：顯示器、原生和視訊<br><br><b>注意：</b> 請參閱「[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)」以取得詳細資訊。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （僅適用於套件層級）預算配置會優先處理具有最低CPA的刊登版位。<br><br>拍賣評估會優先考慮CPA。 如果達成支出目標，DSP將會在降低CPM與降低CPA之間取得平衡。 | 行銷活動型別：績效<br><br>基準：最低CPA<br><br>廣告型別：顯示器、原生和視訊<br><br><b>注意：</b> 請參閱「[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)」以取得詳細資訊。 |
| [!UICONTROL Lowest Cost Per Click] | 透過套件層級最佳化，預算分配將優先處理CPC最低的刊登版位。<br><br>拍賣評估會優先評估CPC。 如果達成支出目標，DSP將在降低CPM與提高CTR以降低CPC之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達到最佳的CPC。 若要保證最高的CPM，請將其用作投放位置的最高出價。 |
| [!UICONTROL Lowest Cost Per Completion] | 透過套件層級最佳化，預算分配將優先處理每次完成成本最低的刊登版位。<br><br>拍賣評估會優先處理視訊完成率(VCR)。 如果達成支出目標，DSP將會在降低CPM與增加VCR之間取得平衡，以嘗試降低每次完成的成本。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的完成率<br><br>廣告型別：僅限前段廣告 |
| [!UICONTROL Lowest Cost Per Engagement] | 透過套件層級最佳化，預算分配將優先處理參與率最低的刊登版位。<br><br>拍賣評估會優先處理參與率。 如果達成支出目標，DSP會嘗試在降低CPM與降低每次參與的成本之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的參與率<br><br>廣告型別：僅限行動插播式廣告 |
| [!UICONTROL Lowest CPM] | 透過套件層級最佳化，預算分配將優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 如果達成支出目標，DSP會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：有效率的CPM<br><br>廣告型別：前段、顯示器、CTV、原生、音訊 |
| [!UICONTROL Lowest Cost Per View] | 其運作方式與最低CPM類似。 透過套件層級最佳化，預算分配將優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 如果達成支出目標，DSP會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的點進率<br><br>廣告型別：前段、顯示 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 透過套件層級最佳化，預算分配將優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作投放位置的最高出價。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 透過套件層級最佳化，預算分配將優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作投放位置的最高出價。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 透過套件層級最佳化，預算分配將優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作投放位置的最高出價。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最有效果。 只有在您已為行銷活動啟用IAS整合時，才使用此目標。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 透過套件層級最佳化，預算分配將優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作投放位置的最高出價。<br><br>此設定最適合來自的第三方資料 [!DNL Moat] 會通知演演算法。 只有在您已啟用「 」時，才使用此目標 [!DNL Moat] 行銷活動的整合。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 透過套件層級最佳化，預算分配將優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標可達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作投放位置的最高出價。<br><br>此設定最適合來自的第三方資料 [!DNL Moat] 會通知演演算法。 只有在您已啟用「 」時，才使用此目標 [!DNL Moat] 行銷活動的整合。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [位置層級的競標前篩選條件及其使用方式](optimization-pre-bid-filters.md)
>* [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
