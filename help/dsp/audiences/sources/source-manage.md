---
title: 管理對象來源以啟用通用ID對象
description: 瞭解如何建立及管理來源，以從您的客戶資料平台匯入對象，並將其轉換為包含通用ID的區段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: f24aec0588f0298c5a3aa63226bd05bd4fa95f92
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# 管理對象來源以啟用通用ID對象

*Beta功能*

在DSP中，為您客戶資料平台中的每個第一方對象建立一個來源，您想要將其轉換為包含指定通用ID型別的區段。 您可以將區段匯入貴組織的DSP帳戶或廣告商帳戶。 系統會根據選取的通用ID型別套用資料費用。 建立來源後，需要執行其他步驟才能從每個客戶資料平台擷取對象。 請參閱程式結尾的註記以建立來源。

您稍後可以變更來源對象轉譯成的通用ID型別，並檢視變更記錄。

您也可以刪除來源。

## 建立對象來源

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 按一下 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 功能表，選取您的 [客戶資料平台](source-about.md)：

   * *[!UICONTROL RT-CDP]*：此 [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*：此 [!DNL ActionIQ] 客戶資料平台。

   * *[!UICONTROL Tealium CDP]*：（僅限已設定的使用者） [!DNL Tealium] 客戶資料平台。

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 輸入剩餘的 [來源設定](#source-settings).

   保留 [!UICONTROL Source Key] 所產生的值。 您稍後需要該值。

1. 按一下 **[!UICONTROL Save]**.

>[!NOTE]
>
>在您建立客戶資料平台的來源後，您將需要完成其他步驟。 請參閱 [從匯入對象的工作流程 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [從匯入對象的工作流程 [!DNL Tealium]](source-tealium.md).

## 變更對象來源的ID型別

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 將游標停留在來源列上並按一下 **[!UICONTROL Edit]**.

1. 變更 [為來源選取的ID](#source-settings).

1. 按一下 **[!UICONTROL Save]**.

## 刪除對象來源

刪除來源會移除透過來源轉譯的區段。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 將游標停留在來源列上並按一下 **[!UICONTROL Delete]**.

1. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

## 檢視對象來源的變更記錄

您可以檢視對象來源記錄變更的詳細資料，並可選擇將附註附加至記錄。

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 將游標停留在來源列上並按一下 **[!UICONTROL Change log]**.

1. （選擇性）若要在變更記錄中附加附註：

   1. 將游標停留在來源列上並按一下 **[!UICONTROL Add Notes]**.

   1. 輸入附註，然後按一下 **[!UICONTROL Save]**.

      長度上限為256個字元。

1. （選擇性）若要在較大的詳細資訊畫面中開啟記錄檔，請將游標停留在來源列上，然後按一下 **[!UICONTROL View Details]**.

## 對象來源設定 {#source-settings}

**[!UICONTROL Data Visibility Level]：** 區段是否可供可存取帳戶的單一廣告商使用(*[!UICONTROL Advertiser]*)或所有可存取帳戶的廣告商 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]：** （僅限廣告商層級的可見度）可取得區段的廣告商。 從可存取該帳戶的廣告商清單中選取一個廣告商。

**[!UICONTROL Enter IMS Org Id]：** ([!DNL Real-Time CDP] 僅來源)的Adobe Experience Cloud組織ID [!DNL Adobe Experience Platform] 帳戶。

**[!UICONTROL Convert PII to the following IDs]：** 您要將個人識別資訊(PII)轉換為的ID型別。 如果您選取多種型別，則產生的區段會填入每個所選ID型別的值(例如 [!DNL RampID] 和 [!DNL Unified ID2.0] （適用於每個電子郵件地址）。 據此套用資料費用。

的 [!DNL RampID] 和 [!DNL Unified ID2.0]，廠商會查詢每個電子郵件地址，檢視該ID是否已存在，並在地址可用時將其ID轉譯為相符的ID。 如果地址沒有ID，則會建立新的ID。

>[!NOTE]
>
>在單一位置中，您只能定位一種型別的ID。 若要依ID型別測試效能， [建立個別位置](/help/dsp/campaign-management/placements/placement-create.md) 區段中的每個ID型別。

* *[!DNL RampID]：* 將PII轉換為 [!DNL RampID]. 您可以使用 [!DNL RampIDs] 重新定位登入使用者和 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 測量。

* *[!DNL Unified ID2.0](Beta)：* 將PII轉換為 [統一識別碼2.0](https://unifiedid.com) 用於重新定位登入使用者的ID。

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]：** 將PII轉換為通用ID的服務合約條款。 您或DSP帳戶中的其他使用者必須接受條款一次，才能將資料轉換為新的ID型別。 若客戶擁有受管理的服務合約，您的Adobe客戶團隊將取得您的同意，並代表貴組織接受條款。 若要閱讀條款，請按一下 **>**. 若要接受條款，請捲動至條款底端，然後按一下 **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]：** （唯讀；自動產生）您可以在客戶資料平台中用來建立目的地連線的來源金鑰，以將對象推送至Advertising DSP。 您可以將值複製到剪貼簿，貼到目的地連線設定或檔案中。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](source-about.md)
>* [手動匯入已驗證的區段，從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
