---
title: 搭配使用DSP整合 [!DNL Adobe] [!DNL Real-time CDP]
description: 瞭解如何啟用DSP以擷取您的 [!DNL Adobe] [!DNL Real-time CDP] 第一方區段。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID

*Beta功能*

將DSP整合用於 [此 [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hant)，是Adobe Experience Platform的一部分，可將雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

1. (若要將電子郵件地址轉換為 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))設定追蹤 [!DNL Analytics] 測量：

   1. （如果您尚未這麼做）全部完成 [實作的先決條件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 和 [追蹤URL中的AMO ID和EF ID](/help/integrations/analytics/ids.md).

   1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

      * **的 [!DNL RampIDs]：** 您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到閱覽的轉換。 請聯絡您的Adobe客戶團隊，他們將會為您提供註冊的相關指示。 [!DNL LiveRamp] [!DNL LaunchPad] 標籤來源 [!DNL LiveRamp] 驗證流量解決方案。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

1. [建立對象來源](source-manage.md) 將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何 [可用的通用ID格式](source-about.md).

   來源設定將包含自動產生的來源金鑰，您將在下一個步驟中使用。

1. 在Adobe Experience Platform中，使用「 」設定Advertising DSP目的地連線 [!UICONTROL Source Key] 在DSP來源設定中產生的值。

   如需啟用DSP目的地連線、選取區段及存取控制許可權的指示，請參閱&quot;[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).」

   來源電子郵件地址必須使用SHA-256演演算法執行雜湊處理。

1. 完成所有步驟後，請在對象庫中驗證（您從建立或編輯對象時可使用此對象庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段會在24小時內填入。 比較通用ID的數量與原始雜湊電子郵件地址的數量。

   雜湊電子郵件地址轉譯為通用ID的速率應大於90%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，則應將其轉譯為90個以上的通用ID。 90%或更低的翻譯率是個問題。 如需區段計數可能變異的詳細資訊，請參閱&quot;[電子郵件ID與通用ID之間資料差異的原因](#universal-ids-data-variances).」

   如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

區段每24小時會重新整理一次。 不過，區段中的包含會在30天後過期，以確保符合隱私權規範，因此請每隔30天或更短時間從Real-Time CDP重新推送受眾，以重新整理受眾。

>[!MORELIKETHIS]
>
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄概觀](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [手動匯入已驗證的區段，從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
