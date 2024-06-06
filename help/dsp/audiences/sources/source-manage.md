---
title: 建立和管理對象來源以啟用通用ID對象
description: 瞭解如何建立及管理來源，以從您的客戶資料平台匯入對象，並將其轉換為包含通用ID的區段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# 建立對象來源以啟用通用ID對象

*Beta功能*

在DSP中，為您客戶資料平台中的每個第一方對象建立一個來源，您想要將其轉換為包含指定通用ID型別的區段。 您可以將區段匯入貴組織的DSP帳戶或廣告商帳戶。 系統會根據選取的通用ID型別套用資料費用。

若要從每個客戶資料平台擷取對象，還需要執行其他步驟。 請參閱程式結尾的註記。

## 建立對象來源

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 按一下 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 功能表，選取您的客戶資料平台：

   * *[!UICONTROL RT-CDP]*： [此 [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*：此 [[!DNL ActionIQ] 客戶資料平台](source-about.md).

   * *[!UICONTROL Tealium CDP]*：（僅限已設定的使用者） [[!DNL Tealium] 客戶資料平台](source-about.md).

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 輸入剩餘的 [來源設定](source-settings.md).

   保留 [!UICONTROL Source Key] 所產生的值。 您稍後需要該值。

1. 按一下 **[!UICONTROL Save]**.

>[!NOTE]
>
>在您建立客戶資料平台的來源後，您將需要完成其他步驟。 請參閱 [從匯入對象的工作流程 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [從匯入對象的工作流程 [!DNL Tealium]](source-tealium.md).

## 變更對象來源的ID型別

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 將游標停留在來源列上並按一下 **[!UICONTROL Edit]**.

1. 變更 [為來源選取的ID](source-settings.md).

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

>[!MORELIKETHIS]
>
>* [對象來源設定](source-settings.md)
>* [關於第一方對象來源](source-about.md)
>* [Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
