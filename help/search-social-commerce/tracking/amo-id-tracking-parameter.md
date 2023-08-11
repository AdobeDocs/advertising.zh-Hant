---
title: AMO ID (s_kwcid)追蹤引數
description: 瞭解用來與Adobe Analytics共用Adobe Advertising資料的追蹤引數。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# AMO ID (s_kwcid)追蹤引數

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe AdvertisingAdobe Analytics會使用AMO ID附加引數(也稱為 `s_kwcid` 引數，包含廣告頻道和廣告網路專用元素。

<!-- add everything below to IDs page -->

引數會透過下列其中一種方式新增至您的追蹤URL：

* （建議）已實作伺服器端插入功能。

  的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帳戶與 [!UICONTROL Auto Upload] 若設定已啟用帳戶或促銷活動，當一般使用者點按廣告時，畫素伺服器會自動將AMO ID引數附加至您的登陸頁面尾碼 <!-- click a search ad or views a display ad --> 與Adobe Advertising畫素。

  針對其他廣告網路，或 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帳戶與 [!UICONTROL Auto Upload] 設定已停用，手動將AMO ID引數新增至您的帳戶層級附加引數，這會將其附加至您的基本URL。

* <!-- (Search, Social, & Commerce only) -->未實施伺服器端插入功能，您必須手動將AMO ID引數新增至([!DNL Google Ads] 和 [!DNL Microsoft Advertising])登陸頁面尾碼或（其他廣告網路）帳戶層級的附加引數。

若要實施伺服器端插入功能，或決定最適合您企業的選項，請洽詢您的Adobe帳戶團隊。

## Advertising DSP廣告的AMO ID格式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC` 表示顯示通道。

* `{TM_AD_ID}` 是英數字元廣告金鑰。

* `{TM_PLACEMENT_ID}` 是英數字元放置索引鍵。

## 搜尋、社交和商務廣告的AMO ID格式

這些引數會因廣告網路而異，但下列引數是所有使用者共有的：

* `AL` 表示搜尋管道。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` 是指派給廣告商的不重複使用者ID。

* `{sid}` 將由廣告商廣告網路帳戶的數值ID取代： *3* 的 [!DNL Google Ads]， *10* 的 [!DNL Microsoft Advertising]， *45* 的 [!DNL Meta]， *86* 的 [!DNL Yahoo! Display Network]， *87* 的 [!DNL Naver]， *88* 的 [!DNL Baidu]， *90* 的 [!DNL Yandex]， *94* 的 [!DNL Yahoo! Japan Ads]， *105* 的 [!DNL Yahoo Native] （已棄用），或 *106* 的 [!DNL Pinterest] （已棄用）。

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

其中包括使用的購物行銷活動 [!DNL Google Merchant Center].

* 使用最新AMO ID格式的帳戶，支援最高成效行銷活動的行銷活動和廣告群組層級報告，以及草稿和實驗行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帳戶：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* 對於動態搜尋廣告， {keyword} 填入了自動鎖定目標。
>* 當您產生的追蹤 [!DNL Google] 購物廣告、產品ID引數、 `{adwords_producttargetid}`，會插入在keyword引數之前。 產品ID引數未出現在 [!DNL Google Ads] 帳戶層級和促銷活動層級的追蹤引數。
>* 若要使用最新的AMO ID追蹤程式碼，請參閱&quot;[更新的AMO ID追蹤程式碼 [!DNL Google Ads] 帳戶](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).」 <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* 搜尋行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 購物行銷活動(使用 [!DNL Microsoft Merchant Center])：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 對象網路行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [管理廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [百度行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo！ Japan Ads促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
