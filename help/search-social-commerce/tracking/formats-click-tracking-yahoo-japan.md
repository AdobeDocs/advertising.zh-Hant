---
title: 的點選追蹤格式 [!DNL Yahoo! Japan Ads]
description: 瞭解的點選追蹤格式 [!DNL Yahoo! Japan Ads] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 贊助廣告的點選追蹤格式於 [!DNL Yahoo! Japan Ads]

下列基本追蹤範本格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

或者，當中的帳戶設定了自動標籤選項時 [!DNL Yahoo! Japan Ads]：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

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

