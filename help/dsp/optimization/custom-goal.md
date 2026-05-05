---
title: 自訂目標的最佳實務
description: 瞭解為針對最低CPA或最高ROAS而最佳化的套件定義自訂目標的最佳實務。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# 自訂目標的最佳實務

自訂目標定義廣告商實現其業務目標所需的成功事件。 每個使用最佳化目標&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;的套件都必須包含自訂目標，以協助達成整體最佳化目標。 您可以建立自訂目標作為&#x200B;*[自訂目標](/help/dsp/admin/custom-objectives-manage.md)*。

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每個自訂目標（目標）包含要追蹤和最佳化的一或多個轉換量度，以及這些量度的相對權重。 您可以[將自訂目標](/help/dsp/campaign-management/packages/package-settings.md)指派給套件，以使用[!DNL Adobe AI]進行報告和演演算法最佳化。

若要建立和管理自訂目標，請參閱[管理自訂目標](/help/dsp/admin/custom-objectives-manage.md)。

## 使用單一量度的自訂目標

下列範例說明如何設定以單一轉換量度為目標的目標。

### 具有&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;最佳化目標的行銷活動範例

如果您的行銷活動目標是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，且來自所有裝置型別的收入對您而言同樣重要，則請加入權重為1 (1)的&quot;[!UICONTROL Revenue]&quot;量度。 選取量度型別&#x200B;*[!UICONTROL Goal]*。

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 針對任何裝置上的顯示廣告所追蹤的每個$1收入，一(1)的權重等於一(1)的值。 例如，權重為1 (1)的$250轉換會回報為$250的轉換。 如果轉換量度的權重為0.5，則$250轉換在Adobe Advertising中會報告為$125 （$250轉換* 0.5 [!UICONTROL weight] = $125）。

### 具有&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;最佳化目標的行銷活動範例

如果您的行銷活動目標是每次贏取的最低成本(CPA)，並且只需要一個成功事件（例如「應用程式提交」），則請包含該量度，並將量度型別指定為&#x200B;*[!UICONTROL Goal]*。 最佳實務是將權重設定為一(1)。

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 針對任何裝置上的顯示廣告所追蹤的每次轉換，一(1)的權重等於一(1)的值。 例如，如果追蹤10個「應用模組提交」轉換，則會報告10個「應用模組提交」轉換。 但是，如果轉換量度的權重為0.5，則10次轉換在Adobe Advertising中會報告為5 (5) （10次轉換* 0.5 [!UICONTROL weight] = 5）。

## 具有多個量度的自訂目標

在兩種情況下，您會在自訂目標中使用多個量度：

* 您的行銷活動目標有多個成功事件。 例如，您可能會針對多個網站上的動作（PDF下載、聯絡我們及電子郵件註冊）進行廣告，這些動作都會對您的CPA目標有所貢獻。 如果目標包含三個個別的量度，每個量度的權重為一(1)，則[!DNL Adobe AI]支援的演演算法會將每個量度和使用者裝置型別視為同等重要性。 如果不同量度的成本或重要性不同，請相應地調整其相對權重。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自訂目標中的單一轉換量度無法達到最佳化效能所需的每天至少10次轉換。 由於每日封裝支出最小或自然轉換次數有限，因此轉換次數可能會較低。 將其他支援量度新增至自訂目標可協助您實現每天10次轉換的臨界值。 10個支援事件可協助套件達到10/天臨界值，即便每個事件的權重都低於一(1)。 但您不一定需要新增那麼多的事件。

  當您將支援量度新增至自訂目標時，請根據支援量度對主要成功事件的相對重要性為其加權，並牢記資料點的數量。 這可讓[!DNL Adobe AI]支援的演演算法平衡多個量度，並針對您的目標最佳化。

  下列範例目標包含三個量度，每個量度具有不同的權重：應用程式提交= 1、應用程式開始= 0.1，以及廣告商登陸頁面= 0.01。 這表示每個應用程式提交轉換對您的企業而言平均有10個應用程式開始轉換和100個廣告商登陸頁面轉換，它們具有相同的價值。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

反之，如果您將應用程式提交的登陸頁面造訪次數平均加權，則原本較高的登陸頁面造訪次數可能會壓倒您的目標，並使最佳化傾向登陸頁面造訪次數。

>[!MORELIKETHIS]
>
>* [管理自訂目標](/help/dsp/admin/custom-objectives-manage.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
