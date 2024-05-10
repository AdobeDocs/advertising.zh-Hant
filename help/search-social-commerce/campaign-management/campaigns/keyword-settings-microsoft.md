---
title: 『[!DNL Microsoft Advertising] 關鍵字設定
description: 參考設定 [!DNL Microsoft Advertising] 關鍵字。
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 關鍵字設定

您可以為使用搜尋和顯示網路的行銷活動建立關鍵字。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 關鍵字，包括任何 [!DNL Microsoft Advertising] 比對語法和預留位置。 每個關鍵字的長度上限為100個字元。

您最多可以輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

>[!NOTE]
>
>* 您可以從以下位置建立負關鍵字： [!UICONTROL Keywords] > [!UICONTROL Negatives] 在廣告群組和促銷活動設定中檢視和。
>* 變更 [!DNL Microsoft Advertising] 關鍵字會刪除現有關鍵字，並使用新的關鍵字ID建立新關鍵字。 但是，變更相符型別並不會刪除現有的關鍵字。

**[!UICONTROL Status]：** 關鍵字的顯示狀態： *作用中* 或 *已暫停*. 新關鍵字的預設值為 *作用中*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 預留位置

**[!UICONTROL Param2]：** 如果關鍵字的基本URL或廣告的標題、說明或基本URL包含 [此 `{Param2}` 動態替代字串](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 長度上限為70個字元，但請注意，您使用廣告元素的最大長度限制（例如，標題1和標題2的合併長度上限為76個字元）。

**[!UICONTROL Param3]：** 如果關鍵字的基本URL或廣告的標題、說明或基本URL包含 [此 `{Param3}` 動態替代字串](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 長度上限為70個字元，但請注意，您使用廣告元素的最大長度限制（例如，標題1和標題2的合併長度上限為76個字元）。

## URL選項

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

此欄位可選擇性包含 `{Param2}` 和 `{Param3}` 動態替代變數。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
