---
title: 影像轉換追蹤標籤的格式
description: 參考影像轉換追蹤標籤的格式。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 影像轉換追蹤標籤的格式

>[!NOTE]
>
>如需關於何時使用影像標籤與JavaScript標籤的詳細資訊，請參閱 [有關追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* 具有HTTP的網站的非安全標籤：

   ```
   <img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>
   ```

* 使用HTTPS的網站的安全標籤：

   ```
   <img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>
   ```

其中：

* `<ef-userid>` 是Search、Social和Commerce指派給廣告商的不重複數值使用者ID。

* `<propertyname>` 是要追蹤的轉換。 例如，如果您追蹤的轉換稱為「註冊」，則標籤會包含引數 `ev_registration=<registration>`，而且您必須傳遞每個交易的實際收入(例如 `ev_registration=1`)。 追蹤多個屬性時，系統會使用&amp;符號(`&`)，例如 `ev_registration=<registration>&ev_sale=<sale>` (例如， `ev_registration=1&ev_sale=12.99`)。 **注意：**  屬性名稱不得包含特殊字元。

* `<transid>` 是廣告商產生並傳遞的唯一交易ID （例如實際訂單ID），用於識別交易。 只有在「[!UICONTROL Include unique transaction IDs]「 」選項已選取。

   Search， Social， &amp; Commerce會使用交易ID來消除具有相同交易ID和屬性值的重複交易。 交易ID包含在 [!UICONTROL Transaction Report]，可用來使用廣告商的資料驗證Adobe廣告中的資料。 **注意：** 如果廣告商的資料並未包含每個交易的唯一ID，則Search、Social和Commerce仍會根據交易時間產生唯一ID。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [產生Adobe廣告轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [關於轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript轉換追蹤標籤第2版的格式](format-conversion-tag-jsv2.md)
>* [JavaScript轉換追蹤標籤第3版的格式](format-conversion-tag-jsv3.md)

