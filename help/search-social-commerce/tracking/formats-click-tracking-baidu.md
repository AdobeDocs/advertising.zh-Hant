---
title: 的點選追蹤格式 [!DNL Baidu]
description: 瞭解的點選追蹤格式 [!DNL Baidu] 帳戶。
exl-id: a57ff0cf-0bcf-4d55-9a86-7551db8a08e7
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# 上的贊助廣告的點選追蹤格式 [!DNL Baidu]

下列基本目的地URL格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `<campaignID>` 是數值促銷活動ID的變數。
>
>* `<the landing page>` 是變數，代表一般使用者要導向的網站URL。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID追蹤程式碼的格式](skwcid-tracking-parameter.md)
