---
title: '"[!DNL Yandex] 關鍵字設定」'
description: 參考設定 [!DNL Yandex] 關鍵字。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] 關鍵字設定

Yandex關鍵字同時用於搜尋和顯示（內容）網路。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字片語，包括任何 [Yandex比對型別語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html) 用於關鍵字。 每個關鍵字最多可以有7個單字（停用字除外）。

您最多可以輸入或貼上2000個關鍵字。 以逗號分隔多個關鍵字，或在不同的行中輸入關鍵字。

>[!NOTE]
>
>* 變更 [!DNL Yandex] keyword或match type會刪除現有關鍵字並建立新關鍵字。
>* 每個Yandex廣告群組最多可包含200個關鍵字。


**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param1]** **[!UICONTROL Param2]：** 的值 `{param1}` 和 `{param2}` 替代變數，可在使用關鍵字顯示廣告時，取代基本URL中廣告和網站連結的{param1}和{param2}的任何執行個體。 最大長度為255個位元組。

特殊字元會自動以UTF-8編碼。 例如，如果相關廣告的基底URL為「http://www.example.com/{param1}」，而{param1}的關鍵字層級值為「shoes/flats.html」，則廣告會導向http://www.example.com/shoes%2Fflats.html。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

