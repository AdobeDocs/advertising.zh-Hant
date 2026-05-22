---
title: 從 [!DNL AdFixus]匯入第一方區段
description: 瞭解如何將包含 [!DNL AdFixus] 通用ID的 [!DNL AdFixus] 第一方區段匯入至DSP。
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# 從[!DNL AdFixus]匯入第一方區段

*僅適用於澳洲的廣告商*

使用Advertising DSP與[!DNL AdFixus]的整合，匯入您的[!DNL AdFixus]通用ID以及目標廣告的區段對應。[!DNL AdFixus] ID僅在澳洲提供。 DSP不會將[!DNL AdFixus]個ID變更為其他ID型別，也不會將其他ID型別轉換為[!DNL AdFixus]個ID。 DSP不收取匯入ID的費用。

將[!DNL AdFixus]區段匯入至DSP後，您就可以將位置鎖定在[!DNL AdFixus] ID和來自[!DNL AdFixus]的特定第一方區段。 您也可以將[!DNL AdFixus]區段新增至可重複使用的對象。 任何區段的詳細資料都包含適用的[!DNL AdFixus] ID計數。

您可以在自訂報表中檢視具有[!DNL AdFixus] ID之使用者的曝光數、點選數、頻率和其他量度。 具有[!DNL Analytics for Advertising]的廣告商也可以從Adobe Analytics檢視[!DNL AdFixus] ID的瀏覽資料，以及來自DSP中Adobe Analytics的資料。

1. 使用[!DNL AdFixus]將您組織的第一方資料轉換為具有[!DNL AdFixus] ID的區段。

   這需要具有[!DNL AdFixus]和有效授權金鑰的個別帳戶。 您還需要針對網站屬性和網域實作[!DNL AdFixus]特定程式碼。 直接使用[!DNL AdFixus]產生具有ID的區段。

1. （具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)的廣告商）為[!DNL Analytics]測量設定追蹤：

   1. （如果您尚未這樣做）完成實作 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)的所有[必要條件，以及在您的追蹤URL](/help/integrations/analytics/ids.md)中的AMO ID和EF ID。

   1. 在您的網頁上部署[!DNL AdFixus]專屬的程式碼，以符合從桌上型電腦和行動網頁瀏覽器（但不包括行動應用程式）上的[!DNL AdFixus] ID轉換至瀏覽次數。

1. 匯入您的第一方[!DNL AdFixus]區段：

   1. [建立[!UICONTROL Type] **[!UICONTROL AdFixus ID]**&#x200B;的對象來源](source-manage.md)。 您必須同意服務合約條款。

      來源設定將包含自動產生的來源金鑰。

   1. 與您的[!DNL AdFixus]團隊共用來源金鑰，好讓他們可以將所需的區段串流到DSP。

1. 在對象庫的[!UICONTROL First Party Segments]區段中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在位置設定中建立或編輯對象時，可使用此區段）確認區段已填入。 比較[!DNL AdFixus] ID數目與[!DNL AdFixus]內的使用者ID數目。

   區段一建立，即可在DSP中使用。

區段會重新整理，並可供每三小時鎖定目標一次，雖然DSP中顯示的計數會每24小時重新整理一次。 **注意：**&#x200B;區段中的包含專案會在您於[!DNL AdFixus]中設定的指定到期期間後到期。 在到期之前從[!DNL AdFixus]重新推播您的區段，以重新整理區段。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄總覽](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
