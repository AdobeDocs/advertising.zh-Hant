---
title: '[!DNL Yandex]關鍵字設定'
description: 參考[!DNL Yandex]關鍵字的設定。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex]關鍵字設定

[!DNL Yandex]關鍵字同時用於搜尋和顯示（內容）網路。

## [!UICONTROL Basic Settings]

*僅限新關鍵字*

**[!UICONTROL Network]：**&#x200B;廣告網路。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign]：**&#x200B;行銷活動。

**[!UICONTROL Ad Group]：**&#x200B;廣告群組。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;關鍵字片語，包括關鍵字的任何[[!DNL Yandex] 相符型別語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 每個關鍵字最多可以有七個單字，不包括停用詞。

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 變更[!DNL Yandex]關鍵字或比對型別會刪除現有關鍵字並建立新關鍵字。
>* 每個[!DNL Yandex]廣告群組最多可包含200個關鍵字。

**[!UICONTROL Status]：**&#x200B;關鍵字的顯示狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。 新關鍵字的預設值為&#x200B;*[!UICONTROL Active]*。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>特殊字元會自動以UTF-8編碼。 例如，如果相關廣告的基底URL為`http://www.example.com/{param1}`，而關鍵字層級值為`{param1}`，則廣告會導向`http://www.example.com/shoes%2Fflats.html`。`shoes/flats.html`

**[!UICONTROL Param1]：**&#x200B;當關鍵字用於顯示廣告時，如果基礎URL包含廣告和網站連結的`{param1}`動態替代字串，則要用作替代值的字串。 最大長度為255個位元組。

**[!UICONTROL Param2]：**&#x200B;當關鍵字用於顯示廣告時，如果基礎URL包含廣告和網站連結的`{param2}`動態替代字串，則要用作替代值的字串。 最大長度為255個位元組。

>[!MORELIKETHIS]
>
>* [管理關鍵字](keyword-manage.md)
