---
title: ' [!DNL Yahoo! Japan Ads]的點選追蹤格式'
description: 瞭解 [!DNL Yahoo! Japan Ads] 帳戶的點選追蹤格式。
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ZFNzA0bfxKhlNW6fvPWMwBc4naT7rOhvym-wSpxvYXg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# [!DNL Yahoo! Japan Ads]上贊助廣告的點選追蹤格式

下列基本追蹤範本格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

或者，當在[!DNL Yahoo! Japan Ads]中為帳戶設定自動標籤選項時：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`cq?`之後以`<advertiser_ID>`取代`c?`。
>
>* `<the landing page>`是變數，代表一般使用者在網站上導向的URL。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
