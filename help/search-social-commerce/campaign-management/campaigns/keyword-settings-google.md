---
title: '[!DNL Google Ads]關鍵字設定'
description: 參考 [!DNL Google Ads] 關鍵字的設定。
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# [!DNL Google Ads]關鍵字設定

您可以為使用搜尋和顯示網路的行銷活動建立關鍵字。

請參閱Google廣告說明，瞭解每個帳戶](https://support.google.com/google-ads/answer/6372658)的[關鍵字限制。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;關鍵字，包括任何符合關鍵字及預留位置的[!DNL Google Ads]語法。 [!DNL Google Ads]帳戶需要具有以下屬性的關鍵字：

* 每個關鍵字的長度上限為80個字元，但不超過10個字元。
* 關鍵字只能包含字母、數字和下列特殊字元：空格`# $ & _ - " [] ' + . / :`

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 您可以從[!UICONTROL Keywords] > [!UICONTROL Negatives]檢視並在廣告群組和行銷活動設定中建立負面關鍵字。
>* 變更[!DNL Google Ads]關鍵字或比對型別會刪除現有關鍵字並建立新關鍵字。

**[!UICONTROL Status]：**&#x200B;關鍵字的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新關鍵字的預設值為&#x200B;*Active*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param1]：**&#x200B;如果基底URL或追蹤範本包含[動態替代字串`{param1}`](https://support.google.com/google-ads/answer/6305348)，則要用作替代值的字串。

**[!UICONTROL Param2]：**&#x200B;如果基底URL或追蹤範本包含[動態替代字串`{param2}`](https://support.google.com/google-ads/answer/6305348)，則要用作替代值的字串。

## URL選項

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
