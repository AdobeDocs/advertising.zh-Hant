---
title: 『[!DNL Baidu] 關鍵字設定
description: 參考設定 [!DNL Baidu] 關鍵字。
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] 關鍵字設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字。 每個關鍵字的長度上限為30個單位元組或15個雙位元組字元

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。 使用下列語法：

* `keyword` 廣泛匹配
* `"keyword"` 用於短語比對
* `[keyword]` 以取得完全相符

>[!NOTE]
>
>* [!DNL Baidu] 每個廣告群組的每個關鍵字只允許一個符合型別。 例如，廣告群組1不能同時包含兩者 `"keyword"` 和 `[keyword]`.
>* 您可以從以下位置建立負關鍵字： [!UICONTROL Keywords] > [!UICONTROL Negatives] 在廣告群組和促銷活動設定中檢視和。
>* 變更 [!DNL Baidu] 關鍵字會刪除現有關鍵字，並使用新的關鍵字ID建立新關鍵字。 但是，變更相符型別並不會刪除現有的關鍵字。

**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL選項

**[!UICONTROL Base URL]：** （僅限具有關鍵字層級追蹤的促銷活動；選用）使用者按一下您的廣告時所前往的登陸頁面URL。 其中可能包含協力廠商重新導向和追蹤程式碼。 如果您輸入值，該值會覆寫廣告的基本URL。

儲存記錄後，基本URL會包含為促銷活動或帳戶設定的任何附加引數。

如果您使用Adobe Advertising轉換追蹤服務，且行銷活動設定包含使用 [!UICONTROL EF Redirect] 以及在關鍵字層級新增追蹤，則Search、Social和Commerce會自動新增自己的點選追蹤程式碼。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
