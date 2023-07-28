---
title: 『[!DNL Google Ads] 關鍵字設定
description: 參考設定 [!DNL Google Ads] 關鍵字。
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] 關鍵字設定

您可以為使用搜尋和顯示網路的行銷活動建立關鍵字。

請參閱Google Ads說明，瞭解 [每個帳戶的關鍵字限制](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字，包括任何 [!DNL Google Ads] 比對關鍵字及預留位置的語法。 [!DNL Google Ads] 帳戶需要具有以下屬性的關鍵字：

* 每個關鍵字的長度上限為80個字元，但不超過10個字元。
* 關鍵字只能包含字母、數字和下列特殊字元：空格 `# $ & _ - " [] ' + . / :`

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 您可以從以下位置建立負關鍵字： [!UICONTROL Keywords] > [!UICONTROL Negatives] 在廣告群組和促銷活動設定中檢視和。
>* 變更 [!DNL Google Ads] keyword或match type會刪除現有的關鍵字，並建立新的關鍵字。

**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param1]：** 如果基礎URL或追蹤範本包含 [此 `{param1}`](https://support.google.com/google-ads/answer/6305348) 動態替代字串。

**[!UICONTROL Param2]：** 如果基礎URL或追蹤範本包含 [此 `{param2}`](https://support.google.com/google-ads/answer/6305348) 動態替代字串。

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
