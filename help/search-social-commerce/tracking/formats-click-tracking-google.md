---
title: 的點選追蹤格式 [!DNL Google Ads]
description: 瞭解的點選追蹤格式 [!DNL Google Ads] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# 的點選追蹤格式 [!DNL Google Ads]

以下是Search、Social和Commerce所需的基本追蹤範本和登陸頁面尾碼（最終URL尾碼）格式 [!DNL Google Ads].

## 追蹤範本格式

### 搜尋/顯示網路，包括網站連結

下列格式適用於搜尋和顯示網路上的所有可追蹤廣告型別，以及網站連結。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

範例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe廣告中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* 此 [!DNL ValueTrack] 在追蹤範本中指出最終URL的引數必須是 `{lpurl}` 或 `!{unescapedurl}`.
>
>* （文字廣告）當您依據關鍵字競標時，引數 `ev_pl` （適用於位置）沒有值。 當您依位置競標時， `ev_ln` （適用於關鍵字）沒有值。 當您按廣告群組或任何其他維度競標時，兩者皆可 `ev_ln` 和 `ev_pl` 沒有值。
>
>* （動態搜尋廣告） `{keyword}` 表示動態搜尋目標運算式，例如 `_cat:[VALUE]` 或 `_url:[VALUE]`.
>
>* （動態搜尋廣告） [!DNL Google Ads] 會以動態方式決定最終URL，因此您不需要輸入URL。
>
>* （網站連結）您可以透過產生「 」，檢視點選網站連結產生了哪些轉換 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] sitelink的欄值為 `sl:<Sitelink text>`，例如 `sl:See Current Offers`.


### 購物網路

下列格式適用於購物網路中的購物廣告和產品群組。 您可以在帳戶、行銷活動、廣告群組或產品群組層級指定追蹤範本。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

範例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe廣告中廣告商唯一ID的變數。
>
>* 此格式表示促銷活動已啟用Token傳遞（預設）。 如果停用權杖傳遞，請替代 `cq?` 晚於 `<advertiser_ID>` 替換為 `c?`.
>
>* 此 [!DNL ValueTrack] 在追蹤範本中指出最終URL的引數必須是 `{lpurl}` 或 `!{unescapedurl}`.
>
>* [!DNL Google Ads] 會使用Google商家中心摘要中的產品URL作為最終URL，因此您不需要輸入產品資料或產品群組的最終URL。
>
>* 您可以產生「 」，檢視哪些轉換是購物廣告點選所致 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] 產品廣告的欄值為pla：`<product ID>`，例如 `pla:8525822`.


## 登陸頁面尾碼（最終URL尾碼）格式

使用Adobe廣告轉換追蹤的帳戶必須包含廣告網路的點選識別碼(`gclid` 的 [!DNL Google Ads])在尾碼中：

* 當廣告商與Adobe Analytics整合時，尾碼必須包含下列其中一項：

   * [!DNL Google Ads] 使用最新版本的帳戶 `s_kwcid` 格式，可支援行銷活動和廣告群組層級報告，以提供最高成效行銷活動和草稿與實驗行銷活動：

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

      如果帳戶具有伺服器端s_kwcid實作，且帳戶或行銷活動設定»[!UICONTROL Auto Upload]「 」已啟用，則會自動新增引數。 否則，您需要手動新增。

   * 所有其他 [!DNL Google Ads] 帳戶：

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* 當廣告商沒有Adobe Analytics整合時，尾碼必須包含以下專案：

   `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* 較低層級的登入頁面尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。
>
>* (動態搜尋廣告；具有Adobe Analytics且沒有伺服器端追蹤的廣告商)如果您想要包含從Adobe廣告到Analytics的反向饋送追蹤，則附加 `s_kwcid` 追蹤程式碼至帳戶層級登陸頁面尾碼結尾。


>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤服務的點選追蹤URL格式](formats-click-tracking-about.md)
>* [s\_kwcid追蹤程式碼的格式](skwcid-tracking-parameter.md)

