---
title: 產生點選追蹤URL
description: 瞭解如何手動產生搜尋、社交和Commerce點選追蹤URL。
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 使用追蹤URL工具產生搜尋、社交和Commerce點選追蹤URL

*僅追蹤Adobe Advertising轉換的廣告商*

如需關於何時必須手動產生及實作點選追蹤URL的資訊，請參閱[何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)。

>[!NOTE]
>
>此功能未在相關廣告帳戶中實作追蹤範本或目的地URL。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**。

1. 從清單中選取廣告網路帳戶。

   （[!DNL Google Ads]個關鍵字；文字、行動應用程式安裝及動態搜尋廣告；位置；網站連結；及產品群組）會顯示追蹤範本欄位的追蹤標籤。 它們不包含任何帳戶層級的附加引數。 跳至步驟4。

   對於所有其他型別的標籤，輸入資訊以產生標籤。

1. （如有必要）產生標籤：

   1. 以下列其中一種方式指定登入頁面，並在請求時提供網站連結或產品名稱：

      * 輸入完整路徑和檔案名稱，或按一下&#x200B;**[!UICONTROL Browse]**&#x200B;在您的裝置或網路上尋找檔案，以指定包含資訊的檔案。 檔案必須是以Tab分隔的文字檔案，每行有一個專案，格式如下：

         * （創意內容，標準廣告） `**landing_page**`

           其中`landing_page`為有效的登陸頁面URL或基底URL。

           範例： http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising]個網站連結） `sitelink <tab> ** <tab> landing_page`

           其中`sitelink`是網站連結名稱，`landing_page`是有效的登陸頁面URL或基底URL。

           範例： `Careers <tab> ** <tab> http://www.example.com/careers.html`

           檔案最多可包含10,000行。

         * （[!DNL Google Merchant Center]產品群組和[!DNL Microsoft Advertising]產品廣告） `product name <tab> ** <tab> landing_page`

           其中`product name`是產品名稱，`landing_page`是有效的登陸頁面URL或基底URL。

           範例： `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           檔案最多可包含10,000行。

      * 在輸入欄位中，以下列格式每行輸入一個專案：

         * （創意內容，標準廣告） `landing_page`

           其中`landing_page`為有效的登陸頁面URL或基底URL。

           範例： http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising]個網站連結） `sitelink**landing_page`

           其中`sitelink`是網站連結名稱，`landing_page`是有效的登陸頁面URL或基底URL。

           範例： `Careers**http://www.example.com/careers.html`

         * （[!DNL Google Merchant Center]產品群組和[!DNL Microsoft Advertising]產品廣告） `product name**landing_page`

           其中`product name`是產品名稱，`landing_page`是有效的登陸頁面URL或基底URL。

           範例： Acme PR208**http://www.example.com/travel.html

   1. 按一下&#x200B;**[!UICONTROL Generate Tracking URLs]**。

1. （選用）從畫面或輸出頁面複製URL （以「http」或「https」開頭），並在搜尋或社交帳戶中實作URL。

對於具有目的地URL的帳戶，請在適當的[!UICONTROL Base URL]欄位中輸入值。

對於具有最終URL的帳戶，請在適當的[!UICONTROL Tracking Template]欄位中輸入熒幕上的值。 您必須在`&url=`引數（例如`{lpurl}`）之後新增最終URL的引數。 對於[!DNL Yahoo! Japan Ads]帳戶，請使用引數`{lpurl}`。 如需表示追蹤範本中最終URL的[!DNL Google Ads]和[!DNL Microsoft Advertising]引數清單，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348) （請參閱「可用的[!DNL ValueTrack]引數」一節中的「僅限追蹤範本」引數）和[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799/2)。

>[!MORELIKETHIS]
>
>* [關於建立和解碼追蹤標籤的工具](tracking-tools-about.md)
>* [何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [解碼搜尋、社交和Commerce點選追蹤URL](click-tracking-url-decode.md)
