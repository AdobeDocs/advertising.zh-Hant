---
title: ' [!DNL Yahoo! Japan Ads]的點選追蹤格式'
description: 瞭解 [!DNL Yahoo! Japan Ads] 帳戶的點選追蹤格式。
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '100'
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
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `<the landing page>`是變數，代表一般使用者在網站上導向的URL。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
