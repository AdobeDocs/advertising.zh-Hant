---
title: 管理對象來源以啟用通用ID對象
description: 瞭解如何建立及管理來源，以從您的客戶資料平台匯入對象，並將其轉換為包含通用ID的區段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
TQID: https://experienceleague.adobe.com/us8NC8BEngb240MAW8hEo-DHGoW7MRDWvu0HedMsnFs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 0%

---

# 管理對象來源以啟用通用ID對象

在DSP中，為您客戶資料平台中要匯入或轉換為包含指定通用ID型別的區段的每個第一方對象建立來源。 您可以將區段匯入貴組織的DSP帳戶或廣告商帳戶。 將受眾轉換為通用ID時，會根據選取的通用ID型別套用費用。 建立來源後，需要執行其他步驟以從每個客戶資料平台串流來源對象。 請參閱程式結尾的註記以建立來源。

對於[!DNL AdFixus]以外的所有客戶資料平台，您稍後可以變更來源對象轉譯成的全域ID型別，並檢視變更記錄。

您也可以刪除來源。

## 建立對象來源

您可以為通用ID合作夥伴和帳戶或個別廣告商的每個組合建立一個來源。 例如，您可以有一個帳戶的[!UICONTROL RT-CDP]來源、一個廣告商1的[!UICONTROL RT-CDP]來源及一個廣告商2的[!UICONTROL RT-CDP]來源。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 按一下&#x200B;**[!UICONTROL Add Source]**。

1. 在[!UICONTROL Select a Type]功能表中，選取您的[客戶資料平台](source-about.md)：

   * *[!UICONTROL RT-CDP]*： [!DNL Adobe Real-Time CDP]。

   * *[!UICONTROL AdFixus ID]*： [!DNL AdFixus]客戶資料平台。 僅適用於澳洲的廣告商。

   * *[!UICONTROL ActionIQ]*： [!DNL ActionIQ]客戶資料平台。

   * *[!UICONTROL Amperity]*： [!DNL Amperity]客戶資料平台。

   * *[!UICONTROL Optimizely]*： [!DNL Optimizely]客戶資料平台。

   * *[!UICONTROL Tealium CDP]*： （僅限已設定的使用者） [!DNL Tealium]客戶資料平台。

1. 指定[!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]*&#x200B;或&#x200B;*[!UICONTROL Account]*。

1. 輸入其餘的[來源設定](#source-settings)。

   保留產生的[!UICONTROL Source Key]復本。 您稍後需要該值。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>在您建立客戶資料平台的來源後，必須完成其他步驟以匯入對象：
>* 針對[!DNL ActionIQ]來源，請與您的Adobe帳戶團隊合作。
>* 若為其他來源型別，請參閱<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), -->適用於 [!DNL AdFixus]](source-adfixus.md), the [workflow for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)的[工作流程、 [!DNL Amperity]](source-amperity.md)的[工作流程、 [!DNL Optimizely]](source-optimizely.md)的[工作流程以及 [!DNL Tealium]](source-tealium.md)的[工作流程。

## 變更對象來源的ID型別

*適用於[!DNL AdFixus]*&#x200B;以外的所有支援客戶資料平台

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 將游標停留在來源資料列上，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 變更為來源](#source-settings)選取的[ID。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 刪除對象來源

刪除來源會移除透過來源匯入的區段，包括所有轉譯的ID。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 將游標停留在來源資料列上，然後按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

## 檢視對象來源的變更記錄

您可以檢視對象來源記錄變更的詳細資料，並可選擇將附註附加至記錄。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 將游標停留在來源資料列上，然後按一下&#x200B;**[!UICONTROL Change log]**。

1. （選擇性）若要在變更記錄中附加附註：

   1. 將游標停留在來源資料列上，然後按一下&#x200B;**[!UICONTROL Add Notes]**。

   1. 輸入備註，然後按一下&#x200B;**[!UICONTROL Save]**。

      長度上限為256個字元。

1. （選擇性）若要在較大的詳細資訊畫面中開啟記錄檔，請將游標停留在來源列上，然後按一下&#x200B;**[!UICONTROL View Details]**。

## 對象來源設定 {#source-settings}

**[!UICONTROL Data Visibility Level]：**&#x200B;區段是否可供存取帳戶(*[!UICONTROL Advertiser]*)的單一廣告商使用，或可供存取帳戶&#x200B;*[!UICONTROL Account]*&#x200B;的所有廣告商使用。

**[!UICONTROL Advertiser]：** （僅限廣告商層級的可見度）可提供區段的廣告商。 從可存取該帳戶的廣告商清單中選取一個廣告商。

**[!UICONTROL Enter IMS Org Id]：** （僅限[!DNL Real-Time CDP]個來源） [!DNL Adobe Experience Platform]帳戶的Adobe CX Enterprise組織識別碼。

**[!UICONTROL Convert PII to the following IDs]：** （除了[!DNL AdFixus]之外，可用於所有支援的客戶資料平台）您將用來轉換個人識別資訊(PII)的ID型別。 如果您選取多個型別，則產生的區段會填入每個所選ID型別的值（例如每個電子郵件地址的[!DNL RampID]和[!DNL Unified ID2.0]）。 據此套用資料費用。

對於[!DNL RampID]和[!DNL Unified ID2.0]，廠商會查詢每個電子郵件地址，檢視識別碼是否已存在，並將地址轉譯成相符識別碼（可用時）。 如果地址沒有ID，則會建立新的ID。

>[!NOTE]
>
>在單一位置中，您只能定位一種型別的ID。 若要依ID型別測試效能，請[為區段中的每個ID型別建立個別的位置](/help/dsp/campaign-management/placements/placement-create.md)。

* *[!DNL RampID]：*&#x200B;要將PII轉換為[!DNL RampID]。 您可以使用[!DNL RampIDs]來重新定位登入使用者並進行[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)測量。

* *[!DNL Unified ID2.0]：*&#x200B;若要將PII轉換為[統一識別碼2.0](https://unifiedid.com)識別碼，以重新定位登入使用者。

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]：**&#x200B;將PII轉換為通用ID的服務合約條款。 您或DSP帳戶中的其他使用者必須接受條款一次，您才能匯入ID、將資料轉換為新的ID型別或目標ID型別。對於擁有受管服務合約的客戶，您的Adobe帳戶團隊取得您的同意，並代表貴組織接受條款。 若要閱讀條款，請按一下&#x200B;**>**。 若要接受條款，請捲動至條款底部，然後按一下&#x200B;**[!UICONTROL Accept]**。

**[!UICONTROL Source Key]：** （唯讀；自動產生）來源金鑰，您可以在客戶資料平台中用來建立目的地連線，以將對象推送至Advertising DSP。 您可以將值複製到剪貼簿，貼到目的地連線設定或檔案中。 與將讓受眾串流到DSP的團隊共用值。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](source-about.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [將使用者ID從 [!DNL Adobe Real-Time CDP] 轉換為通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [將使用者ID從 [!DNL Amperity] 轉換為通用ID](/help/dsp/audiences/sources/source-amperity.md)
>* [將使用者ID從 [!DNL Optimizely] 轉換為通用ID](/help/dsp/audiences/sources/source-optimizely.md)
>* [將使用者ID從 [!DNL Tealium] 轉換為通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [從 [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)匯入第一方區段
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
