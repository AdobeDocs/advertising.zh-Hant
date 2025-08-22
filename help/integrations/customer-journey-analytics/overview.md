---
title: Adobe Advertising與Adobe Customer Journey Analytics之間整合的概述
description: 瞭解將Adobe Advertising與Adobe Customer Journey Analytics整合的選項。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: 37c0485189c9bf084d4051fec501a1b2128687ec
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Adobe Advertising與Customer Journey Analytics之間整合的概觀

<!-- title? If I change, change refs throughout -->

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

Adobe Advertising已與Adobe Customer Journey Analytics整合，以進行雙向資料共用和報告。 您有兩個選項可設定整合：

* 同時具有[!DNL Analytics for Advertising]和Customer Journey Analytics的廣告商具有透過[!DNL Analytics for Advertising]提供的相同功能，並在Customer Journey Analytics中新增視覺效果。

  您仍可使用Adobe Experience Platform Web SDK (`alloy.js`)或Adobe Experience Cloud Identity Service (`visitorAPI.js`)追蹤點進事件。 使用Advertising DSP的廣告商仍會使用JavaScript程式碼片段來追蹤瀏覽事件。 Customer Journey Analytics中可用的資料包括：

   * 來自Customer Journey Analytics中Adobe Advertising的行銷活動績效資料

   * 由Customer Journey Analytics中的[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Meta]追蹤的網站活動和轉換

   * 來自Adobe Advertising中[!DNL Analytics]的歸因資料，可用於最佳化和報告

  在此使用案例中，除了選擇性[收集AMO ID和EF ID的歷史資料以用於Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)之外，您不需要執行任何額外的步驟。

* （即將推出測試版功能） Customer Journey Analytics的廣告商若沒有[!DNL Analytics for Advertising]，則可在Adobe Advertising與Customer Journey Analytics之間原生交換下列資料，方法是使用Adobe Experience Platform Web SDK (`alloy.js`)追蹤點進和檢視事件。 資料可用於行銷活動、廣告群組、套件、位置和關鍵字層級。

   * 來自Customer Journey Analytics中Adobe Advertising的行銷活動績效資料

     **注意：**&#x200B;來自[!DNL Apple]和[!DNL Tiktok]的資料無法使用。

   * 由Customer Journey Analytics中的[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Meta]追蹤的網站活動和轉換

   * Adobe Advertising中Customer Journey Analytics的歸因資料，可用於最佳化和報告

  **注意：**&#x200B;目前沒有可用的有機資料。<!-- Does that belong somewhere up above? -->

  在此使用案例中，使用Web SDK追蹤網站事件（使用Cookie、雜湊IP位址或通用ID），並將網站事件歸因於[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Meta]中的付費媒體活動，以及Adobe DSP。 您也可以使用Adobe Experience Platform進行資料收集。

## 如何啟動Adobe Advertising與Customer Journey Analytics之間的原生整合

請聯絡您的Adobe客戶團隊，他們將會完成開始所需的初始設定，並將幫助您根據組織的需求規劃實施與資料使用。

>[!MORELIKETHIS]
>
>* [必要條件](prerequisites.md)
>* (Adobe Analytics使用者) [收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
