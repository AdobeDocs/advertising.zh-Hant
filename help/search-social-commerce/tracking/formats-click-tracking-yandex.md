---
title: 的點選追蹤格式 [!DNL Yandex]
description: 瞭解的點選追蹤格式 [!DNL Yandex] 帳戶。
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# 上的贊助廣告的點選追蹤格式 [!DNL Yandex]

下列基本目的地URL格式適用於贊助廣告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `<the landing page>` 是變數，代表一般使用者要導向的網站URL。
>
>* `source_type`  是相符型別。
>
>* `source` 是廣告顯示於搜尋或內容型網站上。
>
>* `position` 是區塊中廣告的位置編號。 若為非搜尋流量，值為「0」。
>
>* `position_type` 是顯示廣告的區塊 [!DNL Yandex]. 可能的值： 「premium」（頂端區塊）、「other」（右側區塊）或「none」（非搜尋流量）。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
