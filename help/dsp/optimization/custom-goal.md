---
title: 自訂目標
description: 瞭解自訂目標，以在針對最低CPA或最高ROAS而最佳化的套件中定義成功事件。
feature: DSP Optimization
source-git-commit: 6dba85185789c365bd72787eb0fa16ef90bf6b9e
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# 自訂目標

自訂目標定義廣告商實現其業務目標所需的成功事件。 每個使用最佳化目標的套件»[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]「必須包含有助於實現整體最佳化目標的自訂目標。 您可以建立自訂目標為 *目標* 在 [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每個自訂目標包含一或多個轉換量度，以及這些量度的相對權重。 可用的轉換量度包含使用Adobe Advertising轉換畫素並透過Adobe Analytics追蹤的所有量度。

例如，假設三個轉換量度與您的其中一個行銷活動中的特定套件相關：價值20美元的「PDF下載」、價值30美元的「電子郵件註冊」和價值40美元的「訂單確認」。 如果您想要根據客戶動作的一次性貨幣值給予權重，則量度的相對權重為1、1.5和2。

一旦您 [建立自訂目標](#custom-goal-create)，您可以 [將其指派給封裝](/help/dsp/campaign-management/packages/package-settings.md) 使用Adobe Sensei進行報告和演演算法最佳化。

## 建立自訂目標 {#custom-goal-create}

若要建立自訂目標，DSP帳戶必須連結至 [!DNL Search, Social, & Commerce] 在中使用相同Adobe Experience Cloud組織ID的帳戶 [!DNL Search, Social, & Commerce] 使用者端設定。 如果您的DSP帳戶未連結至 [!DNL Search, Social, & Commerce] 帳戶，然後聯絡您的Adobe帳戶團隊。

1. 登入 [!DNL Advertising Search, Social, & Commerce] at （北美使用者） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他使用者） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. 確認已追蹤您要在目標中納入的量度、可在產品中使用，且包含顯示名稱：

   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. 找到量度，並確定 **[!UICONTROL Show in UI and Reports]** 已針對量度啟用。

      >[!NOTE]
      >
      >* [!DNL Analytics] 自訂事件會遵循以下命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 範例： `custom_event_16_examplersid`

   1. 如果量度中沒有值 **[!UICONTROL Display Name]** 欄，然後按一下儲存格，輸入顯示名稱，然後按一下 **[!UICONTROL Apply].**

1. 建立自訂目標為 *目標*：

   1. 在主功能表中，按一下 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. 在工具列中，按一下 ![建立](/help/dsp/assets/create-search-ui.png "建立").

   1. 輸入目標設定，包括非行動裝置和行動裝置的相關量度及其相對數值權重，然後儲存目標。

      至少一個量度必須有量度型別 *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] 自訂事件會遵循以下命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 範例： `custom_event_16_examplersid`
      >* [!DNL Analytics] 維度和區段無法用於Adobe Advertising最佳化。

      >[!TIP]
      >
      >為獲得最佳效能，自訂目標（目標）中的合併量度每天必須至少總十次轉換。 若未包含，最佳作法是將其他支援的轉換量度（例如產品頁面或應用程式啟動）新增至目標。 另請參閱 [建立自訂目標的最佳實務](#custom-goal-best-practices) 以取得指引。

在使用最佳化目標的套件的DSP套件設定中&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]，」目標名稱現在包含在 [!UICONTROL Custom Goals] 清單。 當您選取目標作為套件的自訂目標時， [!UICONTROL Conversion Metric] 清單包含目標的所有目標量度。

## 建立自訂目標的最佳實務 {#custom-goal-best-practices}

### 使用單一量度的自訂目標

下列範例說明如何設定以單一轉換量度為目標的目標。

#### 具有「」的行銷活動範例[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;最佳化目標

如果您的行銷活動目標是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，而來自所有裝置型別的收入對您而言同樣重要，則請包含&quot;[!UICONTROL Revenue]「非行動權重的量度（適用於非行動裝置的轉換）為1 (1)，而行動權重的量度（適用於行動裝置的轉換）為1 (1)。 選取量度型別 *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 行動權數或非行動權數一(1)等於追蹤的每個$1收入的一(1)值。
>
> 例如，非行動權重為1 (1)的$250轉換會回報為$250的轉換。 如果轉換量度被指派為0.5的非行動權重，則來自非行動裝置的$250轉換會報告為$125的Adobe Advertising($250的轉換* 0.5 [!UICONTROL Non-mobile Weight] = $125)。

#### 具有「」的行銷活動範例[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;最佳化目標

如果您的行銷活動目標是每次贏取的最低成本(CPA)，並且只需要一個成功事件（例如「應用程式提交」），則請納入該量度，並將量度型別指定為 *[!UICONTROL Goal]*. 最佳實務是將非行動權重與行動權重都設定為一(1)。

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 行動權重或行動權重一(1)對於所追蹤的每次轉換等於一(1)的值。 例如，如果追蹤10個「應用模組提交」轉換，則會報告10個「應用模組提交」轉換。 但是，如果轉換量度被指派為0.5的非行動權重，則10個非行動轉換會在Adobe Advertising中報告為五(5) （10個轉換* 0.5） [!UICONTROL Non-mobile Weight] = 5)。

### 具有多個量度的自訂目標

在兩種情況下，您會在自訂目標中使用多個量度：

* 您的行銷活動目標有多個成功事件。 例如，您可能會針對多個網站上的動作(PDF下載、聯絡我們和電子郵件註冊)進行廣告，這些動作都會對您的CPA目標有所貢獻。 如果目標包含三個獨立的量度，每個量度的非行動權重和行動權重各為1 (1)，則 [!DNL Adobe Sensei] 演演算法會將每個量度和使用者裝置型別視為同等重要性。 如果不同的量度和裝置型別具有不同的成本或重要性，您可以據此調整其相對權重。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自訂目標中的單一轉換量度無法達到最佳化效能所需的每天至少10次轉換。 發生此狀況的原因可能是每日封裝支出極低或自然轉換次數有限。 將其他支援量度新增至自訂目標可協助您實現每天10次轉換的臨界值。 10個支援事件可協助套件達到10/天臨界值，即便每個事件的權重都低於一(1)。 但您不一定需要新增那麼多的事件。

  當您將支援量度新增至自訂目標時，請根據支援量度對主要成功事件的相對重要性為其加權，並牢記資料點的數量。 這可讓Adobe Sensei演演算法平衡多個量度，並針對您的目標最佳化。

  下列範例目標包含三個量度，每個量度具有不同的非行動權重：應用程式提交= 1、應用程式開始= 0.1，以及廣告商登陸頁面= 0.01。這表示來自非行動裝置的每個應用程式提交轉換對您的業務而言都具有相同的值，平均有10個來自非行動裝置的應用程式開始轉換和100個來自非行動裝置的廣告商登陸頁面轉換。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

反之，如果您將應用程式提交的登陸頁面造訪次數平均加權，則較高的登陸頁面造訪次數可能會壓倒您的目標，並扭曲至登陸頁面造訪次數。<!--reword-->

>[!MORELIKETHIS]
>
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
