---
title: '"[!DNL Baidu] 關鍵字設定」'
description: 參考設定 [!DNL Baidu] 關鍵字。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] 關鍵字設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字。 每個關鍵字的最大長度是30個單位元組或15個雙位元組字元

您最多可以輸入或貼上2000個關鍵字。 以逗號分隔多個關鍵字，或在不同的行中輸入關鍵字。 使用下列語法：

* `keyword` 廣泛匹配
* `"keyword"` 用於短語比對
* `[keyword]` 以取得完全相符

>[!NOTE]
>
>* [!DNL Baidu] 每個廣告群組的每個關鍵字僅允許一個符合型別。 例如，廣告群組1不能同時包含兩者 `"keyword"` 和 `[keyword]`.
>* 您可以從以下位置建立負關鍵字： [!UICONTROL Keywords] > [!UICONTROL Negatives] 在廣告群組和行銷活動設定中檢視和。
>* 變更 [!DNL Baidu] 關鍵字會刪除現有關鍵字，並使用新關鍵字ID建立新關鍵字。 但是，變更相符型別並不會刪除現有關鍵字。


**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL選項

**[!UICONTROL Base URL]：** （僅限具有關鍵字層級追蹤的促銷活動；選用）使用者按一下您的廣告時，被帶往的登陸頁面URL。 其中可包含協力廠商重新導向和追蹤程式碼。 如果您輸入值，該值會覆寫廣告的基本URL。

儲存記錄後，基本URL會包含為行銷活動或帳戶設定的任何附加引數。

如果您使用Adobe廣告轉換追蹤服務，且行銷活動設定包含使用 [!UICONTROL EF Redirect] 和在關鍵字層級新增追蹤，則Search、Social和Commerce會自動新增自己的點選追蹤程式碼。

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

