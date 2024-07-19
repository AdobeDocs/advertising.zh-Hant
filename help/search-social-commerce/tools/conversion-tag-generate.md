---
title: 產生Adobe Advertising轉換追蹤標籤
description: 瞭解如何建立Adobe Advertising轉換標籤以追蹤您的轉換事件。
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# 產生Adobe Advertising轉換追蹤標籤

*僅追蹤Adobe Advertising轉換的廣告商*

為您要追蹤的每組量度建立個別的轉換標籤，並將標籤提供給廣告商或代理商，並提供要插入每組量度的網頁清單。

>[!NOTE]
>
>此功能不會將影像標籤或[!DNL JavaScript]標籤新增至廣告商的網頁。 標籤必須根據廣告商更新網頁的正常程式進行新增。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**。

1. 指定[轉換標籤設定](#conversion-tag-settings)。

1. 產生標籤：

   * 如果網站使用HTTP，請按一下&#x200B;**[!UICONTROL Generate Conversion Tag]**。

   * 如果網站在安全伺服器(HTTPS)上執行，請按一下&#x200B;**[!UICONTROL Generate Secure Conversion Tag]**。

1. 從對話方塊複製標籤，然後視需要將其貼到適當的網頁中。

>[!NOTE]
>
>新轉換標籤中的每個量度都會自動列在[!UICONTROL Admin] > [!UICONTROL Conversions]中，即使它未實作或它所位於的網頁未收到任何點按。 此行為不同於手動或其他方式建立之標籤中的量度行為，這些標籤不會列在[!UICONTROL Admin] > [!UICONTROL Conversions]中，直到其中一個網頁收到點按為止。 但在所有情況下，每個量度一開始都會從投資組合目標、報表和檢視中排除，直到您明確提供它們為止。 不過，在將量度新增至投資組合目標之前，請考慮先使量度可供使用，並將量度新增至報表，以驗證量度何時收到點按。

## Adobe Advertising轉換標籤設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：**&#x200B;要建立的標籤型別：

* *[!UICONTROL Image]：*&#x200B;若要建立影像標籤以在網頁上顯示1畫素x 1畫素透明影像（畫素），一般使用者無法看到該影像。 最佳實務是只有在網站有原則禁止使用JavaScript標籤時，才使用影像標籤。

* *[!UICONTROL JavaScript]：*&#x200B;若要建立JavaScript標籤。

如需標籤型別之間差異的詳細資訊，請參閱[有關Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。

**[!UICONTROL Tag Properties]：**&#x200B;當一般使用者檢視包含轉換標籤的頁面時，要追蹤的一或多個轉換量度。 若要新增量度至清單，請在&quot;[!UICONTROL Add new property]&quot;欄位中輸入量度名稱，然後按一下&#x200B;**[!UICONTROL Add]**。

追蹤多個量度時，標籤中的&amp;符號(`&`)會加入這些量度，例如`ev_Property1=<Property1>&ev_Property2=<Property2>`。

>[!NOTE]
>
>新增至此清單的量度未儲存於任何位置，或與[!UICONTROL Admin]標籤上使用者端的[!UICONTROL Conversions]清單整合。 不過，當Adobe Advertising實際收集量度的資料後，量度就會自動新增到使用者端的[!UICONTROL Conversions]清單中，當轉換標籤在頁面上實作，且一般使用者完成開啟該頁面的交易時，就會發生這種情況。

**[!UICONTROL Include unique transaction IDs]：** （選擇性）在標籤中包含交易ID屬性(`ev_transid=<transid>`)。 依預設，會選取選項。

選取此選項時，當交易完成時，廣告商必須產生`<transid>`的唯一值（例如實際訂單ID），並將其傳回Adobe Advertising，例如`ev_transid=0123`。 Adobe Advertising使用交易ID來消除具有相同交易ID和屬性值的重複交易。 交易ID不能包含保留為引數分隔符號的&amp;符號(`&`)。 交易ID包含在[的[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)中，您可以使用它來驗證Search、Social和Commerce中與廣告商資料相關的資料。

如果資料並未包含每個交易的唯一ID，則Adobe Advertising仍會根據交易時間產生唯一ID。

>[!NOTE]
>
>如果您傳送含有離線轉換轉換資料的[交易ID摘要](/help/search-social-commerce/tracking/feed-transaction-id.md)，則您必須針對交易離線部分的摘要資料中的線上部分提交交易ID (`ev_transid`)。

**[!UICONTROL Page is inside FB app]：**&#x200B;已過時

**[!UICONTROL Segment users]：**&#x200B;已過時

**[!UICONTROL JS Version]：** （僅限[!DNL JavaScript]個標籤）要建立的[!DNL JavaScript]標籤版本： *[!UICONTROL v2]* （預設）或&#x200B;*[!UICONTROL v3]*。

請參閱[有關Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。 以取得差異的詳細資訊。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [關於建立和解碼追蹤標籤的工具](tracking-tools-about.md)
>* 有關轉換和頁面檢視追蹤標籤的[常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript轉換追蹤標籤格式3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)版的格式
>* [影像轉換追蹤標籤的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe AdvertisingJavaScript轉換對應標籤](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [關於管理廣告商的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
