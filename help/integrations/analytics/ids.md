---
title: 使用的Adobe AdvertisingID [!DNL Analytics]
description: 使用的Adobe AdvertisingID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 336664e00f626a7841c328b53b8f5cea1444f3d7
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# 使用的Adobe AdvertisingID [!DNL Analytics]

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*適用於Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用兩個ID進行網站上的效能追蹤： *EF ID* 和 *AMO ID*.

當廣告曝光發生時，Adobe Advertising會建立AMO ID和EF ID值並加以儲存。 當看過廣告的訪客進入網站而未點按廣告時， [!DNL Analytics] 會從Adobe Advertising呼叫這些值，一直到 [!DNL Analytics for Advertising] JavaScript程式碼。 針對檢視流量， [!DNL Analytics] 產生補充ID (`SDID`)，用於將EF ID和AMO ID彙整至 [!DNL Analytics]. 若為點進流量，這些ID會使用包含在登陸頁面URL中 `ef_id` 和 `s_kwcid` （適用於AMO ID）查詢字串引數。

Adobe Advertising會使用下列條件來區分網站的點進或檢視專案：

* 當使用者在檢視廣告後造訪網站，但未按一下網站時，則會擷取瀏覽專案。 [!DNL Analytics] 如果符合兩個條件，則會記錄檢視：

   * 訪客的「 」沒有點進 [!DNL DSP] 或 [!DNL Search, Social, & Commerce] 廣告時段 [按一下回顧視窗](#lookback-a4adc).

   * 訪客已看過至少一個 [!DNL DSP] 廣告時段 [曝光回顧期間](#lookback-a4adc). 最後曝光會以檢視的方式傳遞。

* 當網站訪客在進入網站前按一下廣告時，會擷取點進專案。 [!DNL Analytics] 發生下列任一情況時擷取點進：

   * URL包含EF ID和AMO ID，可透過Adobe Advertising新增至登陸頁面URL。

   * URL未包含追蹤程式碼，但Adobe AdvertisingJavaScript程式碼會偵測到過去兩分鐘內有人點按。

![Adobe Advertising檢視型 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1：Adobe Advertising檢視型 [!DNL Analytics] 整合*

![Adobe Advertising點選URL型 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2：Adobe Advertising點選URL型 [!DNL Analytics] 整合*

## ADOBE ADVERTISINGEF ID

EF ID是不重複權杖，Adobe Advertising會使用它來將活動與線上點選或廣告曝光度建立關聯。 EF ID儲存於 [一個 [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或 [!DNL rVar] (已保留 [!DNL eVar])維度(Adobe AdvertisingEF ID)並追蹤每個廣告在個別瀏覽器或裝置層級的點選或曝光情形。 EF ID主要作為傳送的金鑰 [!DNL Analytics] 資料要Adobe Advertising，以便在Adobe Advertising中報告和競標最佳化。

### EF ID格式

>[!NOTE]
>
>EF ID區分大小寫。 如果 [!DNL Analytics] 實作會強制將URL追蹤轉換為小寫，然後Adobe Advertising將無法辨識EF ID。 這將影響Adobe Advertising競標和報告，但不會影響內的Adobe Advertising報告 [!DNL Analytics].

#### [!DNL Google Ads] 搜尋廣告

```
{gclid}:G:s
```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是網路型別（「s」代表搜尋）。

#### Microsoft Advertising搜尋廣告

```
{msclkid}:G:s
```

其中：

* `msclkid` 是 [!DNL Microsoft Click ID] (MSCLKID)。
* `s` 是網路型別（「s」代表搜尋）。

#### 在其他搜尋引擎上顯示廣告和搜尋廣告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising訪客ID*>是每個訪客的唯一ID （例如UhKVaAABCkJ0mDt）。 也稱為 *瀏覽者ID*.

* &lt;*timestamp*>是YYYYMMDDHHMMSS格式的時間(例如20190821192533 for Year 2019， Month 08， Day 21， Time 19):25:33)。

* &lt;*頻道型別*>是造成按一下或曝光的管道型別：

   * `d` 針對DSP顯示廣告（顯示點進）的點按
   * `i` 針對DSP顯示廣告的曝光（顯示閱覽）
   * `s` ，按一下搜尋廣告（搜尋點進）。

範例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 報表中，您可以透過搜尋 [!UICONTROL EF ID] 維度和使用 [!UICONTROL EF ID Instance] 量度。

EF ID在Analysis Workspace中需遵守500,000的唯一識別碼限制。 一旦達到500k值，所有新的追蹤程式碼都會報告在單行專案標題下&quot;[!UICONTROL Low Traffic].」 由於可能會遺失報表精確度，EF ID不會進行分類，您不應將其用於中的區段或報表 [!DNL Analytics].

## ADOBE ADVERTISINGAMO ID {#amo-id}

AMO ID會在較不精細的層級追蹤每個不重複廣告組合，並用於 [!DNL Analytics] 資料分類以及從Adobe Advertising擷取廣告量度（例如曝光數、點按數和成本）。 AMO ID會儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)，並專門用於 [!DNL Analytics].

AMO ID也稱為 `s_kwcid`，有時發音為「[!DNL the squid].」

### 實作AMO ID的方式

引數會透過下列其中一種方式新增至您的追蹤URL：

* （建議）已實作伺服器端插入功能。

   * DSP客戶：當一般使用者檢視含有Adobe Advertising畫素的顯示廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登入頁面尾碼。

   * 搜尋、社交和商務客戶：

      * 的 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帳戶與 [!UICONTROL Auto Upload] 若設定為已啟用帳戶或促銷活動，當一般使用者按一下包含Adobe Advertising畫素的廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登陸頁面尾碼。

      * 針對其他廣告網路，或 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帳戶與 [!UICONTROL Auto Upload] 設定已停用，手動 [將引數新增至帳戶層級的附加引數](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，這會將其附加至您的基本URL。

* 未實作伺服器端插入功能：

   * DSP客戶：

      * 的 [!DNL Flashtalking] 新增標籤，手動插入其他巨集(根據&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md).」

      * 的 [!DNL Google Campaign Manager 360] 新增標籤，手動插入其他巨集(根據&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md).」

  <!--  * For all other ads, XXXX. -->

   * 搜尋、社交和商務客戶：

      * 針對([!DNL Google Ads] 和 [!DNL Microsoft® Advertising])廣告，請手動將AMO ID引數新增至您的登陸頁面尾碼，最好在 [帳戶層級](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} 除非需要對個別帳戶元件進行不同追蹤。

      * 針對所有其他廣告網路上的廣告，手動進行 [將AMO ID引數新增至帳戶層級的附加引數](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，這會將其附加至您的基本URL。

若要實施伺服器端插入功能，或決定最適合您企業的選項，請洽詢您的Adobe帳戶團隊。

### AMO ID格式 {#amo-id-formats}

#### AMO ID格式 [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC` 表示顯示通道。

* `{TM_AD_ID}` 是Adobe Advertising產生的英數字元廣告金鑰。 它會使用廣告的唯一識別碼，並作為將Adobe Advertising實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

* `{TM_PLACEMENT_ID}` 是Adobe Advertising產生的英數字元放置索引鍵。 它會使用位置的唯一識別碼，並作為將Adobe Advertising實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

範例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

#### 搜尋、社交和商務廣告的AMO ID格式

這些引數會因廣告網路而異，但下列引數是所有使用者共有的：

* `AL` 表示搜尋管道。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` 是指派給廣告商的不重複使用者ID。

* `{sid}` 將由廣告商廣告網路帳戶的數值ID取代： *3* 的 [!DNL Google Ads]， *10* 的 [!DNL Microsoft Advertising]， *45* 的 [!DNL Meta]， *86* 的 [!DNL Yahoo! Display Network]， *87* 的 [!DNL Naver]， *88* 的 [!DNL Baidu]， *90* 的 [!DNL Yandex]， *94* 的 [!DNL Yahoo! Japan Ads]， *105* 的 [!DNL Yahoo Native] （已棄用），或 *106* 的 [!DNL Pinterest] （已棄用）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

其中：

* `{creative}` 是廣告網路的唯一創意數值ID。
* `{placement}` 是點按廣告的網站。
* `{keywordid}` 是觸發廣告之關鍵字的廣告網路唯一數值ID。

##### [!DNL Google Ads]

其中包括使用的購物行銷活動 [!DNL Google Merchant Center].

* 使用最新AMO ID格式的帳戶，支援最高成效行銷活動的行銷活動和廣告群組層級報告，以及草稿和實驗行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帳戶：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

其中：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` 是 [!DNL Google Ads] 創意內容的不重複數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的相符型別： `e` 確切地說， `p` 用於片語，或 `b` 適用於廣泛。
* `{placement}` 是廣告被點按所在網站的網域名稱。 值適用於以位置為目標的行銷活動中的廣告，以及內容網站上顯示之以關鍵字為目標的行銷活動中的廣告。
* `{network}` 表示發生點按的網路： `g` 的 [!DNL Google] 搜尋（僅適用於以關鍵字為目標的廣告）， `s` （僅適用於關鍵字目標廣告），或 `d` 適用於顯示網路（適用於關鍵字目標或位置目標廣告）。
* `{product_partition_id}` 是用於產品廣告之產品群組的廣告網路唯一數值ID。
* `{keyword}` 是觸發您廣告的特定關鍵字（在搜尋網站上）或最佳比對關鍵字（在內容網站上）。
* `{campaignid}` 是促銷活動的廣告網路唯一數值ID。
* `{adgroupid}` 是廣告群組的廣告網路唯一數值ID。

>[!NOTE]
>
>* 對於動態搜尋廣告， {keyword} 填入了自動鎖定目標。
>* 當您產生的追蹤 [!DNL Google] 購物廣告、產品ID引數、 `{adwords_producttargetid}`，會插入在keyword引數之前。 產品ID引數未出現在 [!DNL Google Ads] 帳戶層級和促銷活動層級的追蹤引數。
>* 若要使用最新的AMO ID追蹤程式碼，請參閱&quot;[更新的AMO ID追蹤程式碼 [!DNL Google Ads] 帳戶](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).」 <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 搜尋行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 購物行銷活動(使用 [!DNL Microsoft Merchant Center])：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 對象網路行銷活動：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

其中：

* `{AdId}` 是廣告網路的唯一創意數值ID。
* `{OrderItemId}` 是關鍵字的廣告網路數值ID。
* `{CriterionId}` 是用於產品廣告之產品群組的廣告網路數值ID。

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

其中：

* `{creative}` 是廣告網路的唯一創意數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的相符型別： `be` 確切地說， `bp` 用於片語，或 `bb` 適用於廣泛。
* `{network}` 表示發生點按的網路： `n` 針對原生或 `s` 以進行搜尋。
* `{keyword}` 是觸發廣告的關鍵字。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

其中：

* `{ad_id}` 是廣告網路的唯一創意數值ID。
* `{source_type}` 是廣告已顯示所在的網站型別： *b* 進行搜尋， *c* 內容（內容），或 *ct* 類別。
* `{phrase_id}` 是關鍵字的廣告網路數值ID。

### 中的AMO IDDimension [!DNL Analytics]

在Analytics報表中，您可以搜尋 [!UICONTROL AMO ID] 維度和使用 [!UICONTROL AMO ID Instance] 量度。 此 [!UICONTROL AMO ID] 維度會儲存所有擷取的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度會指出網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按四次，但Analytics追蹤了七個網站專案，則 [!UICONTROL AMO ID Instance] 為七(7)和 [!UICONTROL Clicks] 為四(4)。

對於內的任何報告或稽核 [!DNL Analytics]，最佳實務是使用AMO ID及其對應的例項。 如需詳細資訊，請參閱&quot;[資料驗證 [!DNL Analytics for Advertising]](data-variances.md#data-validation)「預期資料差異： [!DNL Analytics] 和Adobe Advertising。」

## 關於Analytics分類

在 [!DNL Analytics]， a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是指定追蹤代碼（例如帳戶、促銷活動或廣告）的中繼資料。 Adobe Advertising會使用分類來分類原始Adobe Advertising資料，以便在您產生報表時能以不同的方式顯示資料（例如依廣告型別或促銷活動）。 分類構成中Adobe Advertising報告的基礎 [!DNL Analytics] 可與AMO量度搭配使用，例如 [!UICONTROL AMO Cost]， [!UICONTROL AMO Impressions]、和 [!UICONTROL AMO Clicks]、以及自訂和標準站上事件(例如 [!UICONTROL Visits]， [!UICONTROL Leads]， [!UICONTROL Orders]、和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [預期資料差異： [!DNL Analytics] 和Adobe Advertising](data-variances.md)
