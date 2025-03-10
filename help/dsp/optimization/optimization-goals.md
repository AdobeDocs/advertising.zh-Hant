---
title: 最佳化目標及使用方式
description: 參考可用的最佳化目標，並瞭解何時使用這些目標。
feature: DSP Optimization
exl-id: ad684c99-7ae5-48eb-abfe-d48fd3d34cd0
source-git-commit: d9cefafe7411febe2fcc6ae57eec1d9e02266769
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 0%

---

# 最佳化目標及使用方式

| 最佳化目標 | 說明 | 使用此目標的時機 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Clickthrough Rate] | 透過套件層級最佳化，預算分配會以最高的點進率來排定刊登版位的優先順序。<br><br>拍賣評估會優先處理CTR達成支出目標的情形。 提交的競標一律為集合[!UICONTROL Max Bid]，但如果位置花費良好，則預計CTR臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標以及必須最大化的CTR目標，請使用此目標。 將「最高出價」設定為所需的CPM目標，DSP在嘗試花費完整預算的同時達成最佳的CTR。 |
| [!UICONTROL Always Max Bid & Completion Rate] | 透過套件層級最佳化，預算分配會優先處理完成率最高的刊登版位。<br><br>拍賣評估會優先處理達成花費目標的「完成率」。 提交的競標一律為設定的「最高競標」，但如果刊登刊登花費良好，預計完成率臨界值會較嚴格。 | 行銷活動型別：品牌推廣<br><br>基準：最高完成率<br><br>廣告型別：僅前置滾動<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標和必須最大化的「完成率」目標，請使用此目標。 將「最高出價」設定為所要的CPM目標，DSP在嘗試花費完整預算的同時達到最佳完成率。 |
| [!UICONTROL Always Max Bid & Engagement Rate] | 透過套件層級最佳化，預算分配會優先處理參與率最高的刊登版位。<br><br>拍賣評估會優先處理達成花費目標的參與率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，預計參與率臨界值就會變得更嚴格。 | 行銷活動型別：品牌推廣<br><br>基準：最高參與率<br><br>廣告型別：僅限行動插播式廣告<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標和必須最大化的參與目標，請使用此目標。 將「最高出價」設定為所需的CPM目標，DSP在嘗試花費完整預算的同時達到最佳參與率。 |
| [!UICONTROL Always Max Bid & Maximize Reach] | 此目標會嘗試一律使用位置層級[!UICONTROL Max Bid]，以指定曝光次數達到最大家庭觸及率。 如果達成花費目標，DSP就會變得更具選擇性，只有在有機會取得遞增的不重複觸及時才會競標。 | 行銷活動型別：品牌<br><br>基準：觸及最大範圍<br><br>廣告型別：前段、顯示、CTV、原生、音訊和通用視訊 |
| [!UICONTROL Always Max Bid & Viewability Rate (Adobe - GroupM)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>拍賣評估會優先處理達成花費目標的可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅互動式前段<br><br><b>注意：</b>此目標一律使用位置層級的「最高出價」。<br><br>如果行銷活動的「可檢視度敏感度」設定設為「標準（觀看連續2秒佔廣告的50%）」，則會將媒體評等委員會(MRC)可檢視度測量標準用於行銷活動。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊持續時間為50%）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應該將行銷活動設定與最佳化目標和競標前篩選設定做比對。 |
| [!UICONTROL Always Max Bid & Viewability Rate (Adobe - MRC)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>拍賣評估會優先處理達成花費目標的可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅互動式前段<br><br><b>注意：</b>此目標一律使用位置層級的「最高出價」。<br><br>如果行銷活動的「可檢視度敏感度」設定設為「標準（觀看連續2秒佔廣告的50%）」，則會將媒體評等委員會(MRC)可檢視度測量標準用於行銷活動。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊持續時間為50%）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應該將行銷活動設定與最佳化目標和競標前篩選設定做比對。 |
| [!UICONTROL Always Max Bid & Viewability Rate (IAS - MRC)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>拍賣評估會優先處理達成花費目標的可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅互動式前段<br><br><b>注意：</b>此目標一律使用位置層級的「最高出價」。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最有效。 只有在您已啟用行銷活動的IAS整合時，才使用此目標。 |
| [!UICONTROL Highest Return on Ad Spend (ROAS)] | （僅適用於套件層級）預算分配會針對指定自訂目標中包含的最終轉換事件，以最高ROAS的版位為優先順序，並考慮自訂目標中的所有其他加權上層漏斗事件（例如網站造訪和購物車新增）。 您可以指定最佳化模型應該只從點按式轉換學習，還是同時從點按和曝光式轉換學習。<br><br>拍賣評估會優先處理ROAS。 達成支出目標，DSP則在降低CPM與提高ROAS之間取得平衡。 | 行銷活動型別：效能<br><br>基準：最高收入<br><br>廣告型別：顯示器、原生、視訊、CTV和通用視訊<br><br><b>注意：</b>如需詳細資訊，請參閱「[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)」。 |
| [!UICONTROL Lowest Cost per Acquisition (CPA)] | （僅適用於套件層級）預算分配會針對指定自訂目標中包含的最終轉換事件，以最低CPA的版位為優先順序，並考慮自訂目標中的所有其他加權上層漏斗事件（例如網站造訪和購物車新增）。 您可以指定最佳化模型應該只從點按式轉換學習，還是同時從點按和曝光式轉換學習。<br><br>拍賣評估會優先處理CPA。 達成支出目標，DSP則在降低CPM與降低CPA之間取得平衡。 | 行銷活動型別：效能<br><br>基準：最低的CPA<br><br>廣告型別：顯示器、原生、視訊、CTV和通用視訊<br><br><b>注意：</b>如需詳細資訊，請參閱[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)。 |
| [!UICONTROL Lowest Cost per Click] | 透過套件層級最佳化，預算分配會優先處理具有最低CPC的版位。<br><br>拍賣評估會優先處理CPC。 達成支出目標，然後DSP在降低CPM與提高CTR以降低CPC之間取得平衡。 | 行銷活動型別：品牌推廣<br><br>基準：有效的CPM與最高的點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b>使用此目標可達成最佳的CPC。 若要保證CPM的最高出價，請將其用作此位置的最高出價。 |
| [!UICONTROL Lowest Cost per Completion] | 透過套件層級最佳化，預算分配會以最低的每次完成成本來排定刊登版位的優先順序。<br><br>拍賣評估會優先處理視訊完成率(VCR)。 達成支出目標，DSP便會在降低CPM與增加VCR之間取得平衡，藉此降低每次完成的成本。 | 行銷活動型別：品牌<br><br>基準：有效的CPM與最高的完成率<br><br>廣告型別：僅限前段廣告 |
| [!UICONTROL Lowest Cost per Engagement] | 透過套件層級最佳化，預算分配會優先處理參與率最低的刊登版位。<br><br>拍賣評估會優先處理參與率。 達成支出目標，DSP便會嘗試在降低CPM與降低每項參與的成本之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：有效的CPM與最高的參與率<br><br>廣告型別：僅限行動插播式廣告 |
| [!UICONTROL Lowest Cost per Reach] | 此目標會嘗試在指定預算內實現最大的家庭觸及率。 如果達成支出目標，則競標會依實現遞增獨特觸及的機會而有所不同。 | 行銷活動型別：品牌<br><br>基準：每個觸及的有效成本<br><br>廣告型別：前段、顯示器、CTV、原生、音訊和通用視訊 |
| [!UICONTROL Lowest Cost per View] | 運作方式與最低CPM類似。 透過套件層級最佳化，預算分配會優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 達成支出目標，DSP就會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：有效的CPM與最高的點進率<br><br>廣告型別：前段、顯示 |
| [!UICONTROL Lowest CPM] | 透過套件層級最佳化，預算分配會優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 達成支出目標，DSP就會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：有效的CPM<br><br>廣告型別：前段、顯示、CTV、原生、音訊 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：有效的CPM和最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b>使用此目標可達成最佳的vCPM。<br><br>若要保證CPM的最高出價，請將其用作此位置的最高出價。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：有效的CPM和最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b>使用此目標可達成最佳的vCPM。<br><br>若要保證CPM的最高出價，請將其用作此位置的最高出價。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 達成支出目標，DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：有效的CPM和最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b>使用此目標可達成最佳的vCPM。<br><br>若要保證CPM的最高出價，請將其用作此位置的最高出價。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最有效。 只有在您已啟用行銷活動的IAS整合時，才使用此目標。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [位置層級競標前篩選及使用方式](optimization-pre-bid-filters.md)
>* [行銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
