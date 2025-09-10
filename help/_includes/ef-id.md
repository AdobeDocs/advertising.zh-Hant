---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

EF ID是不重複Token，Adobe Advertising會使用它，將活動與個別瀏覽器或裝置層級的線上點選或廣告曝光建立關聯。 EF ID主要當作金鑰，用於將[!DNL Analytics]資料和Customer Journey Analytics資料傳送至Adobe Advertising，以在Adobe Advertising內最佳化報表和競標。

針對[!DNL Analytics]，EF ID儲存在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或[!DNL rVar] （保留的[!DNL eVar]）維度(Adobe Advertising EF ID)中。

對於Customer Journey Analytics，EF ID儲存在`trackingIdentities`物件的`conversionDetails`屬性中，這是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。
