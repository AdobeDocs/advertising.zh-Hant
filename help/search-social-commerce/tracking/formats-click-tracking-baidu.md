---
title: ' [!DNL Baidu]的點選追蹤格式'
description: 瞭解 [!DNL Baidu] 帳戶的點選追蹤格式。
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# [!DNL Baidu]上贊助廣告的點選追蹤格式

下列基本目的地URL格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `<campaignID>`是數值促銷活動ID的變數。
>
>* `<the landing page>`是變數，代表一般使用者在網站上導向的URL。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
