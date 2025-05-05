---
title: 收集來自Advertising DSP Campaigns的點按和曝光資料
description: 瞭解如何使用Audience Manager畫素從Advertising DSP廣告擷取Cookie型曝光次數和點選事件
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# 從Advertising DSP Campaigns收集媒體曝光資料

*僅使用Advertising DSP的廣告商*

*僅整合Adobe Advertising-Adobe Audience Manager的廣告商*

本檔案說明如何使用Audience Manager畫素來標籤Advertising DSP廣告，以擷取Cookie型曝光次數和點選事件，以及使用資料所需的其他工作。

事件畫素不會擷取在無Cookie環境中發生的事件，例如行動應用程式和連線電視(CTV)。

## 步驟1：在Audience Manager中設定資料Source {#set-up-data-source}

在Audience Manager中，為DSP曝光數建立[資料來源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=zh-Hant)，然後按一下資料。 在每個事件標籤[&#128279;](#implement-dsp-pixels)中包含資料來源識別碼，以便所有追蹤的事件都歸因於資料來源。

>[!NOTE]
> 您可以在單一資料來源中，針對在多個DSP上執行的廣告行銷活動，收集其所有曝光次數和點按資料。

## 步驟2：在網頁上實作曝光和點選事件畫素 {#implement-dsp-pixels}

廣告商可以為自己的品牌建立和實施事件標籤。 如有需要，請聯絡您的Adobe Audience Manager顧問或Adobe客戶團隊以尋求支援。

>[!NOTE]
>
>如果您的組織使用[!DNL Analytics]追蹤，則您可能不需要Audience Manager點選追蹤。 Adobe Analytics會擷取點選訊號，並可透過[伺服器端轉送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=zh-Hant)傳送給Audience Manager。

### 畫素語法

事件畫素必須包括下列引數。

**曝光追蹤畫素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[可選的其他引數](#parameters)加上前置詞`&`

**點選追蹤畫素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[可選的其他引數](#parameters)加上前置詞`&`

其中：

* `[Audience Manager customer domain]`是會將曝光或點按事件傳送至[!DNL Adobe]的網域名稱。

* `[source id]`是您追蹤DSP曝光次數與點選資料的[資料來源](#set-up-data-source)識別碼。

* `[redirect URL]`是雙重編碼的重新導向URL。 如果您使用線上編碼工具(例如www.urlencoder.org)，請透過編碼器執行字串並重新編碼結果。

* `${TM_CAMPAIGN_ID_NUM}`是DSP中的數值促銷活動ID。 如果您想要以硬式編碼個別促銷活動ID，而不使用DSP巨集，請在促銷活動設定中找出該ID。

* 每個[引數](#key-value-pairs)都以`&`為前置詞，且格式為`d_parameter=parameter_id`，其中`parameter`會由新欄位的索引鍵值配對取代。 範例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 索引鍵值配對的引數 {#parameters}

**格式：** `d_parameter=parameter_id`

    其中：
    
    *引數的前置詞為&#39;&amp;&#39;
    
    * &#39;parameter&#39;會由新欄位
    
    的索引鍵/值組取代。範例： &#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

這兩種型別的畫素都可以包含其他引數做為&#x200B;*索引鍵值配對*，以收集特徵或提供其他報表的行銷活動中繼資料（例如位置名稱或行銷活動名稱）。 機碼值組包含兩個相關元素：定義資料集的常數&#x200B;*機碼*&#x200B;和屬於資料集的變數&#x200B;*值*。

在索引鍵/值組中，值變數可以是硬式編碼ID或&#x200B;*巨集*，這是獨立程式碼的一個小單位，當廣告標籤載入促銷活動和使用者追蹤時，會動態取代為對應的值。 對於促銷活動相關引數，您可以使用[DSP巨集](/help/dsp/campaign-management/macros.md)，而不是Audience Manager巨集，在所有廣告中使用單一畫素，連同對應的曝光數或點按資料一起傳送促銷活動屬性以進行Audience Manager。 您插入事件畫素的DSP巨集必須是包含在畫素中的機碼值組的適當值。 例如，若是`d_placement`鍵，您會使用DSP巨集`${TM_PLACEMENT_ID_NUM}`作為值，擷取Adobe Advertising巨集產生的位置ID。

如需Audience Manager支援曝光事件畫素的巨集清單，請參閱[透過畫素呼叫擷取促銷活動的曝光資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=zh-Hant#supported-key-value-pairs)。

如需Audience Manager支援點選事件畫素的巨集清單，請參閱[透過畫素呼叫擷取促銷活動的點選資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=zh-Hant)。

>[!TIP]
>
>* 最佳作法是納入行銷活動、位置、創意（廣告）和網站ID，讓您能夠使用行銷活動屬性來建立Audience Manager特徵。
>* 若要建立Audience Optimization報表，則需要其他引數。
>* 在索引鍵值配對中，將值取代為相關的[DSP巨集](/help/dsp/campaign-management/macros.md)，這樣您就可以在所有行銷活動的所有廣告中使用單一畫素。 例如，將`d_campaign=[%campaignID%]`變更為`d_campaign=${TM_CAMPAIGN_ID_NUM}`以擷取Adobe Advertising巨集產生的促銷活動ID。
>* 如有需要，您可以使用硬式編碼值建立自己的引數。 範例： `d_DSP=AdCloud`

曝光事件畫素的範例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 增加畫素的位置

#### 曝光追蹤畫素

將曝光事件追蹤畫素附加至您[!DNL DSP]行銷活動中的所有廣告。 您可以在下列任何位置執行此操作：

* 在版位層級，預設會將畫素套用至版位中的所有廣告。 在位置設定的「追蹤」區段中，在[[!UICONTROL Event pixels]欄位](/help/dsp/campaign-management/placements/placement-settings.md)中新增畫素。

* 在廣告層級，會覆寫任何位置層級事件畫素。 在廣告設定中，[在[!UICONTROL Pixel]標籤](/help/dsp/campaign-management/ads/ad-edit.md)上建立事件畫素。

* （適用於協力廠商廣告伺服器上的廣告）在廣告伺服器內的廣告層級。

#### 點選追蹤畫素

在廣告伺服器中，將點選事件畫素插入您通常插入廣告點進URL的任意位置（已附加編碼URL）。

## 步驟3：實作後工作

實施事件標籤後，資料會流入Audience Manager資料收集伺服器。 請先完成下列作業，您才可以在報表中使用資料。

### 建立[!DNL Amazon S3]貯體和資料Source

一旦您的資料位於Audience Manager伺服器上，您必須建立[!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])貯體，然後建立資料來源，所有畫素資料都會傳送至該來源。 如果您需要支援，請連絡您的Audience Manager顧問或[客戶服務](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=zh-Hant)。

### 建立Audience Manager特徵和區段

您的事件資料會以[未使用的訊號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=zh-Hant)流入Audience Manager。 從擷取的資料手動建立[規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=zh-Hant)，然後使用這些特徵建立[區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=zh-Hant)，您才可以在報表中使用資料。

為在DSP中展示特定創意內容的使用者填入使用者層級資料的特徵範例：

1. 將事件識別為`d_event = imp`。
1. 識別DSP促銷活動中的創作ID，然後將其對應至特徵做為`d_creative=[Creative ID]`。

![特徵建立畫面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
>* [傳送DSP媒體曝光資料給Adobe Audience Manager的總覽](overview.md)
>* [使用案例](use-cases.md)
