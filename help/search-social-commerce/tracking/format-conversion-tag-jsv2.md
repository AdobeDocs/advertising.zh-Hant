---
title: JavaScript轉換追蹤標籤第2版的格式
description: 參考JavaScript轉換追蹤標籤第2版的格式。
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# JavaScript轉換追蹤標籤第2版的格式

以下格式適用於使用HTTPS的網站。 對於使用HTTP的網站，URL應該以「http」開頭。

>[!NOTE]
>
>如需何時使用版本2與版本3的相關資訊，請參閱追蹤標籤[&#128279;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)上的常見問題集。

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<ID5_PartnerID>
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

* `<ef-userid>`是Search、Social和Commerce指派給廣告商的不重複數值使用者ID。

* `<ID5_PartnerID>`是組織的ID5合作夥伴識別碼，組織會在與[!DNL ID5]簽署合約後收到此識別碼。 只有當組織使用DSP且有[個自訂區段追蹤與ID5通用ID](/help/dsp/audiences/universal-ids.md)相關聯的使用者時，才包含此變數。

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
>* [影像轉換追蹤標籤的格式](format-conversion-tag-image.md)
