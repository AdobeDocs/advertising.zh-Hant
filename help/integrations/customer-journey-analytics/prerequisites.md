---
title: 將Adobe Advertising與Customer Journey Analytics整合的先決條件
description: 將Adobe Advertising與Customer Journey Analytics整合的先決條件
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 194675147b64af37de6373116f246f1e61388a23
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 將Adobe Advertising與Customer Journey Analytics整合的先決條件

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

* 同時具有[!DNL Analytics for Advertising]和Customer Journey Analytics的廣告商：

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [ [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有其他必要條件。

* 使用Customer Journey Analytics但不使用[!DNL Analytics for Advertising]的廣告商：

   * Adobe Experience Platform Web SDK資料庫： `alloy.js`

     用於Web SDK及Adobe Advertising廣告商帳戶的[!DNL Org ID]必須相同。 您可以在Adobe Experience Cloud Debugger[的](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)摘要標籤上找到此ID。

     ![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

     您需要來自Experience Platform網站管理員的支援，才能建立Experience Platform資料流和XDM結構描述。

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     您需要內部網頁分析人員的支援，才能設定與資料集的連線及設定報告。

>[!TIP]
>
>若要改善資料保真度，請使用每個程式庫的最新版本。

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* (Adobe Analytics使用者) [收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
