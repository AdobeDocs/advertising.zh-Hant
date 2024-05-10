---
title: 關於Adobe Advertising轉換追蹤標籤
description: 瞭解如何使用Adobe Advertising轉換追蹤標籤。
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 關於Adobe Advertising轉換追蹤標籤

Adobe Advertising會使用Adobe Advertising轉換追蹤標籤(插入在轉換事件發生時開啟的網頁（例如「成功」頁面）來追蹤廣告點選所產生的轉換。 標籤包含內嵌資訊，可連同使用者的Adobe AdvertisingCookie傳送交易資料至追蹤伺服器，交易會從該伺服器計入適當的廣告點選數或曝光數（根據廣告商的轉換歸因設定）。

>[!NOTE]
>
>如果使用者沒有有效的Cookie，則Adobe Advertising不會報告轉換。

您必須針對要追蹤的每組轉換量度，建立個別的轉換標籤。 提供標籤給廣告商或代理商，並附上要插入每個標籤的網頁清單。 您可以產生下列任一型別的轉換標籤。 請參閱&quot;[產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)」以取得指示。

* （建議） JavaScript標籤（版本3或版本2），不會顯示在網頁中。

* HTML影像標籤以在網頁上顯示1畫素x 1畫素透明影像（畫素），一般使用者無法看到這些影像。 只有在公司有禁止使用JavaScript標籤的原則時，才使用影像標籤。

如需關於標籤型別之間差異的詳細資訊，請參閱&quot;[Advertising Cloud轉換追蹤標籤相關常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).」

>[!NOTE]
>
>* 此功能不會將影像標籤或JavaScript標籤新增到廣告商的網頁。 標籤必須根據廣告商更新網頁的正常程式進行新增。
>* 請務必考慮實作標籤所需的時間。 根據公司的政策，實作可能需要數週甚至數月。

## Adobe Advertising轉換追蹤標籤的功能

轉換追蹤畫素可讓Adobe Advertising執行下列動作：

* 追蹤和報告搜尋行銷活動關鍵字層級的轉換資料。

* 追蹤和報告所有行銷管道廣告（創意）層級的轉換資料（付費搜尋和顯示），這有助於創意測試。

* 追蹤和報告所有行銷管道交易層級的轉換資料。

* 顯示轉換在不同行銷管道中的分配方式，讓您瞭解哪些最有效。

* 報告並最佳化不同的歸因層級（例如將轉換歸因到最後一個相關事件，或平均加權所有事件）。

* 顯示點按協助（搜尋有助於轉換漏斗的關鍵字或位置）和管道協助（有助於轉換漏斗的使用者事件，可能橫跨多個行銷管道）。

* 提供網站流量和轉換之地理分佈和反向連結網域的可見度，因此您可以調整地理和網站目標定位。

* 分析一週中的某天或當天趨勢，這些趨勢可用來改善轉換率。

>[!MORELIKETHIS]
>
>* [轉換追蹤選項](conversion-tracking-about.md)
>* [產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript轉換追蹤標籤第3版的格式](format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤第2版的格式](format-conversion-tag-jsv2.md)
>* [影像轉換追蹤標籤的格式](format-conversion-tag-image.md)
>* [關於轉換和頁面檢視追蹤標籤的常見問題集](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe AdvertisingJavaScript轉換對應標籤](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
