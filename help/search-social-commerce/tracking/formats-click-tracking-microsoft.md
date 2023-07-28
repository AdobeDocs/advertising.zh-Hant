---
title: 的點選追蹤格式 [!DNL Microsoft Advertising]
description: 瞭解的點選追蹤格式 [!DNL Microsoft Advertising] 帳戶。
exl-id: 725981db-1b9a-4c89-b95d-98d07ec99756
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# 的點選追蹤格式 [!DNL Microsoft Advertising]

以下是Search、Social和Commerce所需的基本追蹤範本和登陸頁面尾碼（最終URL尾碼）格式 [!DNL Microsoft Advertising].

## 追蹤範本格式

### 搜尋和受眾網路（網站連結除外）

以下格式適用於搜尋和受眾網路上的所有可追蹤廣告型別。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `{TargetId}` 代表a)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象） （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」，或關鍵字僅使用「kwd-123」）的ID。

### 網站連結

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `{TargetId}` 代表a)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象） （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」，或關鍵字僅使用「kwd-123」）的ID。
>
>* `{adextensionid}` 未使用。
>
>* （網站連結）您可以透過產生「 」，檢視點按網站連結產生了哪些轉換 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] sitelink的欄值為 `sl:<Sitelink text>`，例如 `sl:See Current Offers`.

### 購物網路

下列格式適用於購物網路中的購物廣告。 您可以在帳戶、行銷活動、廣告群組或產品群組層級指定追蹤範本。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

範例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* `{TargetId}` 代表a)關鍵字或b)觸發廣告的關鍵字和再行銷清單（對象） （例如，關鍵字和再行銷清單均使用「kwd-123：aud-456」，或關鍵字僅使用「kwd-123」）的ID。
>
>* （可選）您可以將追蹤URL新增至中的產品資料，而不需在帳戶、行銷活動、廣告群組或產品群組層級輸入追蹤範本。 [!DNL Microsoft Merchant Center] 帳戶。 若要這麼做，請納入追蹤URL，連同「」中的值`link`「或」`mobile_link`「自訂欄中的欄位」[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)」在產品摘要中。 「」中的值`bingads_redirect`「欄位會取代」中的值`link`「和」`mobile_link`「欄位。 使用此方法產生的URL不包含任何在Search、Social和Commerce帳戶或行銷活動設定中指定的追蹤引數。

## 登陸頁面尾碼（最終URL尾碼）格式

>[!NOTE]
>
>較低層級的登陸頁面尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。

### 搜尋和受眾網路

使用Adobe Advertising轉換追蹤的帳戶必須包含廣告網路的點選識別碼(`msclkid` 的 [!DNL Microsoft Advertising])的後置字元：

* 當廣告商整合Adobe Analytics時，尾碼必須包括下列專案：

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 當廣告商沒有Adobe Analytics整合時，尾碼必須包括下列專案：

  `&ev_efid={msclkid}:G:s`

### 購物網路

使用Adobe Advertising轉換追蹤的帳戶必須包含廣告網路的點選識別碼(`msclkid` 的 [!DNL Microsoft Advertising])的後置字元：

* 當廣告商整合Adobe Analytics時，尾碼必須包括下列專案：

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 當廣告商沒有Adobe Analytics整合時，尾碼必須包括下列專案：

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [s\_kwcid追蹤程式碼的格式](skwcid-tracking-parameter.md)
