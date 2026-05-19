---
title: 建立可重複使用的對象
description: 瞭解如何建立可重複使用的受眾，其中包含受眾區段和其他儲存的受眾。 可選擇使用AI輔助受眾代理，透過在自然語言提示中描述您的目標受眾；代理會建議第三方區段並建置受眾運算式，以作為目標或排除專案。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# 建立可重複使用的對象

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他儲存的對象，您可將其用作多個位置的目標或排除專案。 手動建立受眾，或使用AI輔助受眾代理程式，根據您所述的需求，使用所有您可用的第一方和第三方區段來產生新的可重複使用受眾。

>[!NOTE]
>
>（DSP將其雜湊電子郵件ID轉換為LiveRamp RampID區段的廣告商）未附加至使用中、已排程或暫停位置的第一方RampID區段會暫停。 該區段在區段清單中記錄為「自動暫停」。

## 手動建立可重複使用的對象

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

1. 在[!UICONTROL New Audience]設定中：

   1. 輸入唯一的&#x200B;**[!UICONTROL Audience Name]**。

   1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的選項。

      當您共用對象時，該對象會成為帳戶中所有廣告商的目標或排除專案。 不過，受眾中的個別區段僅供共用區段的使用者使用。 例如，如果您將包含Adobe Analytics區段的對象與未對應至相同[!DNL Analytics]帳戶的廣告商共用，則不會在該廣告商的對象中預覽該區段。 在對象中只會預覽該廣告商可用的區段。

   1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 按一下右側面板中的&#x200B;**[!UICONTROL Switch to manual mode]**&#x200B;按鈕。

   AI選項是預設值。

1. 建立對象：

   >[!NOTE]
   >
   >當您建置對象時，右側面板中會更新詳細的[對象人數資料](audience-about.md)

   * 若要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]索引標籤](audience-settings.md)上可用的區段來手動建立區段邏輯，請執行下列動作。

      * （選用）搜尋區段名稱、說明或路徑。

        搜尋結果包括以您使用的確切辭彙為基礎的區段。 當您輸入多個字詞時，必須找到區段的所有字詞。

      * 若要新增第一個區段，請在左側面板中找出該區段，然後選取區段名稱旁的核取方塊。

      * 若要將區段新增至現有區段群組：

         1. 按一下右側面板中的區段群組。

         1. （選用）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

            *[!UICONTROL Exclude All]*&#x200B;不適用於第一個區段群組。 若對象僅包含排除專案，請將此對象建置為&#x200B;*[!UICONTROL Include Any]*，然後在位置中，從「排除的對象」選單中選取該對象。

         1. 在左側面板中找出新區段，並選取區段名稱旁的核取方塊。

            區段群組會自動更新為新區段。

      * 若要新增區段群組：

         1. 按一下右側面板中的&#x200B;**[!UICONTROL + New Group]**。

            1. （選用）視需要將上一個群組與新群組之間的邏輯變更為&#x200B;*[!UICONTROL And]*&#x200B;或&#x200B;*[!UICONTROL Or]*。

            1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

            1. （選用）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

   * 若要使用現有對象中的區段邏輯：

      1. 透過下列任何方式，從現有對象複製區段邏輯：

         * 在「所有對象」檢視中，將游標停留在對象列上，然後按一下「**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**」。

         * 在現有對象的設定中，按一下區段邏輯面板頂端的&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文字編輯器中，使用英數字元區段ID和[布林值語法](audience-segment-logic-syntax.md)手動建立區段邏輯，並將其複製到剪貼簿。

      1. 按一下&#x200B;**[!UICONTROL paste in an audience rule to begin building]**，將現有的區段邏輯貼到輸入欄位中，然後按一下&#x200B;**[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果對象已包含任何區段邏輯，則貼入新區段邏輯會覆寫現有邏輯。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 使用產生AI建立可重複使用的對象

*Beta功能*

*僅支援英文*

>[!NOTE]
>
>此功能目前處於Beta版模式，可能會有變動。 在建立對象並將其用於您的位置之前，請確定產生的對象運算式代表您想要的對象。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

1. 在[!UICONTROL New Audience]設定中：

   1. 輸入唯一的&#x200B;**[!UICONTROL Audience Name]**。

   1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的選項。

      當您共用對象時，該對象會成為帳戶中所有廣告商的目標或排除專案。 不過，受眾中的個別區段僅供共用區段的使用者使用。 例如，如果您將包含Adobe Analytics區段的對象與未對應至相同[!DNL Analytics]帳戶的廣告商共用，則不會在該廣告商的對象中預覽該區段。 在對象中只會預覽該廣告商可用的區段。

   1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 建立對象：

   1. 輸入一或多個提示，說明您要包含和排除的對象特性。 若要提交每個提示，請按一下![提交提示](/help/dsp/assets/submit-prompt.png "提交提示")。

      如需詳細資訊，請參閱[撰寫提示](#writing-prompts)和[建立對象簡介的最佳實務](#audience-brief-best-practices)。

      在適用時，代理程式會建議使用其他區段篩選器，協助您建立更有效的對象簡報。 您可以接受或拒絕建議。

      當受眾代理程式找到相關的區段時，會根據您的條件建立布林值受眾運算式。 在尋找相符區段以組合受眾之前，也會要求您核准。 您可以選擇忽略請求，然後繼續指定其他對象條件。

   1. 當受眾代理程式呈現的受眾運算式足以描述您的受眾時，請告訴受眾代理程式繼續組裝受眾。

      您可以輸入「繼續」、「確定」、「確定」、「是」或其他類似的字詞。 代理程式會列出每個特徵的所有建議區段（例如「Parents」）。 展開任何特徵可檢視針對該特徵建議的個別區段的相關詳細資訊。

   1. （如有必要）指定其他條件。 當受眾代理程式呈現符合您所有條件的受眾運算式時，請告訴受眾代理程式繼續組裝受眾。

      若要集合對象，請輸入「繼續」、「確定」、「是」或其他類似字詞。 代理程式會列出每個特徵的所有建議區段（例如「Parents」）。 展開任何特徵可檢視針對該特徵建議的個別區段的相關詳細資訊。

1. 當您對集合的對象感到滿意時，請按一下「**[!UICONTROL Create]**」以建立指定的對象。

   >[!NOTE]
   >
   >您之後無法再使用對象代理程式來編輯對象。 請改用[手動編輯對象運算式](/help/dsp/audiences/reusable-audience-edit.md)。

### 寫入提示的基本知識 {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### 提示應包含哪些內容？

* 使用清楚的描述性語言來說明目標對象。

   * 您可以輸入完整的句子或只輸入一串特性。 除非為清楚起見，否則不需要標點符號。

   * 一般而言，提示不區分大小寫。

   * 對象代理程式會辨識最常見的同義字。

* 提供您想要包含的所有對象特性，以及您明確想要排除的任何特性的詳細資訊。 您提供的詳細資料越多，取得符合您需求之結果的機會就越大。

* 識別要包含或排除的位置、裝置型別和資料提供者。

* 在儲存對象之前，會反複提供詳細資訊，以調整您的條件和產生的對象運算式。

* 瞭解透過實驗進行提示。

  如果您的提示不清楚，受眾代理只會要求另一個提示，以便您可以再試一次。

  對象代理程式不會自動將產生的對象運算式儲存為對象。 您只能按一下提示區域之外的[!UICONTROL Create]按鈕來儲存對象，這樣您就可以復原不想保留的任何變更。

請參閱[建立對象簡介的最佳實務](#audience-brief-best-practices)，以取得最佳化對象提示的進一步方法。

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### 您無法在提示中包含哪些內容？

* 現有對象運算式的參考。

* 英文以外的其他語言文字。

#### 對象代理程式回應範例及回覆方式

當對象代理程式需要您的回應時，您可以使用請求中的關鍵字或使用常見同義字進行回覆。

#### Audience Agent詢問您問題

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

您的肯定回覆： 「繼續」、「確定」、「確定」、「是」或其他類似字詞

您也可以忽略請求，改為繼續指定其他對象條件。

##### 受眾代理程式會要求您從多個選項中選擇

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

您的回覆： `1`、`proceed`、`2`、`maximum reach`等。

您也可以忽略請求，改為繼續指定其他對象條件。

### 建立對象簡介的最佳實務 {#audience-brief-best-practices}

對象摘要是定義行銷活動目標對象的策略性寫入。 精心設計的摘要可協助DSP受眾代理程式識別最相關的區段，以組合您的目標受眾。

#### 有效受眾簡介的重要元件

在您的簡介中儘可能加入以下清單中的對象屬性型別。 指定有關要排除的屬性的特定資訊。

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **人口統計**

  包括年齡範圍、性別、婚姻狀況、家庭組成（家庭人數、子女人數、多代家庭）等屬性。

* **社會經濟指標**

  透過家庭收入(HHI)等級、教育程度、職業/職稱、就業狀況以及房屋擁有狀況來建立財務能力。

* **地理引數**

  定義包括國家/地區、區域（歐洲、中東和非洲、亞太及北美）、人口密度（城市/郊區/農村）的位置範圍。

* **興趣和喜好程度**

  識別嗜好（運動、藝術、戶外活動）、媒體消費模式、品牌喜好和生活方式活動（旅遊、餐飲、娛樂）等激情和偏好設定。

* **心理圖形**

  擷取心態和價值，包括抱負（追求地位、自我改善）、核心價值（可持續性、創新、傳統）、性格特徵（冒險者、早期採用者）和購買動機。

* **行為訊號**

  可觀察的動作包括購買行為（購物頻率、管道偏好設定、品牌忠誠度）、線上行為（網站造訪、內容參與、社群媒體活動）和離線行為（商店造訪、事件出席、會籍）。

* **市場內意圖**

  透過正在研究的產品/服務類別、購買時間表（即時、近期、長期）以及觸發購買決策的相關生命週期事件，識別購買整備程度。

* **生命階段**

  目前階段的瞭解包括事業階段（學生、入門級、職業生涯中期、主管、已退休）、家庭階段（新婚、新父母、空巢家庭）和主要的人生轉變。

#### 適用於潛在客戶行銷活動的結構良好的對象簡介範例

以下範例是促銷活動的強大對象簡報，以提高知名度並試用優質餐具訂閱服務：

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
>* [建立和實施自訂區段](custom-segment-create.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
