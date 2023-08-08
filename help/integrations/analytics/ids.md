---
title: 使用的Adobe AdvertisingID [!DNL Analytics]
description: 使用的Adobe AdvertisingID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# 使用的Adobe AdvertisingID [!DNL Analytics]

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*適用於Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用兩個ID進行網站上的效能追蹤： *EF ID* 和 *AMO ID*.

當廣告曝光發生時，Adobe Advertising會建立AMO ID和EF ID值並加以儲存。 當看過廣告的訪客進入網站而未點按廣告時， [!DNL Analytics] 會從Adobe Advertising呼叫這些值，一直到 [!DNL Analytics for Advertising] JavaScript程式碼。 針對檢視流量， [!DNL Analytics] 產生補充ID (`SDID`)，用於將EF ID和AMO ID彙整至 [!DNL Analytics]. 若為點進流量，這些ID會使用包含在登陸頁面URL中 `s_kwcid` 和 `ef_id` 查詢字串引數。

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

## ADOBE ADVERTISINGAMO ID

AMO ID會在較不精細的層級追蹤每個不重複廣告組合，並用於 [!DNL Analytics] 資料分類以及從Adobe Advertising擷取廣告量度（例如曝光數、點按數和成本）。 AMO ID會儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)，並專門用於 [!DNL Analytics].

AMO ID也稱為 `s_kwcid`，有時發音為「[!DNL the squid].」

### AMO ID格式 [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

其中：

* &lt;*管道ID*>可能是：

   * `AC` = Advertising DSP
   * `AL` 的 [!DNL Advertising Search, Social, & Commerce]

* &lt;*廣告ID*>是Adobe Advertising產生的廣告唯一識別碼。 它可當作將Adobe Advertising實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

* &lt;*位置ID*>是Adobe Advertising產生的位置唯一識別碼。 它可當作將Adobe Advertising實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

範例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

### AMO ID格式 [!DNL Search, Social, & Commerce]

的AMO ID [!DNL Search, Social, & Commerce] 每個搜尋引擎請遵循不同的格式。 所有搜尋引擎的格式都以下列專案開頭：

```
AL!{userid}!{sid}
```

其中：

* `AL` 是廣告網路的管道ID。
* `{userid}` 是Adobe Advertising指派給廣告商的不重複數值使用者ID。
* `{sid}` 是Adobe Advertising用於指定廣告網路的數值ID，例如 `3` 的 [!DNL Google Ads] 或 `10` 的 [!DNL Microsoft Advertising].

以下是一些廣告網路的完整AMO ID格式。 如需其他廣告網路的AMO ID格式，請聯絡您的Adobe客戶團隊。

AMO ID格式 [!DNL Google Ads]：

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

其中：

* `{creative}` 是 [!DNL Google Ads] 創意內容的不重複數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的相符型別： `e` 確切地說， `p` 用於片語，或 `b` 適用於廣泛。
* `{placement}` 是廣告被點按所在網站的網域名稱。 值適用於以位置為目標的行銷活動中的廣告，以及內容網站上顯示之以關鍵字為目標的行銷活動中的廣告。
* `{network}` 表示發生點按的網路：  `g` 的 [!DNL Google] 搜尋（僅適用於以關鍵字為目標的廣告）， `s` （僅適用於關鍵字目標廣告），或 `d` 針對「顯示網路」 （針對關鍵字或位置定位的廣告）。
* `{keyword}` 是觸發您廣告的特定關鍵字（在搜尋網站上）或最佳比對關鍵字（在內容網站上）。

AMO ID格式 [!DNL Microsoft Advertising]：

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 創意內容的不重複數值ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 關鍵字的數值ID。

### 中的AMO IDDimension [!DNL Analytics]

在Analytics報表中，您可以搜尋 [!UICONTROL AMO ID] 維度和使用 [!UICONTROL AMO ID Instance] 量度。 此 [!UICONTROL AMO ID] 維度會儲存所有擷取的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度會指出網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按四次，但Analytics追蹤了七個網站專案，則 [!UICONTROL AMO ID Instance] 為七(7)和 [!UICONTROL Clicks] 為四(4)。

對於內的任何報告或稽核 [!DNL Analytics]，最佳實務是使用AMO ID及其對應的例項。 如需詳細資訊，請參閱&quot;[資料驗證 [!DNL Analytics for Advertising]](data-variances.md#data-validation)「預期資料差異： [!DNL Analytics] 和Adobe Advertising。」

## 關於Analytics分類

在 [!DNL Analytics]， a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是指定追蹤代碼（例如帳戶、促銷活動或廣告）的中繼資料。 Adobe Advertising會使用分類來分類原始Adobe Advertising資料，以便在您產生報表時能以不同的方式顯示資料（例如依廣告型別或促銷活動）。 分類構成中Adobe Advertising報告的基礎 [!DNL Analytics] 可與AMO量度搭配使用，例如 [!UICONTROL AMO Cost]， [!UICONTROL AMO Impressions]、和 [!UICONTROL AMO Clicks]、以及自訂和標準站上事件(例如 [!UICONTROL Visits]， [!UICONTROL Leads]， [!UICONTROL Orders]、和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [預期資料差異： [!DNL Analytics] 和Adobe Advertising](data-variances.md)
