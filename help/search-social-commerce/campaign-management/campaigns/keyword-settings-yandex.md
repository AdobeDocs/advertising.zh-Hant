---
title: 『[!DNL Yandex] 關鍵字設定
description: 參考設定 [!DNL Yandex] 關鍵字。
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] 關鍵字設定

Yandex關鍵字同時用於搜尋和顯示（內容）網路。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字片語，包括任何 [Yandex比對型別語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html) 用於關鍵字。 每個關鍵字最多可以有七個單字，不包括停用詞。

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 變更 [!DNL Yandex] keyword或match type會刪除現有的關鍵字，並建立新的關鍵字。
>* 每個Yandex廣告群組最多可包含200個關鍵字。

**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param1]** **[!UICONTROL Param2]：** 的值 `{param1}` 和 `{param2}` 替代變數，這些變數會替代任何的例項 {param1} 和 {param2} 關鍵字用於顯示廣告時，位於廣告和網站連結的基本URL中。 最大長度為255個位元組。

特殊字元會自動以UTF-8編碼。 例如，如果相關廣告的基礎URL為「http://www.example.com/」{param1} 和的關鍵字層級值 {param1} 為「shoes/flats.html」，則廣告會導向http://www.example.com/shoes%2Fflats.html。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
