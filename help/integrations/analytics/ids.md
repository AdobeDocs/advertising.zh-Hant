---
title: ' [!DNL Analytics]使用的Adobe Advertising ID'
description: ' [!DNL Analytics]使用的Adobe Advertising ID'
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '1122'
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

EF ID是不重複Token，Adobe Advertising會使用它，將活動與個別瀏覽器或裝置層級的線上點選或廣告曝光建立關聯。 EF ID主要當作金鑰，用於將[!DNL Analytics]資料和Customer Journey Analytics資料傳送至Adobe Advertising，以在Adobe Advertising內最佳化報表和競標。

針對[!DNL Analytics]，EF ID儲存在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hant)或[!DNL rVar] （保留的[!DNL eVar]）維度(Adobe Advertising EF ID)中。

對於Customer Journey Analytics，EF ID儲存在`trackingIdentities`物件的`conversionDetails`屬性中，該物件是[&#x200B; [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)的一部分。

### EF ID格式 {#ef-id-formats}

>[!NOTE]
>
>EF ID區分大小寫。 如果[!DNL Analytics]或Customer Journey Analytics實作強制將URL追蹤轉換為小寫，則Adobe Advertising無法辨識EF ID。 這會影響Adobe Advertising競標和報告，但不會影響[!DNL Analytics]或Customer Journey Analytics內的Adobe Advertising報告。

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

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

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

### [!DNL Analytics]中的AMO ID Dimension

在Analytics報表中，您可以搜尋[!UICONTROL AMO ID]維度並使用[!UICONTROL AMO ID Instances]量度來尋找AMO ID資料。 [!UICONTROL AMO ID]維度內含所有擷取的AMO ID值，而[!UICONTROL AMO ID Instances]量度則表示網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按四次，但Analytics追蹤了七個網站專案，則[!UICONTROL AMO ID Instances]會是七(7)，[!UICONTROL Clicks]會是四(4)。

對於[!DNL Analytics]內的任何報告或稽核，最佳實務是使用AMO ID及其對應的執行個體。 如需詳細資訊，請參閱「在[和Adobe Advertising之間的預期資料差異」中的 [!DNL Analytics for Advertising]](data-variances.md#data-validation)的[!DNL Analytics]點進資料驗證。

## 關於Analytics分類

在[!DNL Analytics]中，[分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=zh-Hant)是指定追蹤代碼（例如帳戶、促銷活動或廣告）的中繼資料。 Adobe Advertising會使用分類來分類原始Adobe Advertising資料，以便在您產生報表時，可以不同方式（例如依廣告型別或促銷活動）顯示資料。 在[!DNL Analytics]中以Adobe Advertising報告為基礎的分類，可與AMO量度（例如[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]和[!UICONTROL AMO Clicks]）搭配使用，也可與自訂和標準站上事件（例如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）搭配使用。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [預期資料差異介於 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之間
