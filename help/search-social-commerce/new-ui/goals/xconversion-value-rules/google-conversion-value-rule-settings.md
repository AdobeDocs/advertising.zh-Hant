---
title: '[!DNL Google Ads]轉換值規則設定'
description: 參考 [!DNL Google Ads] 轉換值規則的設定。
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# [!DNL Google Ads]轉換值規則設定

<!-- Go through all -->

| 章節 | 引數 | 說明 |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | 廣告網路。 |
| | [!UICONTROL Account] | 廣告網路帳戶。 |
| | [!UICONTROL Campaign] | 廣告行銷活動。 |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[條件型別\] | （現有規則為唯讀）觸發值調整所必須符合的條件型別：<ul><li>**裝置：**&#x200B;將目標鎖定於所有或特定的裝置型別。</li><li>**位置：**&#x200B;若要鎖定所有國家和地區，或鎖定並排除特定位置。</li><li>**對象：**&#x200B;若要鎖定所有或特定對象</li></ul>**注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。 |
| | 狀態型別>裝置 | （僅限裝置條件）目標裝置型別：<ul><li>**所有裝置** — 鎖定所有裝置型別。</li><li>**選取裝置** — 若要指定一或多個要定位的裝置型別： **案頭**、**行動裝置**&#x200B;以及&#x200B;**平板電腦**。</li></ul>在一個條件中，您會使用布林運運算元OR聯結多個目標，因此必須符合任何選項才能起始值調整。 範例：如果\[Device is Mobile OR Tablet\]，則新增1.5。 |
| | 條件型別>位置 | （僅限位置條件）位置目標與排除專案：<ul><li>**所有國家/地區和地區** — 鎖定所有國家/地區和位置，或鎖定並排除特定位置。</li><li>**輸入位置** — 以定位並排除特定位置。</li></ul><ul><li>若要展開位置或子位置，請按一下名稱后面的> 。</li><li>若要新增目標，請選取目標一次，以顯示綠色核取記號。</li><li>若要排除目標，請再次選取該目標以顯示紅色的&#x200B;**[!UICONTROL X]**。</li><li>若要移除目標或排除專案，請執行下列其中一項操作：<ul><li>按一下![欄中專案旁的](/help/search-social-commerce/assets/delete.png "刪除")刪除[!UICONTROL Selections]。</li><li>選取目標，直到沒有核取記號或[!UICONTROL X]出現。</li></ul></li></ul>在一個條件中，多個目標或排除專案會使用布林值運運算元OR聯結，因此必須符合任何選項才能起始值調整。 範例：如果\[Location is Alignalia OR Tunities\]，則新增1.5。 |
| | 條件型別>對象 | （僅限對象條件）對象目標：<ul><li>**所有受眾區段** — 將目標鎖定在所有[!DNL Google Ads]受眾區段。</li><li>**輸入對象區段** — 將特定的[!DNL Google Ads]對象區段設為目標。</li></ul><ul><li>若要將類別或子類別展開至其區段，請按一下名稱后面的「 > 」。</li><li>若要新增目標，請選取目標。</li><li>若要移除目標，請取消選取該目標，或按一下[選取]資料欄中專案旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。</li></ul>在一個條件中，多個目標或排除專案會使用布林值運運算元OR聯結，因此必須符合任何選項才能起始值調整。 範例：如果\[Audience is Bargain Travelers OR Family Vacationers\]，則新增1.5。<br><br>**注意：**&#x200B;一旦儲存對象目標，您可以新增其他對象，但無法在[!DNL Google Ads]編輯器外部移除這些對象。 如果您需要移除對象目標，請直接登入[!DNL Google Ads]並使用[!DNL Google Ads]編輯器。 |
| 條件>次要條件 | | （選用；現有規則為唯讀）觸發值調整所必須滿足的條件型別。 當您包含次要條件時，次要條件會使用布林運運算元ALL聯結至主要條件，因此必須符合兩個條件才能起始值調整。 範例：如果\[Location is Alignalia OR Tunis\]和\[Device is Mobile OR Tablet\]，則新增1.5。<br><br>如需說明，請參閱Primary Condition專案。<br><br>**注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。 |
| 值調整 | 值 | 指定調整型態，然後輸入正值：<ul><li>**新增** — 將指定的值新增至傳遞的轉換值。 值必須大於零(0)。</li><li>**乘** — 將傳遞的轉換值乘以指定的值。 值必須介於0.5到10之間。</li></ul> |

>[!MORELIKETHIS]
>
>* [關於 [!DNL Google Ads] 轉換值規則](about-google-conversion-value-rules.md)
>* [建立 [!DNL Google Ads] 轉換值規則](create-google-conversion-value-rule.md)
>* [編輯 [!DNL Google Ads] 轉換值規則](edit-google-conversion-value-rule.md)
>* [變更 [!DNL Google Ads] 轉換值規則](change-the-status-of-google-conversion-value-rule.md)的狀態

