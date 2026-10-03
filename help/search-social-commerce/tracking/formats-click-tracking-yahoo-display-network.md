---
title: '[!DNL Yahoo DSP]的點選追蹤格式'
description: 瞭解[!DNL Yahoo DSP]帳戶的點選追蹤格式。
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/sQo6hr3UHQwN9GgazCKv2ba-m4ZXf2ZrhdemCpbVYvU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%
---
# [!DNL Yahoo DSP]上贊助廣告的點選追蹤格式

下列基本目的地URL格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
>* [AMO ID格式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
