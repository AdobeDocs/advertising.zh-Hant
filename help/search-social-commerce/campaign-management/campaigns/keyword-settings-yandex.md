---
title: '[!DNL Yandex]關鍵字設定'
description: 參考 [!DNL Yandex] 關鍵字的設定。
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex]關鍵字設定

Yandex關鍵字同時用於搜尋和顯示（內容）網路。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;關鍵字片語，包括關鍵字的任何[Yandex比對型別語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 每個關鍵字最多可以有七個單字，不包括停用詞。

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 變更[!DNL Yandex]關鍵字或比對型別會刪除現有關鍵字並建立新關鍵字。
>* 每個Yandex廣告群組最多可包含200個關鍵字。

**[!UICONTROL Status]：**&#x200B;關鍵字的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新關鍵字的預設值為&#x200B;*Active*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param1]** **[!UICONTROL Param2]：**&#x200B;當關鍵字用於顯示廣告時，`{param1}`和`{param2}`替代變數的值，這些變數會取代基本URL中廣告和網站連結的{param1}和{param2}的任何執行個體。 最大長度為255個位元組。

特殊字元會自動以UTF-8編碼。 例如，如果相關廣告的基底URL為&quot;http://www.example.com/{param1}，而{param1}的關鍵字層級值為&quot;shoes/flats.html&quot;，則廣告會導向http://www.example.com/shoes%2Fflats.html。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
