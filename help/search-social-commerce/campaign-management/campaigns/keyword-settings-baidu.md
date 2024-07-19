---
title: '[!DNL Baidu]關鍵字設定'
description: 參考 [!DNL Baidu] 關鍵字的設定。
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu]關鍵字設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;關鍵字。 每個關鍵字的長度上限為30個單位元組或15個雙位元組字元

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。 使用下列語法：

* 廣泛比對為`keyword`
* `"keyword"`為字詞相符
* `[keyword]`以取得完全相符

>[!NOTE]
>
>* [!DNL Baidu]僅允許每個廣告群組的每個關鍵字有一個符合型別。 例如，廣告群組1不能同時包含`"keyword"`和`[keyword]`。
>* 您可以從[!UICONTROL Keywords] > [!UICONTROL Negatives]檢視並在廣告群組和行銷活動設定中建立負面關鍵字。
>* 變更[!DNL Baidu]關鍵字會刪除現有關鍵字，並建立具有新關鍵字識別碼的新關鍵字。 但是，變更相符型別並不會刪除現有的關鍵字。

**[!UICONTROL Status]：**&#x200B;關鍵字的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新關鍵字的預設值為&#x200B;*Active*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL選項

**[!UICONTROL Base URL]：** （僅具有關鍵字層級追蹤的行銷活動；選用）使用者按一下您的廣告時所前往的登陸頁面URL。 其中可能包括
協力廠商重新導向和追蹤程式碼。 如果您輸入值，該值會覆寫廣告的基本URL。

儲存記錄後，基本URL會包含為促銷活動或帳戶設定的任何附加引數。

如果您使用Adobe Advertising轉換追蹤服務，且行銷活動設定包含使用[!UICONTROL EF Redirect]和在關鍵字層級新增追蹤，則Search、Social和Commerce會自動新增自己的點選追蹤代碼。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
