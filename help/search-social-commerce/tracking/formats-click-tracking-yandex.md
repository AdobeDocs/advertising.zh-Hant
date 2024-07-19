---
title: ' [!DNL Yandex]的點選追蹤格式'
description: 瞭解 [!DNL Yandex] 帳戶的點選追蹤格式。
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# [!DNL Yandex]上贊助廣告的點選追蹤格式

下列基本目的地URL格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `<the landing page>`是變數，代表一般使用者在網站上導向的URL。
>
>* `source_type`是相符型別。
>
>* `source`是廣告顯示於搜尋或內容型網站上。
>
>* `position`是區塊中廣告的位置編號。 若為非搜尋流量，值為「0」。
>
>* `position_type`是在[!DNL Yandex]上顯示廣告的區塊。 可能的值： 「premium」（頂端區塊）、「other」（右側區塊）或「none」（非搜尋流量）。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
