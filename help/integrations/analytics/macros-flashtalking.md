---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤
description: 瞭解新增原因和方法 [!DNL Analytics for Advertising] 將巨集新增至 [!DNL Flashtalking] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: c6a7d99875d54d7ff807f94b8fdd7a903c05b6e5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*僅適用於Advertising DSP*

如果您使用的廣告標籤來自 [!DNL Flashtalking] 若為Advertising DSP廣告，請將Analytics for Advertising引數附加至登陸頁面URL。 引數會記錄AMO ID (`s_kwcid`)和 `ef_id` 登陸頁面URL中的查詢字串引數，可讓Adobe Advertising將廣告的點選資料傳送至Adobe Analytics。

將巨集用於 [!DNL Flashtalking] 下列型別的顯示廣告和視訊廣告 [!DNL Analytics for Advertising] 實作：

* **使用「 」的廣告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**：JavaScript程式碼已記錄AMO ID (`s_kwcid`)和 `ef_id` 查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤功能，加入點按式轉換。 最佳作法是將下列章節中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是一種解決方案，僅適用於Cookie仍可用時的點選追蹤。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用的廣告商 [!DNL Analytics for Advertising] JavaScript程式碼，並仰賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （不含任何瀏覽資料）：報告您透過Adobe Advertising購買的廣告所驅動的站上點選活動時，需要下列巨集。

## 顯示廣告標籤

在 [!DNL Flashtalking] 新增標籤設定，將下列巨集附加至中的點進URL結尾 `Clicktag` 欄位：

```
[ftqs:[AdobeAMO]]
```

如果它是基礎URL之後的第一個或唯一查詢字串，請使用將其與基礎URL分開 `?`. 如果基礎URL將包含多個查詢字串，則第一個字串的開頭為 `?` 以及每個後續的字串，都包含 `&`.

範例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## 影片廣告標籤

在 [!DNL Flashtalking] 新增標籤設定，將下列巨集附加至中的點進URL結尾 `Clicktag` 欄位：

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

如果它是基礎URL之後的第一個或唯一查詢字串，請使用將其與基礎URL分開 `?`. 如果基礎URL將包含多個查詢字串，則第一個字串的開頭為 `?` 以及每個後續的字串，都包含 `&`.

範例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

