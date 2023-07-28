---
title: JavaScript轉換追蹤標籤第2版的格式
description: 參考JavaScript轉換追蹤標籤第2版的格式。
exl-id: c4845694-10ac-41f8-bafb-ca813e42d190
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# JavaScript轉換追蹤標籤第2版的格式

以下格式適用於使用HTTPS的網站。 對於使用HTTP的網站，URL應該以「http」開頭。

>[!NOTE]
>
>如需關於何時使用版本2與版本3的資訊，請參閱 [追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

其中：

* `<ef-userid>` 是Search、Social和Commerce指派給廣告商的不重複數值使用者ID。

* `<propertyname>` 是要追蹤的轉換。 例如，如果您追蹤的轉換稱為「註冊」，則標籤會包含引數 `ev_registration=<registration>`，而且您必須傳遞每個交易的實際收入(例如 `ev_registration=1`)。 追蹤多個屬性時，系統會使用&amp;符號(`&`)，例如 `ev_registration=<registration>&ev_sale=<sale>` (例如， `ev_registration=1&ev_sale=12.99`)。 **注意：**  屬性名稱不得包含特殊字元。

* `<transid>` 是廣告商產生並傳遞以識別交易的唯一交易ID （例如實際訂單ID）。 只有當&quot;[!UICONTROL Include unique transaction IDs]已選取「 」選項。

  搜尋、Social和Commerce會使用交易ID來消除具有相同交易ID和屬性值的重複交易。 交易ID包含在 [!UICONTROL Transaction Report]，可用來使用廣告商的資料驗證Adobe Advertising中的資料。 **注意：** 如果廣告商的資料並未包含每個交易的唯一ID，則Search、Social和Commerce仍會根據交易時間產生唯一ID。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [關於轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript轉換追蹤標籤第2版的格式](format-conversion-tag-jsv2.md)
>* [JavaScript轉換追蹤標籤第3版的格式](format-conversion-tag-jsv3.md)
>* [影像轉換追蹤標籤的格式](format-conversion-tag-image.md)
