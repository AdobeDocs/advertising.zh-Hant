---
title: 常見問題集 [!UICONTROL Household] 報表
description: 深入了解 [!UICONTROL Household] 報告，包括其他報告和疑難排解的不同之處。
source-git-commit: d88ea4ab2ad4a2ee54475346a24724b766b024fc
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# 常見問題集 [!UICONTROL Household] 報表

## 如何 [!UICONTROL Household] 觸及和頻率報告與其他自訂報告不同？

此 [!UICONTROL Household] 報表會根據IP位址，測量家庭層級各維度的觸及率、曝光次數和頻率。 其他自訂報表則在裝置或Cookie層級產生。

例如，即使對一個家庭內的三部裝置提供一次曝光數，「達到不重複家庭次數」量度仍為一次。

### 支援的Dimension

此 [!UICONTROL Household] 報表支援 [下列維度](/help/dsp/reports/report-columns.md):&quot;[!UICONTROL Campaign], &quot;[!UICONTROL Package], &quot;[!UICONTROL Placement], &quot;[!UICONTROL Site/Apps]&quot;（不提供重疊量度的存取權）, &quot;[!UICONTROL Media Type], &quot;[!UICONTROL Feed Type], &quot;[!UICONTROL Device], &quot;[!UICONTROL Publisher], &quot;[!UICONTROL Audience], &quot;[!UICONTROL Creative Length]，和使用者建立的版位&quot;[!UICONTROL Tags].&quot; |

### 支援的量度

此 [可用量度](/help/dsp/reports/report-columns.md) 包括：

* 重疊量度： [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]，和 [!UICONTROL Unique Household (Overlap)].

   重疊量度是僅針對報表的維度或維度組合而發生的值，不針對其他維度。 <!-- For example, it might show the ?? -->

* 非重疊量度： [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]，和 [!UICONTROL Unique Household Reached]

不支援轉換量度和自訂目標。

## 重疊和非重疊量度之間有何差異？

下圖顯示三個促銷活動（A、B和C）的三個度量(獨特家庭、增量家庭和增量家庭（重疊）)。

![家庭重疊量度插圖](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重疊量度插圖")

* 「達到的不重複家庭數」（總計）提供每個促銷活動觸及的不重複家庭數，或每個社交圈的總面積。 在圖中，A所達到的獨特家庭= A +(A+C)+(A+B)+(A+B+C)所達到的增量家庭

* Incremental Houdel Receard是僅通過促銷活動觸及的獨特家庭。 在該數字中，A、B、C的增量家庭分別為A、B、C的增量家庭。

* Incremental Houdey(Overlap)是促銷活動或促銷活動組合觸及的「不重複家庭」。 在圖中，A、C所達到的增量家庭是A+C。

## 工作流程

請依照 [建立自訂報表](report-create.md).

此 [!UICONTROL Household] 報表僅可包含一個維度。 也可以包含a)除網站/應用程式外，任何維度的重疊量度，或b)非重疊量度，但不能同時包含兩者。

## 有哪些限制 [!UICONTROL Household] 報告？ 

含有重疊量度的報表會輸出最多三個值的交集。 例如，如果您使用量度 [!UICONTROL Unique Household (Overlap)] 對於10個刊登版位，您可以看到個別刊登版位觸及的不重複家庭、任何兩個刊登版位結合觸及的普通家庭，以及任何三個刊登版位結合觸及的普通家庭。 你看不到普通家庭被四個或更多位置覆蓋。

對於促銷活動、套件或版位以外的維度，報表支援每個維度最多10個值。 例如，若要產生 [!UICONTROL Unique Household Reached] 報表 [!UICONTROL Audience] 維度中，不重複對象的數量應小於或等於10。 如果您包含超過10個不重複對象，則會產生空白報表。

## 為何頻率和不重複觸及值在我的 [!UICONTROL Custom] 報表與 [!UICONTROL Household] 報告？

以下量度： [!UICONTROL Household] 報表是使用IP位址的實際計數來計算，而 [!UICONTROL Custom] 報告使用使用模型計算的估計數。 但差異應小於10%。

## 如何為 [!UICONTROL Placement Tags] 維度？

若要建立版位的標籤， [開啟版位設定](/help/dsp/campaign-management/placements/placement-edit.md) 並在 [版位標籤欄位](/help/dsp/campaign-management/placements/placement-settings.md).
 
當版位包含多個標籤時，報表會將整個字串視為一個標籤。 報表會為每個唯一字串包含一列。

## [!UICONTROL Household] 報表與資料的比較 [!DNL Advanced Measurement Services]

若要進階報告以家庭為基礎的觸及和頻率， [[!DNL Strategic Advertising Consulting] 團隊](/help/dsp/introduction/advanced-measurement-services.md) 可提供高度可自訂的報表，以及全方位的策略建議。 如需 [!DNL Advanced Measurement Services]，請連絡您的Adobe帳戶團隊。

### 如果我已使用 [!DNL Advanced Measurement Services]，為何應使用 [!UICONTROL Household] 報告？

此 [!UICONTROL Household] 報告使客戶能夠自動即時提取家庭層級的觸及率和頻率量度。

### 我可以同時使用 [!UICONTROL Household] 報表和 [!DNL Advanced Measurement Services]? 

理想的使用案例是同時使用 [!UICONTROL Household] 報表和 [!DNL Advanced Measurement Services] 報告與諮詢服務。 考慮 [!UICONTROL Household] 以交易方式報告，意在提供日常最佳化，以及 [!DNL Advanced Measurement Services] 更具戰略性，旨在提供與整體業務目標掛鈎的整體學習和總結。

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [編輯自訂報表](/help/dsp/reports/report-edit.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [可用報表欄](/help/dsp/reports/report-columns.md)

