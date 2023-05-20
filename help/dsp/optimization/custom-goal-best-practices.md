---
title: 構建自定義目標的最佳做法
description: 瞭解構建自定義目標以定義成功事件的最佳實踐。
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 構建自定義目標的最佳做法

## 具有單個屬性的自定義目標

以下示例說明如何配置針對單個屬性（度量）的目標。

### 具有「」的市場活動示例[!UICONTROL Highest ROAS - Custom Goal]&quot;優化目標

如果您的促銷目標是收入([!UICONTROL Highest ROAS - Custom Goal])，則您的自定義目標（目標）將包括「[!UICONTROL Revenue]&quot;權重為一(1)的屬性。

![具有單個屬性的ROAS自定義目標示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 1等於跟蹤的每1美元收入的1值。
>
> 例如，一個250美元的轉換，其重量為1，報告為250美元。 如果為轉換度量分配了0.5的權重，則在「Adobe廣告」（$250轉換* 0.5）中，$250的轉換報告為$125 [!UICONTROL Property Weight] = 125美元)。

### 具有「」的市場活動示例[!UICONTROL Lowest CPA - Custom Goal]&quot;優化目標

如果您的市場活動目標是每次收購(CPA)的最低成本，並且它只需要一個成功事件，則您將包括該指標（在下例的「申請提交」中）。 最佳做法是將重量設為一(1)。

![具有單個屬性的CPA自定義目標示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 等於跟蹤的每個轉換的值1。
>
> 例如，如果跟蹤10個「申請提交」轉換，則會報告10個「申請提交」轉換。  如果將轉換度量的權重指定為0.5，則在Adobe廣告（10個轉換* 0.5）中，10個轉換將報告為5個(5) [!UICONTROL Property Weight] = 5)。

## 具有多個屬性的自定義目標

在以下兩種情形中，您將在自定義目標中使用多個屬性：

* 您的活動目標有多個成功事件。 例如，您可能在為多個現場活動做廣告，而所有這些都歸因於您的CPA目標。 以下示例目標包括三個獨立的屬性(PDF下載、聯繫我們和電子郵件註冊)，每個屬性的權重為一(1)，它告訴 [!DNL Adobe Sensei] 每個屬性具有同等重要性的算法。 如果您包括具有不同成本或重要性的屬性，則可以相應地調整其相對權重。

   ![具有多個屬性的自定義目標示例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自定義目標中的單個屬性不能實現優化效能所需的每天最少10次轉換。 這可能是因為每日包裹花費最少或自然轉換次數有限。 向自定義目標中添加其他支援屬性有助於您達到每天10次轉換的閾值。 10個支援事件可幫助一個包達到10/天閾值，即使每個重量低於一(1)。 但是，你可能不需要再增加這麼多事件。

   將支援屬性添加到自定義目標時，根據它們對主要成功事件的相對重要性對它們進行加權，並記住資料點的數量。 這使Adobe Sensei算法能夠平衡多個屬性並針對您的目標進行優化。

   以下示例目標包括三個屬性，每個屬性具有不同的權重：申請提交= 1，申請開始= 0.1，廣告商登錄頁= 0.01。這意味著每個「申請提交」轉換對您的業務的價值與平均10個「申請開始」轉換和100個廣告商登錄頁轉換的價值相同。

   ![具有多個屬性的自定義目標示例](/help/dsp/assets/custom-goal-multiple-properties2.png)

   相反，如果您對登錄頁訪問的權重與應用程式提交的權重相等，則登錄頁訪問數量自然會更高，這可能會壓倒您的目標，並偏向登錄頁訪問。<!--reword-->

>[!MORELIKETHIS]
>
>* [關於自定義目標](custom-goal-about.md)
>* [建立自定義目標](custom-goal-create.md)
>* [優化目標及其使用方法](optimization-goals.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [如何優DSP化您的市場活動](optimization-how-dsp-optimizes-campaigns.md)

