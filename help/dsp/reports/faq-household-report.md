---
title: 關於住戶報表的常見問題集
description: 進一步瞭解住戶觸及率、頻率和轉換資料，包括住戶報告與其他報告和疑難排解的差異。
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: bd925c41f7b949c56402edd4e2dc393f0c5bed57
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# 關於住戶報表的常見問題集

## 此 [!UICONTROL Household Reach & Frequency] 報告

### 如何 [!UICONTROL Household Reach & Frequency] 報表有別於其他自訂報表？

此 [!UICONTROL Household Reach & Frequency] 報表會根據IP位址，在家庭層級測量各種維度的觸及率、曝光次數和頻率。 其他自訂報表會在裝置或Cookie層級產生。

例如，即使一個家庭中的三個裝置收到一個曝光數，不重複住戶觸及的量度仍為1。

#### 支援的Dimension

此 [!UICONTROL Household Reach & Frequency] 報告支援 [下列維度](/help/dsp/reports/report-columns.md)： &quot;[!UICONTROL Campaign]，&quot; &quot;[!UICONTROL Package]，&quot; &quot;[!UICONTROL Placement]，&quot; &quot;[!UICONTROL Site/Apps]「 （不提供重疊量度的存取權）， 」[!UICONTROL Media Type]，&quot; &quot;[!UICONTROL Feed Type]，&quot; &quot;[!UICONTROL Device]，&quot; &quot;[!UICONTROL Publisher]，&quot; &quot;[!UICONTROL Audience]，&quot; &quot;[!UICONTROL Creative Length]，」和使用者建立的位置「[!UICONTROL Tags].」 |

#### 支援的量度

此 [可用量度](/help/dsp/reports/report-columns.md) 包括：

* 重疊量度： [!UICONTROL Frequency Overlap]， [!UICONTROL Measurable Impressions (Overlap)]、和 [!UICONTROL Unique Household (Overlap)].

  重疊量度是只針對已報告的維度或維度組合發生的值，而不針對其他維度發生的值。 <!-- For example, it might show the ?? -->

* 非重疊量度： [!UICONTROL Frequency]， [!UICONTROL Incremental Household Reached]， [!UICONTROL % Incremental Household Reached]， [!UICONTROL Impressions]， [!UICONTROL Measurable Impressions]、和 [!UICONTROL Unique Household Reached]

不支援轉換量度和自訂目標。

### 重疊量度與非重疊量度之間有何差異？

下圖顯示三個行銷活動（A、B和C）的三個量度(不重複家庭觸及率、增量家庭觸及率和增量家庭（重疊）)。

![住家重疊量度的插圖](/help/dsp/assets/household-overlap-metrics-illustration.png "住家重疊量度的插圖")

* 「不重複家庭數量達到（總計）」提供每個促銷活動達到的不重複家庭數量或每個圓圈的總面積。 在圖中，A觸及的不重複家庭=觸及的增量家庭+ (A+B) + (A+C) +(A+B+C)

* Incremental Household Accessed是僅透過行銷活動觸及的不重複家庭。 在圖中，A、B、C所達的遞增家庭是分別由A、B、C所達的遞增家庭。

* Incremental Household (Overlap)是行銷活動或行銷活動組合觸及的不重複家庭。 在圖中，由A、C所觸及的增量家庭為A+C。

### 工作流程

請依照一般步驟執行 [建立自訂報表](report-create.md).

此 [!UICONTROL Household Reach & Frequency] 報表只能包含一個維度。 它也可以包括a)任何維度（網站/應用程式除外）的重疊量度，或b)非重疊量度，但不能同時包括兩者。

### 有哪些限制 [!UICONTROL Household Reach & Frequency] 報告？

具有重疊量度的報表會輸出最多三個值的交集。 例如，如果您使用量度 [!UICONTROL Unique Household (Overlap)] 若為10個位置，您會看到個別位置所達致的不重複家庭、任意兩個位置組合所達致的普通家庭，以及任意三個位置組合所達致的普通家庭。 您看不到四個或更多位置觸及的普通家庭。

對於行銷活動、套件或位置以外的維度，報表支援每個維度中最多10個值。 例如，若要產生 [!UICONTROL Unique Household Reached] 報告 [!UICONTROL Audience] 維度時，不重複受眾的數目應少於或等於10。 如果您包含超過10個不重複受眾，則會產生空白報表。

### 為什麼我的設定檔的頻率和唯一觸及值不同 [!UICONTROL Custom] 報告與 [!UICONTROL Household Reach & Frequency] 報告？

中的這些量度 [!UICONTROL Household] 報表是以IP位址的實際計數來計算，而 [!UICONTROL Custom] 報表使用模型計算的預估數字。 不過，差異應小於10%。

### 如何為設定報表 [!UICONTROL Placement Tags] 維度？

若要建立位置標籤， [開啟位置設定](/help/dsp/campaign-management/placements/placement-edit.md) 並在 [位置標籤欄位](/help/dsp/campaign-management/placements/placement-settings.md).

當位置包含多個標籤時，報表會將整個字串視為一個標籤。 報表的每個唯一字串都包含一列。

## 此 [!UICONTROL Household Conversions] 報告

### 中支援哪些歸因方法型別 [!UICONTROL Household Conversions] 報告？

支援兩種型別的歸因方法：

* [!UICONTROL Unique]：計算維度值（例如裝置或位置）在轉換路徑上的次數。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根據維度值（例如裝置或位置）在轉換路徑上的出現頻率，分配每個轉換的評分。 例如，如果在轉換前總共有10次曝光，其中8次在CTV上，2次在Mobile上，則80%的評分(0.8)會提供給CTV熒幕，而0.2次提供給Mobile。

### 在Adobe Analytics中，住戶轉換報表與CTV觀看報告有何不同？

中的CTV檢視資料 [!DNL Analytics] 已供電 [!DNL Analytics] 和住戶轉換資料會使用透過Adobe Advertising轉換追蹤收集的資料。 此外，中的DSP屬性邏輯 [!DNL Analytics] 僅使用最後一個事件，但住家轉換報表支援兩種不同的歸因方法：「不重複」和MTA。

### 我是否可以在以下兩個位置檢視CTV瀏覽資料： [!DNL Analytics for Advertising] 在自訂報表中呢？

不具此功能的廣告商 [!DNL Analytics for Advertising] 只能將「住戶轉換報表」用於住戶轉換報表。

如果貴組織擁有 [!DNL Analytics for Advertising]，一起使用這兩種型別的報表。 雖然CTV閱覽報表適用於廣泛頻道分析、網站行為等，但自訂報表可提供精細的檢視（包含依媒體型別、發佈者等劃分的資料），以指出驅動轉換率的因素。

## [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 報告與資料來源 [!DNL Advanced Measurement Services]

對於以家庭為基礎的觸及率和頻率或轉換的進階報告， [[!DNL Strategic Advertising Consulting] 團隊](/help/dsp/introduction/advanced-measurement-services.md) 可提供高度客製化的報告以及整體策略建議。 如需有關的詳細資訊 [!DNL Advanced Measurement Services]，請聯絡您的Adobe客戶團隊。

### 如果我已經在使用 [!DNL Advanced Measurement Services]，為何應使用 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 報告？

此 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 報表可讓使用者端分別即時自主提取家庭層級的觸及率、頻率和轉換量度。

### 我可以同時使用 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 報告和 [!DNL Advanced Measurement Services]？

理想的使用案例是同時使用 [!UICONTROL Household] 報告與 [!DNL Advanced Measurement Services] 報告與諮詢服務結合在一起。 考慮 [!UICONTROL Household] 以異動方式報告，旨在告知日常最佳化，以及 [!DNL Advanced Measurement Services] 更具策略性，旨在為整體學習及與總體業務目標相關的經驗提供資訊。

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)
