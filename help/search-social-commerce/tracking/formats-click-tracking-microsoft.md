---
title: ' [!DNL Microsoft Advertising]的點選追蹤格式'
description: 瞭解 [!DNL Microsoft Advertising] 帳戶的點選追蹤格式。
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]的點選追蹤格式

以下是Search、Social和Commerce所需的[!DNL Microsoft Advertising]基本追蹤範本和登入頁面尾碼（最終URL尾碼）格式。

## 追蹤範本格式

### 搜尋和受眾網路（網站連結除外）

以下格式適用於搜尋和受眾網路上的所有可追蹤廣告型別。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `{TargetId}`代表A)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象）的ID （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」或「kwd-123」僅使用關鍵字）。

### 網站連結

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `{TargetId}`代表A)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象）的ID （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」或「kwd-123」僅使用關鍵字）。
>
>* `{adextensionid}`未使用。
>
>* （網站連結）您可以透過產生[!UICONTROL Transaction Report]檢視點按網站連結產生了哪些轉換。 Sitelink的[!UICONTROL Link Type]資料行值為`sl:<Sitelink text>`，例如`sl:See Current Offers`。

### 購物網路

下列格式適用於購物網路中的購物廣告。 您可以在帳戶、行銷活動、廣告群組或產品群組層級指定追蹤範本。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中廣告商唯一識別碼的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請在`<advertiser_ID>`之後以`c?`取代`cq?`。
>
>* `{TargetId}`代表A)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象）的ID （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」或「kwd-123」僅使用關鍵字）。
>
>* （選擇性）您不必在帳戶、行銷活動、廣告群組或產品群組層級輸入追蹤範本，而是可以將追蹤URL新增至[!DNL Microsoft Merchant Center]帳戶內的產品資料。 若要這麼做，請在產品摘要的自訂欄「[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)」中，加入追蹤URL以及適當的「`link`」或「`mobile_link`」欄位中的值。 「`bingads_redirect`」欄位中的值會取代「`link`」和「`mobile_link`」欄位中的值。 使用此方法產生的URL不包含任何在「搜尋」、「社交」和「Commerce」帳戶或促銷活動設定中指定的追蹤引數。

## 登陸頁面尾碼（最終URL尾碼）格式

>[!NOTE]
>
>較低層級的登陸頁面尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。

### 搜尋和受眾網路

使用Adobe Advertising轉換追蹤的帳戶必須在尾碼中包含廣告網路的點選識別碼（[!DNL Microsoft Advertising]為`msclkid`）：

* 當廣告商整合Adobe Analytics時，尾碼必須包括下列專案：

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* 當廣告商沒有Adobe Analytics整合時，尾碼必須包括下列專案：

  `&ev_efid={msclkid}:G:s`

### 購物網路

使用Adobe Advertising轉換追蹤的帳戶必須在尾碼中包含廣告網路的點選識別碼（[!DNL Microsoft Advertising]為`msclkid`）：

* 當廣告商整合Adobe Analytics時，尾碼必須包括下列專案：

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* 當廣告商沒有Adobe Analytics整合時，尾碼必須包括下列專案：

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
