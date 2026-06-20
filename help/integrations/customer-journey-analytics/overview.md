---
title: Adobe Advertising與Adobe Customer Journey Analytics之間整合的概述
description: 瞭解將Adobe Advertising與Adobe Customer Journey Analytics整合的選項。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
TQID: https://experienceleague.adobe.com/nxn5AcKCc-xm-k5LXOcKIquNKyoXbt3soR5nhQR0w-E
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 358bcf190b36bd3c01e33a3d5762361a4a015393
workflow-type: tm+mt
source-wordcount: 498
ht-degree: 0%

---

# Adobe Advertising與Customer Journey Analytics之間整合的概觀

<!-- title? If I change, change refs throughout -->

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

Adobe Advertising已與Adobe Customer Journey Analytics整合，以進行雙向資料共用和報告。 您有兩個選項可設定整合：

* 同時具有[!DNL Analytics for Advertising]和Customer Journey Analytics的廣告商具有透過[!DNL Analytics for Advertising]提供的相同功能，並在Customer Journey Analytics中新增視覺效果。

  您仍可使用Adobe Experience Platform Web SDK (`alloy.js`)或Adobe Experience Cloud Identity Service (`visitorAPI.js`)追蹤點進事件。 使用Advertising DSP的廣告商仍會使用JavaScript程式碼片段來追蹤瀏覽事件。 Customer Journey Analytics中可用的資料包括：

   * 來自Customer Journey Analytics中Adobe Advertising的行銷活動績效資料

   * 由[!DNL Google Ads]和[!DNL Microsoft Advertising]在Customer Journey Analytics中追蹤的網站活動和轉換，每日更新

   * 來自Adobe Advertising中[!DNL Analytics]的歸因資料，可用於最佳化和報告

  在此使用案例中，您仍應選擇性[收集AMO ID和EF ID的歷史資料，以用於Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* 具有Customer Journey Analytics但不具有[!DNL Analytics for Advertising]的廣告商可以使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)，以原生方式在Adobe Advertising和Customer Journey Analytics之間交換資料。 您可以使用Cookie、雜湊IP和通用ID （[!DNL LiveRamp RampIDs]和ID5 ID）追蹤網站事件，並將網站事件歸因於付費媒體活動。 行銷活動、廣告群組、套件、位置和關鍵字層級提供下列資料：

   * 來自Customer Journey Analytics中Adobe Advertising的行銷活動績效資料

     **注意：**&#x200B;來自[!DNL Apple]和[!DNL Tiktok]的資料無法使用。

   * 由Customer Journey Analytics中的[!DNL Google Ads]和[!DNL Microsoft Advertising]追蹤的網站活動和轉換

   * Adobe Advertising中Customer Journey Analytics的歸因資料，可用於最佳化和報告

  在此使用案例中，使用Web SDK追蹤網站事件（使用Cookie、雜湊IP位址或通用ID），並將網站事件歸因於[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Meta]和Adobe DSP中的付費媒體活動。 您也可以使用Adobe Experience Platform進行資料收集。

## 報表資料型別的定義

* **事件層級資料：**&#x200B;時間戳記事件，例如工作階段、頁面檢視、潛在客戶表單提交和應用程式提交。

* **摘要資料：**&#x200B;彙總的報告資料，例如，廣告平台、行銷活動、刊登、曝光數、點選數和成本。

* **分類/維度資料：**&#x200B;報表維度，例如Adobe Advertising行銷活動名稱、投資組合名稱或位置ID。 您可以依分類/維度查詢（篩選）事件層級資料和摘要資料。

## 如何啟動Adobe Advertising與Customer Journey Analytics之間的原生整合 {#integration-cja-initiate}

請聯絡您的Adobe客戶團隊，他們將會完成開始所需的初始設定，並將幫助您根據組織的需求規劃實施與資料使用。

>[!MORELIKETHIS]
>
>* [必要條件](prerequisites.md)
>* [由 [!DNL Customer Journey Analytics]](ids.md)使用的Adobe Advertising ID
>* [設定資料收集、資料傳輸及報告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising量度和維度](advertising-data-in-cja.md)
>* （Adobe Analytics使用者） [收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
>* [疑難排解](troubleshooting.md)
