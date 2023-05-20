---
title: 關於 [!UICONTROL Household] 報告
description: 瞭解有關 [!UICONTROL Household] 報告，包括報告與其他報告和故障排除的不同之處。
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# 關於 [!UICONTROL Household] 報告

## 如何 [!UICONTROL Household] 訪問和頻率報告與其他自定義報告不同？

的 [!UICONTROL Household] 根據IP地址，在家庭級別跨不同維度報告測量範圍、印象和頻率。 其他自定義報告在設備或cookie級別生成。

例如，即使一個家庭的三台設備都能得到一個印象，「唯一家庭到達」指標也只有一個。

### 支援的Dimension

的 [!UICONTROL Household] 報告支援 [以下維](/help/dsp/reports/report-columns.md):&quot;[!UICONTROL Campaign], &quot;[!UICONTROL Package], &quot;[!UICONTROL Placement], &quot;[!UICONTROL Site/Apps]&quot;（不提供對重疊度量的訪問）, &quot;[!UICONTROL Media Type], &quot;[!UICONTROL Feed Type], &quot;[!UICONTROL Device], &quot;[!UICONTROL Publisher], &quot;[!UICONTROL Audience], &quot;[!UICONTROL Creative Length]，和用戶建立的位置&quot;[!UICONTROL Tags]&quot; |

### 支援的度量

的 [可用度量](/help/dsp/reports/report-columns.md) 包括：

* 重疊度量： [!UICONTROL Frequency Overlap]。 [!UICONTROL Measurable Impressions (Overlap)], [!UICONTROL Unique Household (Overlap)]。

   重疊度量是僅針對所報告的維或維組合而不針對其他維發生的值。 <!-- For example, it might show the ?? -->

* 非重疊度量： [!UICONTROL Frequency]。 [!UICONTROL Incremental Household Reached]。 [!UICONTROL % Incremental Household Reached]。 [!UICONTROL Impressions]。 [!UICONTROL Measurable Impressions], [!UICONTROL Unique Household Reached]

不支援轉換度量和自定義目標。

## 重疊度量與非重疊度量之間有何區別？

下圖顯示了三個活動（A、B和C）的三個指標（達到唯一家庭、達到增量家庭和重疊）。

![家庭重疊度量的圖示](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重疊度量的圖示")

* Unique House Acceinted(Total)提供每個活動或每個圈子的總面積所達到的Unique House。 在圖中，A所達到的獨特家庭=A +(A+B)+(A+C)+(A+B+C)所達到的增量家庭

* Incremental Housder Accemented是僅通過活動達到的獨特家庭。 在圖中，A、B、C的增量家庭分別是A、B、C的增量家庭。

* Incremental House(Overlap)是活動或活動組合所達到的「唯一家庭」。 在圖中，A、C的增量家庭是A+C。

## 工作流程

按照常規步驟 [建立自定義報表](report-create.md)。

的 [!UICONTROL Household] 報表只能包含一個維。 它還可以包括a)除站點/應用程式外的任何維的重疊度量或b)非重疊度量，但不能同時包括兩者。

## 這些 [!UICONTROL Household] 報告？ 

具有重疊度量的報表輸出交叉點（最多三個值）。 例如，如果使用度量 [!UICONTROL Unique Household (Overlap)] 對於10個安置點，你可以看到個人安置所達到的獨特家庭，任何兩個安置所達到的普通家庭，以及任何三個安置所達到的普通家庭。 看不到一般家庭四個或四個以上的安置。

對於市場活動、包或放置以外的維，報表在每個維中最多支援10個值。 例如，要生成 [!UICONTROL Unique Household Reached] 報告 [!UICONTROL Audience] 維，唯一訪問群體的數量應小於或等於10。 如果您包括10個以上的唯一受眾，則會生成一個空白報告。

## 為什麼頻率和唯一的到達值不同於 [!UICONTROL Custom] 報告和 [!UICONTROL Household] 報告？

中的這些指標 [!UICONTROL Household] 報告使用IP地址的實際計數計算，而 [!UICONTROL Custom] 報告使用使用模型計算的估計數。 但差距應小於10%。

## 如何為 [!UICONTROL Placement Tags] 維度？

要為放置建立標籤， [開啟放置設定](/help/dsp/campaign-management/placements/placement-edit.md) 在 [「放置標籤」欄位](/help/dsp/campaign-management/placements/placement-settings.md)。
 
當放置包含多個標籤時，報告會將整個字串視為一個標籤。 報告為每個唯一字串包括一行。

## [!UICONTROL Household] 報告與資料 [!DNL Advanced Measurement Services]

關於基於家庭的覆蓋範圍和頻率的高級報告， [[!DNL Strategic Advertising Consulting] 團隊](/help/dsp/introduction/advanced-measurement-services.md) 可提供高度可定製的報告以及全面的戰略建議。 有關 [!DNL Advanced Measurement Services]，聯繫您的Adobe帳戶團隊。

### 如果我已經在 [!DNL Advanced Measurement Services]，我為什麼要 [!UICONTROL Household] 報告？

的 [!UICONTROL Household] 報告使客戶能夠即時自主地拉動家庭層面的影響和頻率指標。

### 我能同時使用 [!UICONTROL Household] 報告和 [!DNL Advanced Measurement Services]? 

理想的使用情形是 [!UICONTROL Household] 報告和 [!DNL Advanced Measurement Services] 及諮詢服務。 考慮 [!UICONTROL Household] 報告為事務性，用於通知日常優化， [!DNL Advanced Measurement Services] 更具戰略性，旨在為與總體業務目標相關的全面學習和總結提供資訊。

>[!MORELIKETHIS]
>
>* [關於自定義報告](/help/dsp/reports/report-about.md)
>* [建立自定義報告](/help/dsp/reports/report-create.md)
>* [編輯自定義報告](/help/dsp/reports/report-edit.md)
>* [自定義報表設定](/help/dsp/reports/report-settings.md)
>* [可用報表列](/help/dsp/reports/report-columns.md)

