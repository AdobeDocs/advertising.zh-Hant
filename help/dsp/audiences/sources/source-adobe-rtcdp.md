---
title: 搭配使用DSP整合 [!DNL Adobe] [!DNL Real-time CDP]
description: 瞭解如何啟用DSP以擷取您的 [!DNL Adobe] [!DNL Real-time CDP] 第一方區段。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 5d4dfa7976b1500bf65105cf8fcc6dc5d3e1ec65
workflow-type: tm+mt
source-wordcount: '540'
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

1. 在Adobe Experience Platform中，使用設定Advertising DSP目的地連線， [!UICONTROL Source Key] 在DSP來源設定中產生的值。

   如需啟用DSP目的地連線、選取區段及存取控制許可權的指示，請參閱&quot;[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).」

   來源電子郵件地址必須使用SHA-256演演算法執行雜湊處理。

1. 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在位置設定內)填入的區段，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

   這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

   雜湊電子郵件地址至通用ID的翻譯率應大於90%；的翻譯率 [!DNL RampIDs] 如果所有雜湊電子郵件地址都是唯一的，則尤其應為95%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，應將其轉譯為至少95個 [!DNL RampIDs] 或超過90種其他型別的通用ID。 較低的翻譯率是個問題。 如需區段計數可能變異的詳細資訊，請參閱&quot;[電子郵件ID與通用ID之間資料差異的原因](#universal-ids-data-variances).」

   如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

區段每24小時會重新整理一次。 不過，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 在到期之前從Real-Time CDP重新推送區段，以重新整理區段。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄概觀](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
