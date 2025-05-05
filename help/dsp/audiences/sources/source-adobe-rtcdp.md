---
title: 使用DSP與 [!DNL Adobe] [!DNL Real-time CDP]的整合
description: 瞭解如何啟用DSP以擷取您的 [!DNL Adobe] [!DNL Real-time CDP]第一方區段。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 將使用者ID從[!DNL Adobe Real-Time CDP]轉換為通用ID

*Beta功能*

使用DSP與[ [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hant) (屬於Adobe Experience Platform的一部分)的整合，將雜湊電子郵件地址轉換為通用識別碼以用於目標定位廣告。

1. （若要將電子郵件地址轉換為[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）設定[!DNL Analytics]測量的追蹤：

   1. （如果您尚未這樣做）完成實作 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)的所有[必要條件，以及在您的追蹤URL](/help/integrations/analytics/ids.md)中的AMO ID和EF ID。

   1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

      * **對於[!DNL RampIDs]：**，您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到瀏覽次數的轉換。 請連絡您的Adobe客戶團隊，他們將會指示您從[!DNL LiveRamp]驗證流量解決方案註冊[!DNL LiveRamp] [!DNL LaunchPad]標籤。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

1. [建立對象來源](source-manage.md)以將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何[可用的通用ID格式](source-about.md)。

   來源設定將包含自動產生的來源金鑰，您將在下一個步驟中使用。

1. 在Adobe Experience Platform中，使用在DSP來源設定中產生的[!UICONTROL Source Key]來設定Advertising DSP目的地連線。

   如需啟用DSP目的地連線、選取區段及存取控制許可權的指示，請參閱「[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)」。

   來源電子郵件地址必須使用SHA-256演演算法執行雜湊處理。

1. 驗證在您的對象資料庫中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或版位設定中建立或編輯對象時，可使用此資料庫）有區段正在填入，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

   這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。 如需有關可接受的ID轉譯率以及區段計數可能有所差異的資訊，請參閱[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)。

區段每24小時會重新整理一次。 不過，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 在到期之前從Real-Time CDP重新推送區段，以重新整理區段。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[啟用通用ID的支援](/help/dsp/audiences/universal-ids.md)&quot;。

若要疑難排解轉換程式的問題，請連絡您的Adobe客戶團隊或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄總覽](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
