---
title: 的點選追蹤格式 [!DNL Yahoo! Display Network]
description: 瞭解的點選追蹤格式 [!DNL Yahoo! Display Network] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 贊助廣告的點選追蹤格式於 [!DNL Yahoo! Display Network]

下列基本目的地UR格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe廣告中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `<the landing page>` 是變數，代表一般使用者在網站上被導向的URL。


>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [s\_kwcid追蹤程式碼的格式](skwcid-tracking-parameter.md)

