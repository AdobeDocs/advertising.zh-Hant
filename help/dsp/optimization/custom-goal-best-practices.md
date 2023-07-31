---
title: 建立自訂目標的最佳實務
description: 瞭解建立自訂目標以定義成功事件的最佳實務。
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 2c2f65f45fb7515068cee36493f514ce2e456e75
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 建立自訂目標的最佳實務

## 具有單一屬性的自訂目標

下列範例說明如何設定以單一轉換量度為目標的目標。

### 具有「」的行銷活動範例[!UICONTROL Highest ROAS - Custom Goal]&quot;最佳化目標

如果您的行銷活動目標是收入([!UICONTROL Highest ROAS - Custom Goal])，則您的自訂目標（目標）將包含&quot;[!UICONTROL Revenue]權重為1 (1)的&quot;量度。

![具有單一轉換量度的ROAS自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 對於所追蹤的每個$1收入，其中一個等於一個值。
>
> 例如，權重為1的$250轉換回報為$250。 如果轉換量度的權重為0.5，則$250的轉換會在Adobe Advertising中報告為$125 ($250的轉換* 0.5 [!UICONTROL Property Weight] = $125)。

### 具有「」的行銷活動範例[!UICONTROL Lowest CPA - Custom Goal]&quot;最佳化目標

如果您的行銷活動目標是每次贏取的最低成本(CPA)，並且只需要一個成功事件，則您將包含一個量度（在以下範例中，「應用程式提交」）。 最佳實務是將權重設定為一(1)。

![具有單一轉換量度的CPA自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 對於所追蹤的每次轉換，1的值等於1。
>
> 例如，如果追蹤10個「應用模組提交」轉換，則會報告10個「應用模組提交」轉換。  如果轉換量度的權重為0.5，則10次轉換會在Adobe Advertising中報告為5 (5) （10次轉換* 0.5） [!UICONTROL Property Weight] = 5)。

## 具有多個屬性的自訂目標

在兩種情況下，您會在自訂目標中使用多個屬性：

* 您的行銷活動目標有多個成功事件。 例如，您可能在廣告中要求多個網站上的動作，而所有動作都歸因於您的CPA目標。 以下範例目標包含三個不同的屬性(PDF下載、聯絡我們和電子郵件註冊)，每個屬性的權重為一(1)，用於告知 [!DNL Adobe Sensei] 每個屬性具有相同重要性的演演算法。 如果您包含具有不同成本或重要性的屬性，則可相應地調整其相對權重。

  ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自訂目標中的單一轉換量度無法達到最佳化效能所需的每天至少10次轉換。 發生此狀況的原因可能是每日封裝支出極低或自然轉換次數有限。 將其他支援屬性新增至自訂目標可協助您實現每日10次轉換的臨界值。 10個支援事件可協助套件達到10/天臨界值，即便每個事件的權重都低於一(1)。 但您不一定需要新增那麼多的事件。

  當您將支援屬性新增至自訂目標時，請根據它們對於主要成功事件的相對重要性為其加權，並牢記資料點的數量。 這可讓Adobe Sensei演演算法平衡多個屬性，並針對您的目標最佳化。

  下列範例目標包含三個屬性，每個屬性具有不同的權重：申請提交= 1、申請開始= 0.1，以及廣告商登陸頁面= 0.01。這表示每個應用程式提交轉換對您的企業而言平均有10個應用程式開始轉換和100個廣告商登陸頁面轉換，它們具有相同的價值。

  ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties2.png)

  反之，如果您將應用程式提交的登陸頁面造訪次數平均加權，則登陸頁面造訪次數自然較高，可能會壓倒您的目標並扭曲至登陸頁面造訪次數。<!--reword-->

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標](custom-goal-create.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
