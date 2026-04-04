---
title: 建立 [!DNL Google Ads] 轉換值規則
description: 瞭解如何建立 [!DNL Google Ads] 轉換值規則。
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# 建立[!DNL Google Ads]轉換值規則

您可以在[!DNL Google Ads]帳戶中建立帳戶層級和促銷活動層級轉換值規則，以便在個別帳戶層級或更低層級追蹤轉換。 您無法針對在主要科目層次進行追蹤的跨科目轉換科目，建立相關規則。

每個規則最多包含兩個條件，以及當滿足條件時要套用的轉換值調整。 帳戶中的所有規則都必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。

您可以為每個行銷活動建立多個行銷活動層級規則。 但是，當帳戶層級規則已存在時，[!DNL Google Ads]尚未提供在[!DNL Google Ads]編輯器之外建立新帳戶層級規則的功能。 若要建立其他帳戶層級規則，請直接登入[!DNL Google Ads]並使用[!DNL Google Ads]編輯器。

**注意：**&#x200B;行銷活動層級轉換值規則會覆寫帳戶層級規則，而且只能將一個規則套用至轉換。 如需詳細資訊，請參閱[當轉換符合多個規則的條件時， [!DNL Google Ads] 如何決定要套用至轉換的規則](https://support.google.com/google-ads/answer/10520348)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   依預設，已選取&#x200B;**[!UICONTROL Campaign]**&#x200B;索引標籤以顯示所有行銷活動層級規則。

1. （選擇性）若要改為建立帳戶層級規則，請按一下&#x200B;**[!UICONTROL Account]**&#x200B;標籤。

1. 在工具列中按一下![建立](/help/search-social-commerce/assets/add.png "建立").<!-- Upload newer icon -->

1. 選取廣告網路和帳戶。 對於行銷活動層級規則，請同時選取行銷活動。 然後按一下&#x200B;**[!UICONTROL Next]**。

1. 設定[轉換規則設定](google-conversion-value-rule-settings.md)。

   您必須設定主要條件和值調整。 您可以選擇設定次要條件。

   在一個條件中，多個目標或排除專案會使用布林值運運算元OR聯結，因此必須符合任何選項才能起始值調整。 當您包含次要條件時，次要條件會使用布林運運算元ALL聯結至主要條件，因此必須符合兩個條件才能起始值調整。 範例：如果\[Location is Alignalia OR Tunis\]和\[Device is Mobile OR Tablet\]，則新增1.5。

   **注意：**&#x200B;帳戶中的所有規則必須使用相同型別的主要和（選擇性）次要條件。 例如，如果規則1包含主要條件「Audience」和次要條件「Location」，則帳戶中的所有其他規則都必須具備主要條件「Audience」。 其他規則包含次要條件時，必須是「位置」。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [關於 [!DNL Google Ads] 轉換值規則](about-google-conversion-value-rules.md)
>* [編輯 [!DNL Google Ads] 轉換值規則](edit-google-conversion-value-rule.md)
>* [變更 [!DNL Google Ads] 轉換值規則](change-the-status-of-google-conversion-value-rule.md)的狀態
>* [[!DNL Google Ads] 轉換值規則設定](google-conversion-value-rule-settings.md)

