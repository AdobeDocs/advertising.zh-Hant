---
title: 自訂報表常見問題集
description: 進一步瞭解自訂報告，包括家庭報告和轉換路徑分析報告。
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# 自訂報表常見問題集

## 家庭報表

### [!UICONTROL Household Reach & Frequency]報告

#### [!UICONTROL Household Reach & Frequency]報告與其他自訂報告有何不同？

[!UICONTROL Household Reach & Frequency]報告會根據IP位址，在家庭層級測量各種維度的觸及率、曝光次數和頻率。 其他自訂報表會在裝置或Cookie層級產生。

例如，即使一個家庭中的三個裝置收到一個曝光數，不重複家庭觸及的量度仍為一。

##### 支援的維度

[!UICONTROL Household Reach & Frequency]報告支援[下列維度](/help/dsp/reports/report-columns.md)：「[!UICONTROL Campaign]」、「[!UICONTROL Package]」、「[!UICONTROL Placement]」、「[!UICONTROL Site/Apps]」（不提供對重疊量度的存取權）、「[!UICONTROL Media Type]」、「[!UICONTROL Feed Type]」、「[!UICONTROL Device]」、「[!UICONTROL Publisher]」、「[!UICONTROL Audience]」、「[!UICONTROL Creative Length]」以及使用者建立的位置「[!UICONTROL Tags]」。 |

##### 支援的量度

[可用的量度](/help/dsp/reports/report-columns.md)包括：

* 重疊量度： [!UICONTROL Frequency Overlap]、[!UICONTROL Measurable Impressions (Overlap)]和[!UICONTROL Unique Household (Overlap)]。

  重疊量度是只針對已報告維度或維度組合發生的值，不會針對其他維度發生。<!-- For example, it might show the ?? -->

* 非重疊量度： [!UICONTROL Frequency]、[!UICONTROL Incremental Household Reached]、[!UICONTROL % Incremental Household Reached]、[!UICONTROL Impressions]、[!UICONTROL Measurable Impressions]和[!UICONTROL Unique Household Reached]

不支援轉換量度和自訂目標。

#### 重疊和非重疊量度之間有何差異？

下圖顯示三個行銷活動（A、B和C）的三個量度（不重複家庭觸及率、累加家庭觸及率和累加家庭觸及率）。

![家庭重疊量度圖例](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重疊量度圖例")

* 「不重複家庭（總計）」提供每個促銷活動觸及的「不重複家庭」，或每個圓圈的總面積。 在圖中，A觸及的不重複家庭=觸及的遞增家庭A + (A+B) + (A+C) +(A+B+C)

* Incremental Household Acceeded是僅透過促銷活動觸及的不重複家庭。 在圖中，A、B、C所達的增量家庭是分別由A、B、C所達的增量家庭。

* Incremental Household (Overlap)是行銷活動或行銷活動組合所觸及的不重複家庭。 在圖中，由A、C所觸及的遞增家庭為A+C。

#### 工作流程

依照一般步驟[建立自訂報表](report-create.md)。

[!UICONTROL Household Reach & Frequency]報表只能包含一個維度。 它也可以包含a)任何維度（網站/應用程式除外）的重疊量度，或b)非重疊量度，但不能同時包含兩者。

#### [!UICONTROL Household Reach & Frequency]報告有哪些限制？

重疊量度的報表會輸出最多三個值的交集。 例如，若您使用量度[!UICONTROL Unique Household (Overlap)]檢視10個刊登版位，則您可看到個別刊登版位所觸及的唯一家庭、任意兩個刊登版位組合所觸及的共同家庭，以及任意三個刊登版位組合所觸及的共同家庭。 您無法看到四個或更多位置觸及的普通家庭。

對於行銷活動、套件或位置以外的維度，報表支援每個維度中最多10個值。 例如，若要產生[!UICONTROL Unique Household Reached]維度的[!UICONTROL Audience]報表，唯一受眾的數目應少於或等於10。 如果您包含超過10個不重複受眾，則會產生空白報表。

#### 為什麼我的[!UICONTROL Custom]報告與[!UICONTROL Household Reach & Frequency]報告之間的頻率和唯一觸及值不同？

[!UICONTROL Household]報表中的這些量度是使用IP位址的實際計數來計算，而[!UICONTROL Custom]報表中的量度則是使用模型計算的預估數字。 不過，差異應小於10%。

#### 如何設定[!UICONTROL Placement Tags]維度的報表？

若要建立位置標籤，請[開啟位置設定](/help/dsp/campaign-management/placements/placement-edit.md)，並在[位置標籤欄位](/help/dsp/campaign-management/placements/placement-settings.md)中輸入值。

當位置包含多個標籤時，報表會將整個字串視為一個標籤。 報表的每個唯一字串都包含一列。

### [!UICONTROL Household Conversions]報告

#### [!UICONTROL Household Conversions]報表支援哪些歸因方法？

支援兩種型別的歸因方法：

* [!UICONTROL Unique]：計算維度值（例如裝置或位置）在轉換路徑上的次數。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根據維度值（例如裝置或位置）在轉換路徑上的發生頻率，分配每個轉換的評分。 例如，如果在轉換前共有10次曝光，其中8次在CTV上，2次在行動裝置上，則80%的評分(0.8)會給予予CTV熒幕，而0.2次給予行動裝置。

#### 在Adobe Analytics中，住戶轉換報表與CTV觀看報告有何不同？

* 在[!DNL Analytics]中，[!DNL CTV View-Through Conversion]報告會顯示轉換前CTV曝光為最後接觸點的轉換次數。 相較之下，DSP [!UICONTROL Household Conversions]報表則顯示轉換前，在定義的回顧期間內，任何時間點接觸到CTV曝光的不重複家庭數量。

* 在[!DNL Analytics]中，歸因邏輯會專門將轉換指派給Adobe Advertising的最後一個接觸點。 相反地，DSP [!UICONTROL Household Conversions]報表支援其他歸因模型&#x200B;*[!UICONTROL Unique]*&#x200B;和&#x200B;*[!UICONTROL Multi-Touch Attribution (MTA)]*。

* [!DNL Analytics]報告資料對於依行銷管道、網站參與量度等進行分析，特別有用。 DSP [!UICONTROL Household Conversions]報表可允許轉換資料依各種維度（例如媒體型別和發佈者）分割，以提供更精細的深入分析。

### [!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]報告與來自[!DNL Advanced Measurement Services]的資料

針對以住戶為基礎的觸及率和頻率或轉換的進階報告，[[!DNL Strategic Advertising Consulting] 團隊](/help/dsp/introduction/advanced-measurement-services.md)可提供高度可自訂的報告以及整體策略建議。 如需[!DNL Advanced Measurement Services]的詳細資訊，請連絡您的Adobe客戶團隊。

#### 如果我已經使用[!DNL Advanced Measurement Services]，為什麼要使用[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]報告？

[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]報告可讓使用者端分別即時自主提取家庭層級的觸及率、頻率和轉換量度。

#### 我可以同時使用[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]報告和[!DNL Advanced Measurement Services]嗎？

理想的使用案例是同時使用[!UICONTROL Household]報告和[!DNL Advanced Measurement Services]報告和諮詢服務。 將[!UICONTROL Household]報表視為異動，旨在告知日常最佳化，將[!DNL Advanced Measurement Services]視為更具策略性，旨在告知整體學習和與總體業務目標相連結的學習者。

## 轉換路徑分析報表

### 轉換路徑報表與[!DNL Advanced Measurement Services]和Adobe Analytics Analysis Workspace建立的報表有何不同？

| | 轉換報表的路徑 | Advanced Measurement Services對搜尋報表的光暈效果 | Analysis Workspace中的報表 |
| --- | --- | --- |---|
| 客戶價值 | 產生自助式自訂報表，瞭解廣告歷程的哪些路徑導致更多轉換，以提升最佳化 | 瞭解連線電視(CTV)策略對搜尋點選數的影響 | 瞭解整體Adobe Advertising投資以及其他行銷管道對搜尋點選的影響 |
| 家庭層級 | 是 | 是 | 否 |
| 是否支援CTV？ | 是 | 是 | 是 |
| 歸因方法 | 上次接觸事件（曝光數或點按數）必須在回顧期間內。 | 不重複 | 上次接觸 |
| | 系統會針對轉換路徑考量上次接觸事件前30天以上的互動點。 | （CTV會獲得點數，無論使用者的點按路徑中會出現CTV曝光） | （如果曝光是回顧期間的最後一個事件，且在曝光之前或之後沒有其他格式的付費點按，CTV就會獲得點數） |
| 報告層級 | 粒度 | 粒度 | 廣泛 |
| | (頻道型別、Creative/廣告、關鍵字、路徑、長度、轉換時間) | （CTV策略， CTV應用程式/發佈者） | (Adobe Advertising和其他行銷管道) |
| 行銷管道 | DSP +搜尋(從搜尋、社交和Commerce) | DSP +搜尋(從搜尋、社交和Commerce) | Adobe Advertising點進次數EF ID未追蹤的行銷管道（例如有機搜尋、有機社交、電子郵件和附屬機構） |
| 支援的轉換量度 | 使用Adobe Advertising事件畫素(AMO ID)和Adobe Analytics追蹤功能進行追蹤的量度 | 點按次數（無轉換） | 使用Adobe Analytics追蹤功能追蹤的量度 |

如需有關進階測量服務光暈對搜尋報表影響的詳細資訊，請參閱[進階測量服務](/help/dsp/introduction/advanced-measurement-services.md)。

>[!MORELIKETHIS]
>
>* [關於自訂報告](/help/dsp/reports/report-about.md)
>* [建立自訂報告](/help/dsp/reports/report-create.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [自訂報告設定](/help/dsp/reports/report-settings.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)
