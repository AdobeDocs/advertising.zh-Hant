---
title: 對象Source設定
description: 瞭解對象來源的設定。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# 對象Source設定

*Beta功能*

**[!UICONTROL Data Visibility Level]：**&#x200B;區段是否可供存取帳戶(*[!UICONTROL Advertiser]*)的單一廣告商使用，或可供存取帳戶&#x200B;*[!UICONTROL Account]*&#x200B;的所有廣告商使用。

**[!UICONTROL Advertiser]：** （僅限廣告商層級的可見度）可提供區段的廣告商。 從可存取該帳戶的廣告商清單中選取一個廣告商。

**[!UICONTROL Enter IMS Org Id]：** （僅限[!DNL Real-Time CDP]個來源） [!DNL Adobe Experience Platform]帳戶的Adobe Experience Cloud組織識別碼。

**[!UICONTROL Convert PII to the following IDs]：**&#x200B;您要將個人識別資訊(PII)轉換為的ID型別。 如果您選取多個型別，則產生的區段會填入每個所選ID型別的值（例如每個電子郵件地址的[!DNL RampID]和[!DNL Unified ID2.0]）。 據此套用資料費用。

對於[!DNL RampID]和[!DNL Unified ID2.0]，廠商會查詢每個電子郵件地址，檢視識別碼是否已存在，並將地址轉譯成相符識別碼（可用時）。 如果地址沒有ID，則會建立新的ID。

>[!NOTE]
>
>在單一位置中，您只能定位一種型別的ID。 若要依ID型別測試效能，請[為區段中的每個ID型別建立個別的位置](/help/dsp/campaign-management/placements/placement-create.md)。

* *[!DNL RampID]：*&#x200B;要將PII轉換為[!DNL RampID]。 您可以使用[!DNL RampIDs]來重新定位登入使用者並進行[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)測量。

* *[!DNL Unified ID2.0] (Beta)：*&#x200B;若要將PII轉換為[統一識別碼2.0](https://unifiedid.com)識別碼，以重新定位登入使用者。

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]：**&#x200B;將PII轉換為通用ID的服務合約條款。 您或DSP帳戶中的其他使用者必須接受條款一次，才能將資料轉換為新的ID型別。 若客戶擁有受管理的服務合約，您的Adobe客戶團隊將取得您的同意，並代表貴組織接受條款。 若要閱讀條款，請按一下&#x200B;**>**。 若要接受條款，請捲動至條款底部，然後按一下&#x200B;**[!UICONTROL Accept]**。

**[!UICONTROL Source Key]：** （唯讀；自動產生）您可以在客戶資料平台中用來建立目的地連線的來源金鑰，以將對象推送到Advertising DSP。 您可以將值複製到剪貼簿，貼到目的地連線設定或檔案中。

>[!MORELIKETHIS]
>
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [關於第一方對象來源](source-about.md)
>* [從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手動匯入已驗證的區段
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
