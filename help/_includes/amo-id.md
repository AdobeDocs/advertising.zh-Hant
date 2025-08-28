---
source-git-commit: 6fa4e5d06271789edc915d67d320f775a83ed653
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID會在較不細微的層級追蹤每個不重複廣告組合，並用於[!DNL Analytics]和Customer Journey Analytics資料分類以及從Adobe Advertising擷取廣告量度（例如曝光數、點按數和成本）。

針對[!DNL Analytics]，AMO ID儲存在[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hant)或rVar維度(AMO ID)中。

對於Customer Journey Analytics，AMO ID儲存在`trackingCode`物件的`conversionDetails`屬性中，該物件是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。

AMO ID也稱為`s_kwcid`，有時發音為&quot;[!DNL squid]&quot;。

### （[!DNL Analytics]位使用者）實作AMO ID的方式 {#amo-id-implement}

<!-- Add info about implementing in CJA -->

引數會透過下列其中一種方式新增至您的追蹤URL：

* （建議）實作伺服器端插入功能時。

   * DSP客戶：當一般使用者檢視含有Adobe Advertising畫素的顯示廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登陸頁面尾碼。

   * 搜尋、社交和Commerce客戶：

      * 針對已啟用[!DNL Google Ads]設定的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帳戶（帳戶或促銷活動），當一般使用者按一下包含Adobe Advertising畫素的廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登陸頁面尾碼。

      * 針對其他廣告網路，或停用[!DNL Google Ads]設定的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帳戶，手動將引數新增至您的[帳戶層級附加引數](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，以便將其附加至您的基礎URL。

* 未實作伺服器端插入功能時：

   * DSP客戶： [JavaScript程式碼](javascript.md)會自動記錄點進和檢視。 當瀏覽器不支援第三方Cookie時，您仍可追蹤下列廣告型別的點按型轉換：

      * 針對[!DNL Flashtalking]廣告標籤，手動插入每個[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)的其他巨集。 **注意：**&#x200B;如果您的組織與[!DNL Flashtalking]有直接的合作關係，而且您根據`s_kwcid`支援檔案(位於`ef_id`https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros[!DNL Flashtalking])中的[與](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)追蹤引數，則不需要執行此程式。

      * 針對[!DNL Google Campaign Manager 360]廣告標籤，手動插入每個[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)的其他巨集。

   * 搜尋、社交和Commerce客戶：

      * 針對（[!DNL Google Ads]和[!DNL Microsoft Advertising]）廣告，手動將AMO ID引數新增至您的登入頁面尾碼，最好在[帳戶層級](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，除非個別帳戶元件需要不同的追蹤。

      * 針對所有其他廣告網路上的廣告，手動將AMO ID引數新增至您的[帳戶層級附加引數](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，這會將其附加至您的基本URL。

若要實施伺服器端插入功能，或決定最適合您企業的選項，請洽詢您的Adobe帳戶團隊。

### AMO ID格式 {#amo-id-formats}

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
> &#x200B;>同時，舊版格式（如下）仍可運作：
>* 搜尋行銷活動：
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* 購物行銷活動（使用[!DNL Microsoft Merchant Center]）：
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* 對象網路行銷活動：
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

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
