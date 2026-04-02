---
title: 關於搜尋、社交和Commerce的追蹤
description: 瞭解搜尋、社交和Commerce的追蹤選項。
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/IpPgzsMgRsOCmLv3dyEKBp4EPQwgN90UkVIQy9SaXB8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# 關於搜尋、社交和Commerce的追蹤

若要追蹤廣告成效，搜尋、Social和Commerce需要廣告的曝光數、點選數、成本和轉換（交易）資料。 搜尋、Social和Commerce會使用這些資料來建立所需的資料預測模型，以便最佳化您的廣告組合。

## 成本、點選次數和曝光資料

搜尋、Social和Commerce每天會直接從[支援的廣告網路](/help/search-social-commerce/introduction/supported-inventory.md)擷取印象、點選和成本資料。 此外，搜尋、Social和Commerce可以在您的追蹤範本和目的地URL中新增唯一的點選追蹤程式碼（包括重新導向至追蹤伺服器），以追蹤顯示/內容曝光數、點選次數和成本，並在稍後將事件與轉換相關聯。

如果您想要在Search、Social和Commerce未同步資料的廣告網路上追蹤促銷活動，則您必須傳送包含曝光、點選和成本資料的每日摘要檔案，以便提供這些促銷活動的資料。

### 點選追蹤標籤

您的搜尋、Social和Commerce實作團隊會在您的同步廣告行銷活動中更新廣告、關鍵字、位置、產品群組和Sitelink擴充功能的追蹤範本和目的地URL，以包含唯一的追蹤ID字串和Adobe Advertising重新導向，藉此設定點選追蹤。 此外也會將追蹤新增至您[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶與行銷活動的登入頁面尾碼（最終URL尾碼）。

追蹤引數可讓Adobe Advertising追蹤個別關鍵字層級（搜尋行銷活動）或廣告變數層級（具有內容或網站目標定位的搜尋行銷活動、顯示行銷活動以及社交行銷活動）的點按。 每當使用者檢視顯示/內容廣告或按一下您的其中一個廣告時，廣告網路就會使用與關鍵字或廣告相關聯的點選追蹤標籤，將事件傳送至Adobe Advertising畫素伺服器。 若為點按：

* 針對支援平行追蹤的瀏覽器上的[!DNL Google Ads]和[!DNL Microsoft Advertising]廣告，廣告網路會先將點按傳送至您的網站，然後再傳送至Adobe Advertising畫素伺服器，接著再將Cookie放在使用者的電腦上（如果尚未存在）。

* 在所有其他情況下，廣告網路會直接將點按傳送至Adobe Advertising畫素伺服器。 畫素伺服器會將Cookie放在使用者的電腦上（如果沒有），然後將使用者重新導向至您網站上的相關URL。 一般使用者的整體體驗，與沒有重新導向時相同。

Cookie在[!DNL Adobe]網域(`everesttech.net`)中設定為第一方Cookie。 重新導向後，使用者位在廣告商的網域上，接著系統會將此Cookie視為第三方Cookie。 如需Adobe Advertising Cookie的詳細資訊，請參閱&quot;[Adobe Advertising Cookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html)&quot;。

## 轉換資料

當客戶點按廣告或檢視顯示或社交廣告時，Search、Social和Commerce需要將每個產生的轉換對應回原始點按或顯示/社交印象。

廣告商負責提供所有點按和顯示/社交印象的轉換資料。 轉換資料可包含網站上發生且可用於競標最佳化的任何型別事件的相關資訊。 您可以在廣告商的轉換頁面（例如在客戶完成交易後顯示的「成功」頁面）中實作轉換追蹤代碼，或是傳送包含其他方法擷取的轉換資料的每日摘要檔案，以提供轉換資料。

### 轉換追蹤標籤

您可以使用不同廠商的[轉換標籤](/help/search-social-commerce/tracking/conversion-tracking-about.md)。

當您使用Adobe Advertising轉換標籤且使用者完成成功交易並登陸「成功」頁面時，Adobe Advertising畫素伺服器會檢查使用者電腦上是否存在Cookie （于點選重新導向時設定）。 當找到Cookie時，會使用ef_transid引數傳遞交易事件的相關資訊，而交易會辨識為轉換，並會將其點按計入前一個廣告或顯示曝光中。

如果使用者點按了您的多個廣告，Adobe Advertising會將交易歸因於最終廣告點按，或（針對顯示或影片行銷活動）最終廣告曝光，除非您另有指定。 您的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)會決定付費點按或顯示/視訊曝光（分別）發生後，事件可歸因於轉換的天數。

Adobe Advertising實作團隊會與廣告商合作，決定廣告商需要實作的轉換標籤格式，識別應插入每個轉換標籤的網頁，然後提供要實作的轉換標籤。
