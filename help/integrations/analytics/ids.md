---
title: ' [!DNL Analytics]使用的Adobe Advertising ID'
description: ' [!DNL Analytics]使用的Adobe Advertising ID'
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dbbba0bd75f3b1003325b665d06bce003c5ee054
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 0%

---

# [!DNL Analytics]使用的Adobe Advertising ID

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*適用於Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用兩個ID進行網站上的效能追蹤： *EF ID*&#x200B;和&#x200B;*AMO ID*。

當廣告曝光發生時，Adobe Advertising會建立AMO ID和EF ID值並加以儲存。 當訪客看到廣告而未點按廣告即進入網站時，[!DNL Analytics]會透過[!DNL Analytics for Advertising] JavaScript程式碼從Adobe Advertising呼叫這些值。 針對檢視流量，[!DNL Analytics]會產生補充ID (`SDID`)，用於將EF ID和AMO ID拼接成[!DNL Analytics]。 針對點進流量，這些ID會使用`ef_id`和`s_kwcid` （針對AMO ID）查詢字串引數包含在登陸頁面URL中。

Adobe Advertising會使用下列條件來區分網站的點進或檢視專案：

* 當使用者在檢視廣告後造訪網站，但未按一下網站時，則會擷取瀏覽專案。 如果符合兩個條件，[!DNL Analytics]會記錄檢視：

   * 訪客在[!DNL DSP]點按回顧期間[!DNL Search, Social, & Commerce]沒有[或](/help/integrations/analytics/prerequisites.md#lookback-a4adc)廣告的點進次數。

   * 訪客在[!DNL DSP]印象回顧期間[看見至少一個](/help/integrations/analytics/prerequisites.md#lookback-a4adc)廣告。 最後曝光會以檢視的方式傳遞。

* 當網站訪客在進入網站前按一下廣告時，會擷取點進專案。 發生下列任一情況時，[!DNL Analytics]會擷取點進：

   * URL包含EF ID和AMO ID，由Adobe Advertising新增至登陸頁面URL。

   * URL未包含追蹤程式碼，但Adobe Advertising JavaScript程式碼會在過去兩分鐘內偵測到一次點按。

![Adobe Advertising檢視式[!DNL Analytics]整合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1： Adobe Advertising檢視式[!DNL Analytics]整合*

![Adobe Advertising點按URL型[!DNL Analytics]整合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2： Adobe Advertising點選以URL為基礎的[!DNL Analytics]整合*

## ADOBE ADVERTISING EF ID

EF ID是不重複Token，Adobe Advertising會用來將活動與線上點選或廣告曝光度建立關聯。 EF ID儲存在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或[!DNL rVar] （保留的[!DNL eVar]）維度(Adobe Advertising EF ID)中，並追蹤個別瀏覽器或裝置層級的每個廣告點選或曝光。 EF ID主要當作金鑰，用於將[!DNL Analytics]資料傳送至Adobe Advertising，以便在Adobe Advertising中最佳化報表和競標。

### EF ID格式

>[!NOTE]
>
>EF ID區分大小寫。 如果[!DNL Analytics]實作強制將URL追蹤轉換為小寫，則Adobe Advertising無法辨識EF ID。 這會影響Adobe Advertising競標和報告，但不會影響[!DNL Analytics]內的Adobe Advertising報告。

#### [!DNL Google Ads]個搜尋廣告

```
{gclid}:G:s
```

其中：

* `gclid`是[!DNL Google Click ID] (GCLID)。
* `s`是網路型別（搜尋時為「s」）。

#### [!DNL Microsoft Advertising]個搜尋廣告

```
{msclkid}:G:s
```

其中：

* `msclkid`是[!DNL Microsoft Click ID] (MSCLKID)。
* `s`是網路型別（搜尋時為「s」）。

#### 在其他搜尋引擎上顯示廣告和搜尋廣告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising訪客ID*>是每個訪客的唯一識別碼（例如UhKVaAABCkJ0mDt）。 也稱為&#x200B;*瀏覽者ID*。

* &lt;*timestamp*>是YYYYYMMDDHHMMSS格式的時間(例如20190821192533 for Year 2019， Month 08， Day 21， Time 19:25:33)。

* &lt;*頻道型別*>是負責點選或曝光的頻道型別：

   * `d`點選DSP顯示廣告（顯示點進）
   * `i`用於DSP顯示廣告（顯示瀏覽次數）的曝光
   * `s`搜尋廣告的點按（搜尋點進）。

範例`EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### [!DNL Analytics]中的EF ID Dimension

在[!DNL Analytics]報表中，您可以搜尋[!UICONTROL EF ID]維度並使用[!UICONTROL EF ID Instance]量度來尋找EF ID資料。

EF ID在Analysis Workspace中需遵守500,000的唯一識別碼限制。 一旦達到500k值，所有新追蹤程式碼都會報告於單行專案標題&quot;[!UICONTROL Low Traffic]&quot;下。 由於可能遺失報表精確度，EF ID不會進行分類，您不應該在[!DNL Analytics]中將其用於區段或報表。

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID會在較不細微的層級追蹤每個不重複廣告組合，並用於[!DNL Analytics]資料分類以及從Adobe Advertising擷取廣告量度（例如曝光數、點按數和成本）。 AMO ID儲存在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar維度(AMO ID)中，僅用於[!DNL Analytics]中的報告。

AMO ID也稱為`s_kwcid`，有時發音為&quot;[!DNL squid]&quot;。

### 實作AMO ID的方式 {#amo-id-implement}

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

* `{TM_AD_ID}`是Adobe Advertising產生的英數字元廣告金鑰。 此識別碼是廣告的唯一識別碼，可作為將Adobe Advertising實體中繼資料轉譯為可讀取[!DNL Analytics]維度的索引鍵。

* `{TM_PLACEMENT_ID}`是Adobe Advertising產生的英數字元放置索引鍵。 此識別碼用於位置的唯一識別碼，並作為將Adobe Advertising實體中繼資料轉譯為可讀取[!DNL Analytics]維度的索引鍵。

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

### [!DNL Analytics]中的AMO ID Dimension

在Analytics報表中，您可以搜尋[!UICONTROL AMO ID]維度並使用[!UICONTROL AMO ID Instances]量度來尋找AMO ID資料。 [!UICONTROL AMO ID]維度內含所有擷取的AMO ID值，而[!UICONTROL AMO ID Instances]量度則表示網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按四次，但Analytics追蹤了七個網站專案，則[!UICONTROL AMO ID Instances]會是七(7)，[!UICONTROL Clicks]會是四(4)。

對於[!DNL Analytics]內的任何報告或稽核，最佳實務是使用AMO ID及其對應的執行個體。 如需詳細資訊，請參閱「在[和Adobe Advertising之間的預期資料差異」中的 [!DNL Analytics for Advertising]](data-variances.md#data-validation)的[!DNL Analytics]點進資料驗證。

## 關於Analytics分類

在[!DNL Analytics]中，[分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)是指定追蹤代碼（例如帳戶、促銷活動或廣告）的中繼資料。 Adobe Advertising會使用分類來分類原始Adobe Advertising資料，以便在您產生報表時，可以不同方式（例如依廣告型別或促銷活動）顯示資料。 在[!DNL Analytics]中以Adobe Advertising報告為基礎的分類，可與AMO量度（例如[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]和[!UICONTROL AMO Clicks]）搭配使用，也可與自訂和標準站上事件（例如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）搭配使用。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [預期資料差異介於 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之間
