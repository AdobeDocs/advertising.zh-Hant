---
title: 對象來源設定
description: 瞭解對象來源的設定。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 對象來源設定

**[!UICONTROL Data Visibility Level]：** 區段是否可供可存取帳戶的單一廣告商使用(*[!UICONTROL Advertiser]*)或所有可存取帳戶的廣告商 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]：** （僅限廣告商層級的可見度）可取得區段的廣告商。 從可存取該帳戶的廣告商清單中選取一個廣告商。

**[!UICONTROL Enter IMS Org Id]：** ([!DNL Real-Time CDP] 僅來源)的Adobe Experience Cloud組織ID [!DNL Adobe Experience Platform] 帳戶。

**[!UICONTROL Convert PII to the following IDs]：** ([!DNL ActionIQ] 和 [!DNL Tealium] ID型別；您要將個人識別資訊(PII)轉換為此ID型別。 據此套用資料費用。

* *[!DNL RampID]：* 將PII轉換為RampID。 如果您選擇 *[!DNL RampID]*，您的區段會轉譯為 [!DNL RampIDs] 自動。

* *[!DNL Unified ID2.0]：* ([!DNL ActionIQ] （僅限來源）若要將PII轉換為 [統一識別碼2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]：** （唯讀；自動產生）您可以在客戶資料平台中用來建立目的地連線的來源金鑰，以將對象推送至Advertising DSP。 您可以將值複製到剪貼簿，貼到目的地連線設定或檔案中。

>[!MORELIKETHIS]
>
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [啟用通用ID合作夥伴的已驗證區段](source-universal-id.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
