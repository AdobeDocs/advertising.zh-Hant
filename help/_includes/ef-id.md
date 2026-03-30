---
source-git-commit: 5f410215dfa9d1e76dec2c88efca3b2d786333a7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

## ADOBE ADVERTISING EF ID

EF ID是不重複Token，Adobe Advertising會使用它，將活動與個別瀏覽器或裝置層級的線上點選或廣告曝光建立關聯。 EF ID主要當作金鑰，用於將[!DNL Analytics]資料和Customer Journey Analytics資料傳送至Adobe Advertising，以在Adobe Advertising內最佳化報表和競標。

針對[!DNL Analytics]，EF ID儲存在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hant)或[!DNL rVar] （保留的[!DNL eVar]）維度(Adobe Advertising EF ID)中。

對於Customer Journey Analytics，EF ID儲存在`trackingIdentities`物件的`conversionDetails`屬性中，該物件是[&#x200B; [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)的一部分。

### EF ID格式 {#ef-id-formats}

請參閱「Adobe Analytics元件指南」中EF ID維度專案[的](https://experienceleague.adobe.com/zh-hant/docs/analytics/components/dimensions/amo-ef-id#dimension-items)格式。

>[!NOTE]
>
>EF ID區分大小寫。 如果[!DNL Analytics]或Customer Journey Analytics實作強制將URL追蹤轉換為小寫，則Adobe Advertising無法辨識EF ID。 這會影響Adobe Advertising競標和報告，但不會影響[!DNL Analytics]或Customer Journey Analytics內的Adobe Advertising報告。

<!--

Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
