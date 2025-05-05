---
title: 影像轉換追蹤標籤的格式
description: 參考影像轉換追蹤標籤的格式。
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 影像轉換追蹤標籤的格式

>[!NOTE]
>
>如需關於何時使用影像標籤與JavaScript標籤的詳細資訊，請參閱追蹤標籤[&#128279;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)上的常見問題集。

* 具有HTTP的網站的不安全標籤：

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* 使用HTTPS的網站的安全標籤：

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

其中：

* `<ef-userid>`是Search、Social和Commerce指派給廣告商的不重複數值使用者ID。

* `<propertyname>`是要追蹤的轉換。 例如，如果您正在追蹤稱為「註冊」的轉換，則標籤會包含引數`ev_registration=<registration>`，而且您必須傳遞每個交易的實際收入（例如`ev_registration=1`）。 追蹤多個屬性時，它們會以&amp;符號(`&`)聯結，例如`ev_registration=<registration>&ev_sale=<sale>` （例如`ev_registration=1&ev_sale=12.99`）。 **注意：**&#x200B;屬性名稱不可包含特殊字元。

* `<transid>`是廣告商產生並傳遞以識別交易的唯一交易ID （例如實際訂單ID）。 只有在選取&quot;[!UICONTROL Include unique transaction IDs]&quot;選項時才會包含它。

  搜尋、Social和Commerce會使用交易ID來消除具有相同交易ID和屬性值的重複交易。 交易ID包含在[!UICONTROL Transaction Report]中，您可以使用它來驗證包含廣告商資料的Adobe Advertising中的資料。 **注意：**&#x200B;如果廣告商的資料並未包含每個交易的唯一ID，則Search、Social和Commerce仍會根據交易時間產生一個ID。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* 有關轉換和頁面檢視追蹤標籤的[常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript轉換追蹤標籤2](format-conversion-tag-jsv2.md)版的格式
>* [JavaScript轉換追蹤標籤格式3](format-conversion-tag-jsv3.md)
