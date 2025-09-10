---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---
# AMO ID格式 {#amo-id-formats}

#### [!DNL DSP]的AMO ID格式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC`表示顯示通道。

* `{TM_AD_ID}`是Adobe Advertising產生的英數字元廣告金鑰。 此識別碼是廣告的唯一識別碼，可作為將Adobe Advertising實體中繼資料轉換為可讀取[!DNL Analytics]和Customer Journey Analytics維度的索引鍵。

* `{TM_PLACEMENT_ID}`是Adobe Advertising產生的英數字元放置索引鍵。 這是用於位置的唯一識別碼，可當作將Adobe Advertising實體中繼資料轉譯為可讀取[!DNL Analytics]和Customer Journey Analytics維度的索引鍵。

範例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

#### 搜尋、社交和Commerce廣告的AMO ID格式 {#amo-id-format-search}

這些引數會因廣告網路而異，但下列引數是所有使用者共有的：

* `AL`表示搜尋頻道。<!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}`是指派給廣告商的不重複使用者識別碼。

* `{sid}`已取代為廣告商廣告網路帳戶的數值ID： *的* 3[!DNL Google Ads]、*的* 10[!DNL Microsoft Advertising]、*的* 45[!DNL Meta]、*的* 86[!DNL Yahoo! Display Network]、*的* 87[!DNL Naver]、*的* 88[!DNL Baidu]、*的* 90[!DNL Yandex]、*94* [!DNL Yahoo! Japan Ads]的&#x200B;*、* 105[!DNL Yahoo Native]（已棄用）或&#x200B;*的* 106[!DNL Pinterest]（已棄用）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

其中：

* `{creative}`是廣告網路的創意唯一數值ID。
* `{placement}`是廣告被點按的網站。
* `{keywordid}`是觸發廣告之關鍵字的廣告網路唯一數值ID。

##### [!DNL Google Ads]

其中包括使用[!DNL Google Merchant Center]的購物行銷活動。

* 使用最新AMO ID格式的帳戶，支援最高成效行銷活動的行銷活動和廣告群組層級報告，以及草稿和實驗行銷活動：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帳戶：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

其中：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}`是創意內容的[!DNL Google Ads]唯一數值ID。
* `{matchtype}`是觸發廣告的關鍵字元合型別： `e`表示精確，`p`表示詞句，或`b`表示廣泛。
* `{placement}`是廣告被點按所在網站的網域名稱。 值適用於以位置為目標的行銷活動中的廣告，以及內容網站上顯示之以關鍵字為目標的行銷活動中的廣告。
* `{network}`表示發生點按的網路： `g`個搜尋的[!DNL Google] （僅關鍵字目標廣告）、`s`個搜尋夥伴的 （僅關鍵字目標廣告），或顯示網路的`d` （關鍵字目標或位置目標廣告）。
* `{product_partition_id}`是與產品廣告搭配使用的產品群組的廣告網路唯一數值ID。
* `{keyword}`是觸發您廣告的特定關鍵字（在搜尋網站上）或最佳比對關鍵字（在內容網站上）。
* `{campaignid}`是促銷活動的廣告網路唯一數值ID。
* `{adgroupid}`是廣告群組的廣告網路唯一數值ID。

>[!NOTE]
>
>* 對於動態搜尋廣告，{keyword}會填入自動鎖定目標。
>* 當您產生[!DNL Google]購物廣告的追蹤時，產品ID引數`{adwords_producttargetid}`會插入到關鍵字引數之前。 產品ID引數未出現在[!DNL Google Ads]帳戶層級和促銷活動層級的追蹤引數中。
>* 若要使用最新的AMO ID追蹤代碼，請參閱[更新 [!DNL Google Ads] 帳戶](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)的AMO ID追蹤代碼。<!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 所有行銷活動型別：

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

其中：

* `{AdId}`是廣告網路的創意唯一數值ID。
* `{OrderItemId}`是關鍵字的廣告網路數值ID。
* `{CampaignId}`是促銷活動的廣告網路唯一數值ID。
* `{AdGroupId}`是廣告群組的廣告網路唯一數值ID。

>[!NOTE]
>
> 對於沒有[!UICONTROL Auto Upload]追蹤選項的行銷活動帳戶，如果尚未移轉至新格式，請手動更新每個登入頁面尾碼，以包含上述格式。
> >同時，舊版格式（如下）仍可運作：
>* 搜尋行銷活動：
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* 購物行銷活動（使用[!DNL Microsoft Merchant Center]）：
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* 對象網路行銷活動：
>  >  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

其中：

* `{creative}`是廣告網路的創意唯一數值ID。
* `{matchtype}`是觸發廣告的關鍵字元合型別： `be`表示精確，`bp`表示詞句，或`bb`表示廣泛。
* `{network}`表示發生點選的網路： `n`代表原生，或`s`代表搜尋。
* `{keyword}`是觸發廣告的關鍵字。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

其中：

* `{ad_id}`是廣告網路的創意唯一數值ID。
* `{source_type}`是顯示廣告的網站型別： *b*&#x200B;用於搜尋，*c*&#x200B;用於內容（內容），或&#x200B;*ct*&#x200B;用於類別。
* `{phrase_id}`是關鍵字的廣告網路數值ID。
