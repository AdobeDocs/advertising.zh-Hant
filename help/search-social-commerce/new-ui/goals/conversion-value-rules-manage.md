---
title: （新UI）管理 [!DNL Google Ads] 轉換值規則
description: 瞭解如何在搜尋、社交和Commerce中檢視和管理 [!DNL Google Ads] 轉換值規則。
feature: Conversions
source-git-commit: c2fde4837c4300f4e55b3591992af64630d58ba6
workflow-type: tm+mt
source-wordcount: '1844'
ht-degree: 0%

---

# （新UI）管理[!DNL Google Ads]轉換值規則

*Beta功能*

[!DNL Google Ads] [轉換值規則](https://support.google.com/google-ads/answer/10518330)可讓您根據使用者資訊（包括裝置型別、位置和對象區段）調整轉換事件的值。 透過Google智慧競標，您可以在搜尋、顯示、購物和效能最大化行銷活動中使用價值型競標規則。 對於具有Maximize Conversions和Target ROAS競標策略的行銷活動，[!DNL Google Ads]演演算法將開始偏好具有較高值的轉換。

行銷活動層級轉換值規則會覆寫帳戶層級規則。 當轉換符合多個轉換值規則時，只會套用其中一個規則。 通常會套用最明確的規則，但請參閱不同規則條件型別](https://support.google.com/google-ads/answer/10520348)的優先順序的[[!DNL Google Ads] 檔案。

## [!UICONTROL Conversion Value Rules]檢視和功能

搜尋、Social和Commerce會自動同步您[!DNL Google Ads]帳戶的轉換值規則。 在[!DNL Google Ads]介面中建立的所有規則都會在24小時內同步，並可在[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]檢視中使用。

有些帳戶可以管理其轉換值規則：

* 在已在個別帳戶或促銷活動層級追蹤轉換的帳戶中，您可以[建立](#google-conversion-value-rule-create)、[編輯](#google-conversion-value-rule-edit)和[變更帳戶層級和促銷活動層級規則的狀態](#google-conversion-value-rule-change-status)。

  這些帳戶可以連結到[!DNL Google Ads]個管理員帳戶，但它們不能使用跨帳戶轉換追蹤（針對此追蹤，會跨管理員帳戶中的所有帳戶來追蹤轉換）。

* 在使用跨帳戶轉換追蹤的帳戶中，您的帳戶層級和促銷活動層級規則繼承自管理員帳戶，且為唯讀。

## 使用搜尋、社交和Commerce產品組合的轉換值規則

當廣告商帳戶設定為將「搜尋」、「社交」和「Commerce」目標上傳至「[!DNL Google Ads]」，且您在具有目標的產品組合中加入使用轉換值規則的促銷活動時，[!DNL Google Ads]會將轉換值規則套用至目標中指定的原始轉換值。 因此，搜尋、社交和Commerce中的轉換資料與[!DNL Google Ads]中的轉換資料不同。

例如，假設目標使用單一轉換量度「銷售機會」，並將來自行動裝置的轉換權重設為10，將來自非行動裝置的轉換權重設為10。 搜尋、Social和Commerce會將任一裝置型別的事件計為一(1)次轉換，並將轉換值計為10。 然而，假設該投資組合中的行銷活動使用轉換值規則「如果裝置為行動，則乘以2。」 當為該行銷活動追蹤行動銷售機會事件時，[!DNL Google Ads]也會將轉換計數計為一(1)，但轉換值計為(10 x 2) = 20。

若要檢視規則的詳細資訊，包括套用規則之前的原始轉換值，請參閱 [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848)中的[轉換值規則報告。

## 建立[!DNL Google Ads]轉換值規則 {#google-conversion-value-rule-create}

您可以在[!DNL Google Ads]帳戶中建立帳戶層級和促銷活動層級轉換值規則，以便在個別帳戶層級或更低層級追蹤轉換。 您無法針對在主要科目層次進行追蹤的跨科目轉換科目，建立相關規則。

每個規則最多包含兩個條件，以及當滿足條件時要套用的轉換值調整。 帳戶中的所有規則都必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。

您可以為每個行銷活動建立多個行銷活動層級規則。 但是，當帳戶層級規則已存在時，[!DNL Google Ads]尚未提供在[!DNL Google Ads]編輯器之外建立新帳戶層級規則的功能。 若要建立其他帳戶層級規則，請直接登入[!DNL Google Ads]並使用[!DNL Google Ads]編輯器。

**注意：**&#x200B;行銷活動層級轉換值規則會覆寫帳戶層級規則，而且只能將一個規則套用至轉換。 如需詳細資訊，請參閱[當轉換符合多個規則的條件時， [!DNL Google Ads] 如何決定要套用至轉換的規則](https://support.google.com/google-ads/answer/10520348)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   依預設，已選取&#x200B;**[!UICONTROL Campaign]**&#x200B;索引標籤以顯示所有行銷活動層級規則。

1. （選擇性）若要改為建立帳戶層級規則，請按一下&#x200B;**[!UICONTROL Account]**&#x200B;標籤。

1. 在工具列中按一下&#x200B;**[!UICONTROL Create Campaign Rule]** （從[!UICONTROL Campaign]索引標籤）或&#x200B;**[!UICONTROL Create Account Rule]** （從[!UICONTROL Account]索引標籤）。

1. 選取廣告網路和帳戶。 對於行銷活動層級規則，請同時選取行銷活動。 然後按一下&#x200B;**[!UICONTROL Next]**。

1. 設定[轉換規則設定](#google-ads-conversion-value-rule-settings)。

   您必須設定主要條件和值調整。 您可以選擇設定次要條件。

   在條件內，使用布林運運算元`OR`聯結多個目標或排除專案，因此任何選項都可以符合，以啟動值調整。 當您包含次要條件時，次要條件會使用布林運運算元`ALL`聯結至主要條件，因此必須符合兩個條件才能起始值調整。 範例：如果\[Location is Alignalia OR Tunis\]和\[Device is Mobile OR Tablet\]，則新增1.5。

   **注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 編輯[!DNL Google Ads]轉換值規則 {#google-conversion-value-rule-edit}

您可以在帳戶/行銷活動中編輯轉換值規則，其轉換會在個別帳戶層級或更低層級進行追蹤。 對於在主帳戶層級進行追蹤的跨帳戶轉換，您無法編輯其帳戶的規則。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   依預設，已選取&#x200B;**[!UICONTROL Campaign]**&#x200B;索引標籤以顯示所有行銷活動層級規則。

1. （選擇性）若要改為檢視所有帳戶層級規則，請按一下&#x200B;**[!UICONTROL Account]**&#x200B;標籤。

1. 選取規則旁的核取方塊。

1. 在大量動作工具列中按一下（/help/search-social-commerce/assets/edit-new.png「編輯」）。

1. 編輯[轉換規則設定](#google-ads-conversion-value-rule-settings)。

   您無法編輯現有規則的條件型別，但可以編輯條件和值調整。

   您必須設定主要條件和值調整。 您可以選擇設定次要條件。

   **注意：**&#x200B;如果您新增次要條件，則其條件型別必須與帳戶中的其他規則相同。 例如，如果帳戶中的規則1其他規則具有次要條件「Location」，則當其他規則包含次要條件時，次要條件必須為「Location」。 當您包含次要條件時，次要條件會使用布林運運算元`ALL`聯結至主要條件，因此必須符合兩個條件才能起始值調整。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 變更[!DNL Google Ads]轉換值規則的狀態 {#google-conversion-value-rule-change-status}

對於在個人帳戶層級追蹤轉換的帳戶和行銷活動，您可以暫停、啟用或刪除其中的轉換值規則。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   依預設，已選取&#x200B;**[!UICONTROL Campaign]**&#x200B;索引標籤以顯示所有行銷活動層級規則。

1. （選擇性）若要改為檢視所有帳戶層級規則，請按一下&#x200B;**[!UICONTROL Account]**&#x200B;標籤。

1. 選取每一列旁的核取方塊以進行變更。

1. 在大量動作工具列中，

   * 若要啟用（啟用）暫停的規則，請按一下「**[!UICONTROL ...]>[!UICONTROL Activate]**」。

   * 若要暫停作用中的規則，請按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Pause]**。

   * 若要刪除作用中或暫停的規則，請按一下![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## [!DNL Google Ads]轉換值規則設定 {#google-conversion-value-rule-settings}

| 章節 | 引數 | 說明 |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | 廣告網路。 |
| | [!UICONTROL Account] | 廣告網路帳戶。 |
| | [!UICONTROL Campaign] | （僅限促銷活動層級轉換值規則）廣告促銷活動。 |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[條件型別\] | （現有規則為唯讀）觸發值調整所必須符合的條件型別：<ul><li>*[!UICONTROL Device]：*&#x200B;若要鎖定所有或特定的裝置型別。</li><li>*[!UICONTROL Location]：*&#x200B;若要鎖定所有國家和地區，或鎖定並排除特定位置。</li><li>*[!UICONTROL Audiences]：*&#x200B;若要鎖定所有或特定對象</li></ul>**注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。 |
| | \[條件型別\] > [!UICONTROL Device]和[!UICONTROL Device Level] | （僅限裝置條件）目標裝置型別：<ul><li>*[!UICONTROL All devices]：**若要鎖定所有裝置型別。</li><li>*[!UICONTROL Select devices]：*&#x200B;若要指定一或多個要定位的裝置型別： *[!UICONTROL Desktop]：*、*[!UICONTROL Mobile]*&#x200B;以及&#x200B;*[!UICONTROL Tablet]：*。</li></ul>在條件內，使用布林運運算元`OR`聯結多個目標，因此任何選項都可以符合，以啟動值調整。 範例：如果\[Device is Mobile OR Tablet\]，則新增1.5。 |
| | \[條件型別\] > [!UICONTROL Location]和[!UICONTROL Location Level] | （僅限位置條件）位置目標與排除專案：<ul><li>*[!UICONTROL All countries and territories]：*&#x200B;若要鎖定所有國家/地區和位置，或鎖定並排除特定位置。</li><li>*[!UICONTROL Enter a location]：*&#x200B;若要鎖定和排除特定位置。</li></ul><ul><li>若要展開位置或子位置，請按一下名稱后面的`>`。</li><li>若要新增目標，請選取目標一次，以顯示綠色核取記號。</li><li>若要排除目標，請再次選取該目標以顯示紅色的&#x200B;**[!UICONTROL X]**。</li><li>若要移除目標或排除專案，請執行下列其中一項操作：<ul><li>按一下[!UICONTROL Selections]欄中專案旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。</li><li>選取目標，直到沒有核取記號或[!UICONTROL X]出現。</li></ul></li></ul>在條件內，使用布林運運算元`OR`聯結多個目標或排除專案，因此任何選項都可以符合，以啟動值調整。 範例：如果\[Location is Alignalia OR Tunities\]，則新增1.5。 |
| | \[條件型別\] > [!UICONTROL Audience]和[!UICONTROL Audience Level] | （僅限對象條件）對象目標：<ul><li>*[!UICONTROL All audience segments]：*&#x200B;若要鎖定所有[!DNL Google Ads]個對象區段。</li><li>*[!UICONTROL Enter audience segments]：*&#x200B;以鎖定特定的[!DNL Google Ads]對象區段。</li></ul><ul><li>若要將類別或子類別展開至其區段，請按一下名稱后面的`>`。</li><li>若要新增目標，請選取目標。</li><li>若要移除目標，請取消選取該目標，或按一下[!UICONTROL Selection]欄中專案旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。</li></ul>在一個條件中，多個目標或排除專案會使用布林值運運算元OR聯結，因此必須符合任何選項才能起始值調整。 範例：如果\[Audience is Bargain Travelers OR Family Vacationers\]，則新增1.5。<br><br>**注意：**&#x200B;一旦儲存對象目標，您可以新增其他對象，但無法在[!DNL Google Ads]編輯器外部移除這些對象。 如果您需要移除對象目標，請直接登入[!DNL Google Ads]並使用[!DNL Google Ads]編輯器。 |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[條件型別\] | （選用；現有規則為唯讀）觸發值調整所必須滿足的條件型別。 當您包含次要條件時，次要條件會使用布林運運算元`ALL`聯結至主要條件，因此必須符合兩個條件才能起始值調整。 範例：如果\[Location is Alignalia OR Tunizis\]和\[Device is Mobile OR Tablet\]，則新增1.5。<br><br>檢視主要條件的專案以取得說明。<br><br>**注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。 |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation]和[!UICONTROL Adjustment Value] | 指定調整型態，然後輸入正值：<ul><li>*[!UICONTROL Add]：*&#x200B;將指定的值新增至傳遞的轉換值。 值必須大於零(0)。</li><li>*[!UICONTROL Multiply]：*&#x200B;將傳遞的轉換值乘以指定的值。 值必須介於0.5到10之間。</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
