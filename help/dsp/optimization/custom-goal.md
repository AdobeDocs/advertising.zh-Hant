---
title: 自訂目標
description: 瞭解自訂目標，以在針對最低CPA或最高ROAS而最佳化的套件中定義成功事件。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1207
ht-degree: 0%

---

# 自訂目標

自訂目標定義廣告商實現其業務目標所需的成功事件。 每個使用最佳化目標&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;的套件都必須包含自訂目標，以協助達成整體最佳化目標。 您可以在[!DNL Advertising Search, Social, & Commerce]中將自訂目標建立為&#x200B;*目標*。 DSP每個目標的名稱都必須加上前置詞「ADSP_」。

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每個自訂目標（目標）包含一或多個轉換量度，以及這些量度的相對權重。 可用的轉換量度包含使用Adobe Advertising轉換畫素及透過Adobe Analytics追蹤的所有量度。 DSP自訂目標只會考量非行動權重，但會用於所有廣告型別。

例如，假設三個轉換量度與您的其中一個行銷活動中的特定套件相關：價值20美元的「PDF下載」、價值30美元的「電子郵件註冊」和價值40美元的「訂單確認」。 如果您想要根據客戶動作的一次性貨幣值給予權重，則量度的相對權重為1、1.5和2。

在您[建立自訂目標](#custom-goal-create)後，您可以[將其指派給套件](/help/dsp/campaign-management/packages/package-settings.md)，以使用[!DNL Adobe AI]進行報告和演演算法最佳化。

權重建議是自動為目標中DSP歸因的量度產生，只要按一下即可套用所有權重建議。 前置詞為&quot;ADSP_&quot;的目標之所有權重變更，都會在兩天內以演演算法方式套用至DSP。 如需加權建議的詳細資訊，請參閱「目標」的「最佳化指南」章節，此章節可在「搜尋」、「社交」和「Commerce」中取得。

## 建立自訂目標 {#custom-goal-create}

若要建立自訂目標，DSP帳戶必須從[!DNL Search, Social, & Commerce]使用者端設定中，連結至具有相同Adobe CX Enterprise組織ID的[!DNL Search, Social, & Commerce]帳戶。 如果您的DSP帳戶未連結至[!DNL Search, Social, & Commerce]帳戶，請連絡您的Adobe帳戶團隊。

1. [登入Advertising Search、Social和Commerce](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}。

1. 確認已追蹤您要在目標中納入的量度、可在產品中使用，且包含顯示名稱：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]** > **[!UICONTROL Conversions]**。

      「轉換」檢視會在新的瀏覽器或瀏覽器標籤中開啟。

   1. 找到量度，並確定已為量度啟用&#x200B;**[!UICONTROL Show in UI and Reports]**。

      >[!NOTE]
      >
      >* [!DNL Analytics]個自訂事件遵循此命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 範例： `custom_event_16_examplersid`

   1. 如果量度在&#x200B;**[!UICONTROL Display Name]**&#x200B;欄中沒有值，則按一下儲存格，輸入顯示名稱，然後按一下&#x200B;**[!UICONTROL Apply]。**

1. [建立自訂目標為&#x200B;*目標*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}。 請考量下列事項：

   * 若為Advertising DSP套件使用的目標，目標名稱的開頭必須是「ADSP_」，例如「ADSP_Registrations」。 首碼不區分大小寫。

   * 僅包含歸因於DSP的量度。 歸因於「搜尋」、「社交」和「Commerce」或任何其他廣告網路的任何量度都會被忽略。

   * 至少一個量度必須有量度型別&#x200B;*[!UICONTROL Goal]*。

   * DSP會對所有廣告使用非行動權重。 任何指定的行動權重都會被忽略。

   >[!NOTE]
   >
   >* [!DNL Analytics]個自訂事件遵循此命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 範例： `custom_event_16_examplersid`
   >* [!DNL Analytics]維度和區段無法用於Adobe Advertising最佳化。

   >[!TIP]
   >
   >為獲得最佳效能，自訂目標（目標）中的合併量度每天必須至少總十次轉換。 若未包含，最佳作法是將其他支援的轉換量度（例如產品頁面或應用程式啟動）新增至目標。 如需准則，請參閱[建立自訂目標的最佳實務](#custom-goal-best-practices)。

在使用最佳化目標&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot;或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;之套件的DSP套件設定中，目標名稱現在包含在[!UICONTROL Custom Goals]清單中。 當您選取目標作為封裝的自訂目標時，[!UICONTROL Conversion Metric]清單會包含目標的所有目標量度。

## 建立自訂目標的最佳實務 {#custom-goal-best-practices}

### 使用單一量度的自訂目標

下列範例說明如何設定以單一轉換量度為目標的目標。

#### 具有&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;最佳化目標的行銷活動範例

如果您的行銷活動目標是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，且來自所有裝置型別的收入對您而言同樣重要，則請包含非行動權重為1 (1)的&quot;[!UICONTROL Revenue]&quot;量度；行動權重會被忽略。 選取量度型別&#x200B;*[!UICONTROL Goal]*。

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> A non-mobile weight of one (1) equates to a value of one (1) for each $1 of revenue that&#39;s tracked for display ads on any device. For example, a $250 conversion with a non-mobile weight of one (1) is reported as $250 for conversions. If the conversion metric is assigned a non-mobile weight of 0.5, then the $250 conversion is reported as $125 in Adobe Advertising ($250 Conversion * 0.5 [!UICONTROL Non-mobile Weight] = $125).

#### 具有&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;最佳化目標的行銷活動範例

如果您的行銷活動目標是每次贏取的最低成本(CPA)，並且只需要一個成功事件（例如「應用程式提交」），則請包含該量度，並將量度型別指定為&#x200B;*[!UICONTROL Goal]*。 最佳實務是將非行動權重設定為一(1)；行動權重會被忽略。

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 針對任何裝置上的顯示廣告所追蹤的每次轉換，一(1)的非行動權重等於一(1)的值。 例如，如果追蹤10個「應用模組提交」轉換，則會報告10個「應用模組提交」轉換。 但是，如果轉換量度被指派為0.5的非行動權重，則10次轉換在Adobe Advertising中會報告為5 (5) （10次轉換* 0.5 [!UICONTROL Non-mobile Weight] = 5）。

### 具有多個量度的自訂目標

在兩種情況下，您會在自訂目標中使用多個量度：

* 您的行銷活動目標有多個成功事件。 例如，您可能會針對多個網站上的動作（PDF下載、聯絡我們及電子郵件註冊）進行廣告，這些動作都會對您的CPA目標有所貢獻。 如果目標包含三個個別的量度，每個量度的非行動權重為一(1)，則[!DNL Adobe AI]支援的演演算法會將每個量度和使用者裝置型別視為同等重要性。 如果不同量度的成本或重要性不同，您可以據此調整其相對權重。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自訂目標中的單一轉換量度無法達到最佳化效能所需的每天至少10次轉換。 發生此狀況的原因可能是每日封裝支出極低或自然轉換次數有限。 將其他支援量度新增至自訂目標可協助您實現每天10次轉換的臨界值。 10個支援事件可協助套件達到10/天臨界值，即便每個事件的權重都低於一(1)。 但您不一定需要新增那麼多的事件。

  當您將支援量度新增至自訂目標時，請根據支援量度對主要成功事件的相對重要性為其加權，並牢記資料點的數量。 這可讓[!DNL Adobe AI]支援的演演算法平衡多個量度，並針對您的目標最佳化。

  下列範例目標包含三個量度，每個量度具有不同的非行動權重：應用程式提交= 1、應用程式開始= 0.1，以及廣告商登陸頁面= 0.01。 這表示每個應用程式提交轉換對您的企業而言平均有10個應用程式開始轉換和100個廣告商登陸頁面轉換，它們具有相同的價值。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

反之，如果您將登陸頁面造訪次數加權平均至應用程式提交次數，則原本較高的登陸頁面造訪次數可能會壓垮您的目標，並扭曲至登陸頁面造訪次數。<!--reword-->

>[!MORELIKETHIS]
>
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
