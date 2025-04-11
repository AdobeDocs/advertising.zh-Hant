---
title: 將 [!DNL Analytics for Advertising] 巨集附加至 [!DNL Flashtalking] 廣告標籤
description: 瞭解為何以及如何將 [!DNL Analytics for Advertising] 巨集新增至您的 [!DNL Flashtalking] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e8c8316418acf4a8c62beabcae2c1b7388dbc297
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 將[!DNL Analytics for Advertising]巨集附加至[!DNL Flashtalking]廣告標籤

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*僅與[!DNL Flashtalking]沒有直接合夥關係的組織*

*僅適用於Advertising DSP*

如果您將[!DNL Flashtalking]中的廣告標籤用於Advertising DSP廣告，則必須將追蹤引數附加至登陸頁面URL。 若要與[!DNL Flashtalking]使用Advertising DSP合作關係，請將Advertising的Analytics引數附加至您的登陸頁面URL。 這些引數會在登陸頁面URL中記錄AMO ID (`s_kwcid`)和`ef_id`查詢字串引數，以允許Adobe Advertising將廣告的點選資料傳送至Adobe Analytics。

>[!NOTE]
>
>如果您的組織與[!DNL Flashtalking]有直接的合作關係，則您不需要執行此程式。 請改為登入您的[!DNL Flashtalking]帳戶並遵循[!DNL Flashtalking]支援檔案，在`https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`使用資料傳遞巨集來收集點選資料。

針對下列型別的[!DNL Analytics for Advertising]實作，[!DNL Flashtalking]顯示廣告和視訊廣告使用巨集：

* **在其網站上實作[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript程式碼的廣告商**： JavaScript程式碼已記錄AMO ID (`s_kwcid`)和`ef_id`查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤功能，加入點按式轉換。 最佳實務是將下列區段中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

  >[!NOTE]
  >
  >JavaScript程式碼是僅在Cookie仍可用時用於點選追蹤的解決方案。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用[!DNL Analytics for Advertising] JavaScript程式碼，而是僅仰賴[!DNL Analytics]伺服器端轉送來取得點進資料的廣告商** （不含任何檢視資料）：若要報告您透過Adobe Advertising購買的廣告所驅動的站上點進活動，必須有下列巨集。

## 顯示廣告標籤

在[!DNL Flashtalking]廣告標籤設定中，將下列巨集附加至`Clicktag`欄位中的點進URL結尾：

```
[ftqs:[AdobeAMO]]
```

如果它是基礎URL之後的第一個或唯一查詢字串，則使用`?`將其與基礎URL分開。 如果基底URL包含多個查詢字串，則第一個字串的開頭為`?`，而每個後續字串的開頭為`&`。

範例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## 影片廣告標籤

在[!DNL Flashtalking]廣告標籤設定中，將下列巨集附加至`Clicktag`欄位中的點進URL結尾：

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

如果它是基礎URL之後的第一個或唯一查詢字串，則使用`?`將其與基礎URL分開。 如果基底URL包含多個查詢字串，則第一個字串的開頭為`?`，而每個後續字串的開頭為`&`。

範例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [個Adobe Advertising ID已由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

