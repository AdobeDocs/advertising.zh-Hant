---
title: 的點選追蹤格式 [!DNL Baidu]
description: 瞭解的點選追蹤格式 [!DNL Baidu] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# 贊助廣告的點選追蹤格式於 [!DNL Baidu]

下列基本目的地UR格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe廣告中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `<campaignID>` 是數值促銷活動ID的變數。
>
>* `<the landing page>` 是變數，代表一般使用者在網站上被導向的URL。


>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [s\_kwcid追蹤程式碼的格式](skwcid-tracking-parameter.md)

