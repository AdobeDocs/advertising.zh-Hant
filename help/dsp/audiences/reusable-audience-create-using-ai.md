---
title: 使用產生AI建立可重複使用的對象
description: 瞭解如何使用AI輔助受眾代理在Adobe Advertising DSP中建立可重複使用的受眾。 以自然語言提示描述您的目標對象；代理程式會建議協力廠商區段，並建立對象運算式以作為目標或排除專案。
feature: DSP Audiences
hidefromtoc: true
hide: true
source-git-commit: c632774e68069ab03f41fb9453a27c6fe63c8168
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---

# 使用產生AI建立可重複使用的對象

*Beta功能*

*僅以英文提示*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

使用AI輔助受眾代理，根據您宣告的要求，使用您可用的所有第三方區段來產生新的可重複使用受眾。 您可以使用對象作為多個位置的目標或排除專案。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>此功能目前處於Beta版模式，可能會有變動。 在建立對象並將其用於您的位置之前，請確定產生的對象運算式代表您想要的對象。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

1. 輸入唯一的&#x200B;**[!UICONTROL Audience Name]**。

1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的選項。

   當您共用對象時，該對象會成為帳戶中所有廣告商的目標或排除專案。 不過，受眾中的個別區段僅供共用區段的使用者使用。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 建立對象：

   若使用者擁有測試版許可權，預設為AI選項。 若要[自行組合對象](/help/dsp/audiences/reusable-audience-create.md)，請按一下底部的「切換到手動模式」按鈕。

   1. 輸入一或多個提示，說明您要包含和排除的對象特性。 若要提交每個提示，請按一下![提交提示](/help/dsp/assets/submit-prompt.png "提交提示")。

      如需詳細資訊，請參閱[撰寫提示](#writing-prompts)和[建立對象簡介的最佳實務](#audience-brief-best-practices)。

      當AI代理程式找到相關的區段時，就會根據您的條件建立對象運算式。 在尋找相符區段以組合受眾之前，也會要求您核准。

      您可以選擇忽略請求，然後繼續指定其他對象條件。

   1. 當AI代理程式呈現足以描述您的對象的對象運算式時，請告訴AI代理程式繼續組裝對象。

      您可以輸入「繼續」、「確定」、「確定」、「是」或其他類似的字詞。

1. （如有必要）指定其他條件。 當AI代理程式呈現符合您所有條件的對象運算式時，請告訴AI代理程式繼續組裝對象。

1. 當您對集合的對象感到滿意時，請按一下「**[!UICONTROL Create]**」以建立指定的對象。

   >[!NOTE]
   >
   >您之後無法使用AI代理程式編輯對象。 請改用[手動編輯對象運算式](/help/dsp/audiences/reusable-audience-edit.md)。

## 正在寫入提示 {#writing-prompts}

### 提示應包含哪些內容？

* 使用清楚的描述性語言來說明目標對象。

* 提供您想要包含的所有對象特性，以及您明確想要排除的任何特性的詳細資訊。 您提供的詳細資料越多，取得符合您需求之結果的機會就越大。

* 識別要包含或排除的位置、裝置型別和資料提供者。

* 在儲存對象之前，會反複提供詳細資訊，以調整您的條件和產生的對象運算式。

* 瞭解透過實驗進行提示。

  對象代理程式不會自動將產生的對象運算式儲存為對象。 您只能按一下提示區域之外的[!UICONTROL Create]按鈕來儲存對象，這樣您就可以復原不想保留的任何變更。

請參閱[建立對象簡介的最佳實務](#audience-brief-best-practices)，以取得最佳化對象提示的進一步方法。

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### 您無法在提示中包含哪些內容？

* 現有對象運算式的參考。

* 英文以外的其他語言文字。

### AI代理程式回應範例及回覆方式

當AI代理程式需要您的回應時，您可以使用要求中的關鍵字或相當的常用詞匯進行回覆。

#### AI代理程式回應詢問您問題

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

您的肯定回覆： 「繼續」、「確定」、「確定」、「是」或其他類似字詞

您也可以忽略請求，改為繼續指定其他對象條件。

#### AI代理程式回應會要求您從多個選項中選擇

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

您的回覆： `1`、`proceed`、`2`、`maximum reach`等。

您也可以忽略請求，改為繼續指定其他對象條件。

## 建立對象簡介的最佳實務 {#audience-brief-best-practices}

對象摘要是定義行銷活動目標對象的策略性寫入。 精心設計的摘要可協助DSP受眾代理程式識別最相關的區段，以組合您的目標受眾。

### 有效受眾簡介的基本元件

#### 對象屬性

在簡報中包含下列清單中儘可能多的屬性型別。 指定有關要排除的屬性的特定資訊。

<!-- What about these:

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

### 潛在行銷活動之結構良好的對象簡報範例

以下範例是促銷活動的強大對象簡報，以提高知名度並試用優質餐具訂閱服務：

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [重複可重複使用的對象](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [編輯可重複使用的對象](/help/dsp/audiences/reusable-audience-edit.md)
>* [檢視可重複使用對象的詳細資料](/help/dsp/audiences/reusable-audience-view-details.md)
>* [共用可重複使用的對象](/help/dsp/audiences/reusable-audience-share.md)
>* [匯出可重複使用的對象](/help/dsp/audiences/reusable-audience-export.md)
>* [將可重複使用對象的區段金鑰複製到剪貼簿](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [刪除可重複使用的對象](/help/dsp/audiences/reusable-audience-delete.md)
