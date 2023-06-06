---
title: 關於Adobe廣告轉換追蹤標籤
description: 瞭解如何使用Adobe廣告轉換追蹤標籤。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 關於Adobe廣告轉換追蹤標籤

「Adobe廣告」會使用「Adobe廣告」轉換追蹤標籤（插入在發生轉換事件時開啟的網頁中，例如「成功」頁面），追蹤因廣告點按而產生的轉換。 標籤包含內嵌資訊，可連同使用者的Adobe廣告Cookie將交易資料傳送至追蹤伺服器，交易會從中計入適當的廣告點選數或曝光數（根據廣告商的轉換歸因設定）。

>[!NOTE]
>
>如果使用者沒有有效的Cookie，則Adobe廣告不會報告轉換。

您必須針對要追蹤的每組轉換量度，建立個別的轉換標籤。 將標籤提供給廣告商或代理商，並提供要插入每個標籤的網頁清單。 您可以產生下列任一型別的轉換標籤。 請參閱「[產生Adobe廣告轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)」以取得指示。

* （建議使用） JavaScript標籤（版本3或版本2），這些標籤不會顯示在網頁中。

* HTML影像標籤以在網頁上顯示1畫素x 1畫素的透明影像（畫素），一般使用者無法看到這些影像。 只有當公司有禁止使用JavaScript標籤的原則時，才使用影像標籤。

如需標籤型別之間差異的詳細資訊，請參閱&quot;[Advertising Cloud轉換追蹤標籤的常見問題集](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).」

>[!NOTE]
>
>* 此功能不會將影像標籤或JavaScript標籤新增至廣告商的網頁。 標籤必須根據廣告商更新網頁的正常程式新增。
>* 請務必考慮實作標籤所需的時間。 根據公司的政策，實作可能需要數週甚至數月。


## Adobe廣告轉換追蹤標籤的功能

轉換追蹤畫素可讓Adobe廣告執行下列動作：

* 追蹤和報告搜尋行銷活動之關鍵字層級的轉換資料。

* 跨所有行銷管道（付費搜尋和顯示）在廣告（創意）層級追蹤和報告轉換資料，這可以促進創意測試。

* 追蹤和報告所有行銷管道交易層級的轉換資料。

* 顯示您的轉換如何分佈在不同行銷管道，以便檢視哪個管道最有效。

* 報告並最佳化不同的歸因層級（例如將轉換歸因到最後一個相關事件，或平均加權所有事件）。

* 提供點按協助（搜尋對轉換漏斗有貢獻的關鍵字或位置）和管道協助（對轉換漏斗有貢獻的使用者事件，可能跨多個行銷管道）的可見度。

* 提供網站流量和轉換的地理分佈和反向連結網域的可見度，以便您調整地理和網站目標定位。

* 分析星期幾或當天趨勢，這些趨勢可用來改善轉換率。

>[!MORELIKETHIS]
>
>* [轉換追蹤選項](conversion-tracking-about.md)
>* [產生Adobe廣告轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript轉換追蹤標籤第3版的格式](format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤第2版的格式](format-conversion-tag-jsv2.md)
>* [影像轉換追蹤標籤的格式](format-conversion-tag-image.md)
>* [關於轉換和頁面檢視追蹤標籤的常見問題集](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe廣告JavaScript轉換對應標籤](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

