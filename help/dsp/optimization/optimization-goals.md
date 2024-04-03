---
title: 最佳化目標及使用方式
description: 參考可用的最佳化目標，並瞭解何時使用這些目標。
feature: DSP Optimization
exl-id: ad684c99-7ae5-48eb-abfe-d48fd3d34cd0
source-git-commit: bc1b84dc5dafa4681942183e4d688d9d71879c8b
workflow-type: tm+mt
source-wordcount: '1754'
ht-degree: 0%

---

# 最佳化目標及使用方式

| 最佳化目標 | 說明 | 使用此目標的時機 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 透過套件層級最佳化，預算分配會以最高的點進率來排定刊登版位的優先順序。<br><br>如果達成花費目標，拍賣評估會優先處理CTR。 提交的競標一律已設定 [!UICONTROL Max Bid]，但如果刊登版位花費良好，則預測的CTR臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 如果您有不需要超越的固定CPM目標以及必須最大化的CTR目標，請使用此目標。 將「最高出價」設定為所需的CPM目標，DSP在嘗試花費完整預算的同時將達成最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 透過套件層級最佳化，預算分配會優先處理完成率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理「完成率」。 提交的競標一律為設定的「最高競標」，但如果刊登刊登花費良好，預計完成率臨界值會較嚴格。 | 行銷活動型別：品牌<br><br>基準：最高完成率<br><br>廣告型別：僅限前段<br><br><b>注意：</b> 如果您有不需要超越的固定CPM目標和必須最大化的「完成率」目標，請使用此目標。 將「最高出價」設定為所需的CPM目標，DSP在嘗試花費完整預算時，將達到可能的最佳完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 透過套件層級最佳化，預算分配會優先處理參與率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理參與率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，預計參與率臨界值就會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高參與率<br><br>廣告型別：僅限行動插入式<br><br><b>注意：</b> 如果您有固定的CPM目標不需要超越，且參與目標必須最大化，請使用此目標。 將「最高出價」設定為所需的CPM目標，DSP在嘗試花費完整預算的同時將達成最佳的參與率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe - GroupM)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律使用位置層級的「最高出價」。<br><br>如果促銷活動的可檢視度敏感度設定設為「標準（觀看連續兩秒佔廣告的50%）」，則會將媒體評等委員會(MRC)的可檢視度測量標準用於促銷活動。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊持續時間為50%）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應該將行銷活動設定與最佳化目標和競標前篩選設定做比對。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe - MRC)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律使用位置層級的「最高出價」。<br><br>如果促銷活動的可檢視度敏感度設定設為「標準（觀看連續兩秒佔廣告的50%）」，則會將媒體評等委員會(MRC)的可檢視度測量標準用於促銷活動。 如果促銷活動設為「嚴格（100%的廣告檢視與音訊持續時間為50%）」，則促銷活動會使用GroupM可檢視度測量標準。 理想情況下，您應該將行銷活動設定與最佳化目標和競標前篩選設定做比對。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS - MRC)] | 透過套件層級最佳化，預算分配會優先處理可檢視率最高的刊登版位。<br><br>如果達成花費目標，拍賣評估會優先處理可檢視率。 提交的競標一律為設定的「最高競標」，但如果刊登版位花費良好，則預測可檢視率臨界值會變得更嚴格。 | 行銷活動型別：品牌<br><br>基準：最高可檢視率<br><br>廣告型別：僅限互動式前段廣告<br><br><b>注意：</b> 此目標一律使用位置層級的「最高出價」。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最能發揮效用。 只有在您已啟用行銷活動的IAS整合時，才使用此目標。 |
| [!UICONTROL Always Max Bid and Maximize Reach] | 此目標會嘗試一律使用位置層級，透過指定曝光次數來達到最大的家庭觸及率 [!UICONTROL Max Bid]. 如果達成花費目標，DSP就會變得更具選擇性，只有在有機會取得遞增的不重複觸及時才會競標。 | 行銷活動型別：品牌<br><br>基準：觸及最大化<br><br>廣告型別：前段、顯示器、CTV、原生、音訊和通用視訊 |
| [!UICONTROL Highest Return on Ad Spend (ROAS)] | （僅適用於套件層級）預算分配會針對指定的最終轉換事件，以最高ROAS的版位為優先順序，並考慮指定自訂目標中的任何加權上層漏斗事件（例如網站造訪和購物車新增）。 您可以指定最佳化模型應該只從點按式轉換學習，還是同時從點按和曝光式轉換學習。<br><br>拍賣評估會優先處理ROAS。 如果達成支出目標，則DSP會在降低CPM與提高ROAS之間取得平衡。 | 行銷活動型別：績效<br><br>基準：最高收入<br><br>廣告型別：顯示器、原生、視訊、CTV和通用視訊<br><br><b>注意：</b> 請參閱&quot;[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)」以取得詳細資訊。 |
| [!UICONTROL Lowest Cost Per Click] | 透過套件層級最佳化，預算分配會優先處理具有最低CPC的版位。<br><br>拍賣評估會優先處理CPC。 如果達成支出目標，DSP會在降低CPM與提高CTR以降低CPC之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的點進率<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以獲得最佳的CPC。 若要保證最高的CPM，請將其用作刊登的「最高出價」。 |
| [!UICONTROL Lowest Cost Per Completion] | 透過套件層級最佳化，預算分配會以最低的每次完成成本來排定刊登版位的優先順序。<br><br>拍賣評估會優先處理視訊完成率(VCR)。 如果達成花費目標，DSP會平衡降低CPM與增加VCR，以嘗試降低每次完成的成本。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的完成率<br><br>廣告型別：僅限前段 |
| [!UICONTROL Lowest Cost Per Engagement] | 透過套件層級最佳化，預算分配會優先處理參與率最低的刊登版位。<br><br>拍賣評估會優先處理參與率。 如果達成支出目標，DSP會嘗試在降低CPM與降低每項參與的成本之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的參與率<br><br>廣告型別：僅限行動插入式 |
| [!UICONTROL Lowest Cost per Reach] | 此目標會嘗試在指定預算內實現最大的家庭觸及率。 如果達成支出目標，則競標會依實現遞增獨特觸及的機會而有所不同。 | 行銷活動型別：品牌<br><br>基準：有效率的單次觸及成本<br><br>廣告型別：前段、顯示器、CTV、原生、音訊和通用視訊 |
| [!UICONTROL Lowest Cost Per View] | 其運作方式與最低CPM類似。 透過套件層級最佳化，預算分配會優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 如果達成支出目標，DSP會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的點進率<br><br>廣告型別：前段、顯示 |
| [!UICONTROL Lowest Cost per Acquisition (CPA)] | （僅適用於套件層級）預算分配會針對指定的最終轉換事件，將CPA最低的版位優先排序，並考慮指定自訂目標中的任何加權上層漏斗事件（例如網站造訪和購物車新增）。 您可以指定最佳化模型應該只從點按式轉換學習，還是同時從點按和曝光式轉換學習。<br><br>拍賣評估會優先處理CPA。 如果達成支出目標，則DSP會在降低CPM與降低CPA之間取得平衡。 | 行銷活動型別：績效<br><br>基準：最低CPA<br><br>廣告型別：顯示器、原生、視訊、CTV和通用視訊<br><br><b>注意：</b> 請參閱&quot;[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)」以取得詳細資訊。 |
| [!UICONTROL Lowest CPM] | 透過套件層級最佳化，預算分配會優先處理CPM最低的刊登版位。<br><br>拍賣評估會優先處理CPM。 如果達成支出目標，DSP會逐步降低CPM。 | 行銷活動型別：品牌<br><br>基準：高效率CPM<br><br>廣告型別：前段、顯示器、CTV、原生、音訊 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達到花費目標，則DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作刊登的「最高出價」。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達到花費目標，則DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作刊登的「最高出價」。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達到花費目標，則DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作刊登的「最高出價」。<br><br>當來自IAS的協力廠商資料通知演演算法時，此設定最能發揮效用。 只有在您已啟用行銷活動的IAS整合時，才使用此目標。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達到花費目標，則DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作刊登的「最高出價」。<br><br>此設定最適合來自的第三方資料 [!DNL Moat] 會通知演演算法。 只有在您已啟用 [!DNL Moat] 行銷活動的整合。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 透過套件層級最佳化，預算分配會優先處理具有最低vCPM的刊登版位。<br><br>拍賣評估會優先處理vCPM。 如果達到花費目標，則DSP會嘗試在降低CPM與提高可檢視度之間取得平衡。 | 行銷活動型別：品牌<br><br>基準：高效率的CPM與最高的vCPM<br><br>廣告型別：前段、顯示<br><br><b>注意：</b> 使用此目標以達成最佳可能的vCPM。<br><br>若要保證最高的CPM，請將其用作刊登的「最高出價」。<br><br>此設定最適合來自的第三方資料 [!DNL Moat] 會通知演演算法。 只有在您已啟用 [!DNL Moat] 行銷活動的整合。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [位置層級競標前篩選器及其使用方式](optimization-pre-bid-filters.md)
>* [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
