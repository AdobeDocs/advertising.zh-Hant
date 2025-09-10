---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID會在較不細微的層級追蹤每個不重複廣告組合，並用於[!DNL Analytics]和Customer Journey Analytics資料分類以及從Adobe Advertising擷取廣告量度（例如曝光數、點按數和成本）。

針對[!DNL Analytics]，AMO ID儲存在[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar維度(AMO ID)中。

對於Customer Journey Analytics，AMO ID儲存在`trackingCode`物件的`conversionDetails`屬性中，該物件是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。

AMO ID也稱為`s_kwcid`，有時發音為&quot;[!DNL squid]&quot;。
