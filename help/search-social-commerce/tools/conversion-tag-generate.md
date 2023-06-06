---
title: 產生Adobe廣告轉換追蹤標籤
description: 瞭解如何建立Adobe廣告轉換標籤以追蹤您的轉換事件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# 產生Adobe廣告轉換追蹤標籤

*僅具有Adobe廣告轉換追蹤的廣告商*

為您要追蹤的每組量度建立個別的轉換標籤，並為廣告商或機構提供要插入每組量度的網頁清單。

>[!NOTE]
>
>此功能不會新增影像標籤或 [!DNL JavaScript] 標籤貼到廣告商的網頁。 標籤必須根據廣告商更新網頁的正常程式新增。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. 指定 [轉換標籤設定](#conversion-tag-settings).

1. 產生標籤：

   * 如果網站使用HTTP，然後按一下 **[!UICONTROL Generate Conversion Tag]**.

   * 如果網站在安全伺服器(HTTPS)上執行，則按一下 **[!UICONTROL Generate Secure Conversion Tag]**.

1. 從對話方塊複製標籤，然後視需要將其貼到適當的網頁中。

>[!NOTE]
>
>新轉換標籤中的每個量度都會自動列在 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]，即使未實作或所在的網頁未收到任何點按。 此行為與手動或其他位置建立之標籤中的量度行為不同，這些標籤未列於 [!UICONTROL Admin] > [!UICONTROL Transaction Properties] 直到其中一個網頁收到點按為止。 但在所有情況下，每個量度最初都會從投資組合目標、報表和檢視中排除，直到您明確提供它們為止。 不過，在將量度新增至投資組合目標之前，請先考慮讓量度可供使用，並將它們新增至報表，以驗證它們何時收到點按。

## Adobe廣告轉換標籤設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：** 要建立的標籤型別：

* *[!UICONTROL Image]：* 建立影像標籤以在網頁上顯示1畫素x 1畫素的透明影像（畫素），一般使用者無法看到該影像。 最佳實務是只有在網站有禁止使用JavaScript標籤的原則時，才使用影像標籤。

* *[!UICONTROL JavaScript]：* 建立JavaScript標籤。

如需標籤型別之間差異的詳細資訊，請參閱&quot;[關於Adobe廣告轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).」

**[!UICONTROL Tag Properties]：** 當一般使用者檢視包含轉換標籤的頁面時要追蹤的一或多個交易屬性（量度）。 若要將量度新增至清單，請在「」中輸入量度名稱[!UICONTROL Add new property]」欄位並按一下 **[!UICONTROL Add]**.

追蹤多個量度時，會使用&amp;符號(`&`)，例如 `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>新增至此清單的量度不會儲存在任何地方，也不會與客戶的 [!UICONTROL Transaction Properties] 清單于 [!UICONTROL Admin] 標籤。 不過，量度會新增至使用者端的 [!UICONTROL Transaction Properties] 當Adobe廣告實際收集量度的資料時自動列出，當轉換標籤在頁面上實作，且一般使用者完成開啟該頁面的交易時，就會發生這種情況。

**[!UICONTROL Include unique transaction IDs]：** （選用）包含交易ID屬性(`ev_transid=<transid>`)。 依預設，會選取選項。

選取此選項時，廣告商必須產生唯一值 `<transid>` （例如，實際訂單ID）交易完成時傳回Adobe廣告，例如 `ev_transid=0123`. Adobe廣告會使用交易ID來消除具有相同交易ID和屬性值的重複交易。 交易ID不可包含&amp;符號(`&`)，此引數會保留為引數分隔符號。 交易ID包含在 [此 [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)，可用來使用廣告商的資料驗證Search、Social和Commerce中的資料。

如果資料並未包含每個交易的唯一ID，則Adobe廣告仍會根據交易時間產生唯一ID。

>[!NOTE]
>
>如果您傳送 [交易識別碼摘要](/help/search-social-commerce/tracking/feed-transaction-id.md) 離線轉換的轉換資料中，您必須提交交易ID (`ev_transid`)時，若為交易離線部分的摘要資料，則為交易的線上部分。

**[!UICONTROL Page is inside FB app]：** 已過時

**[!UICONTROL Segment users]：** 已過時

**[!UICONTROL JS Version]：** ([!DNL JavaScript] 僅限標籤)的哪個版本 [!DNL JavaScript] 標籤以建立： *[!UICONTROL v2]* （預設）或 *[!UICONTROL v3]*.

請參閱「[關於Adobe廣告轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).」 以取得差異的詳細資訊。

>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [關於建立和解碼追蹤標籤的工具](tracking-tools-about.md)
>* [關於轉換和頁面檢視追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript轉換追蹤標籤第3版的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤第2版的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [影像轉換追蹤標籤的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe廣告JavaScript轉換對應標籤](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [關於管理廣告商的交易屬性](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)

