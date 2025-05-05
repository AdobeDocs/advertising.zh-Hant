---
title: 實作 [!DNL Google Ads] 最高成效行銷活動
description: 瞭解設定 [!DNL Google Ads] 最高成效行銷活動的工作流程。
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 實施[!DNL Google Ads]個最高成效行銷活動

在[!DNL Google Ads]個最高成效行銷活動中，您未設定廣告群組、廣告或關鍵字。 反之，在行銷活動設定中，您需指定一或多個資產群組，包括標題、說明、以及上傳的影像、標誌和[!DNL YouTube videos]。 [!DNL Google Ads]會自動結合資產，以根據頻道（例如[!DNL YouTube]、[!DNL Gmail]或[!DNL Search]）提供廣告。

您可以在[!DNL Campaigns]檢視中檢視現有的最高成效行銷活動，以表格和趨勢圖表格式呈現成效資料；較低層級不會提供資料。 行銷活動層級的成效資料也可在報告和Adobe Analytics中使用（適用於具有[Analytics整合](/help/integrations/analytics/overview.md)的廣告商）。 若要在[!DNL Analytics]中檢視最高成效行銷活動的績效資料，行銷活動必須使用[升級的AMO ID追蹤代碼](/help/integrations/analytics/ids.md#amo-id-formats) （追蹤行銷活動ID和廣告群組ID）。

>[!NOTE]
>
>* 您必須手動上傳所有影像檔案。 不支援[!DNL Google Merchant Center]產品摘要的連結。
>* 只有必要的設定可供使用。 如需選擇性設定，請登入[!DNL Google Ads]編輯器。
>* 不支援列出群組。 若要管理和檢視清單群組的資料，請登入[!DNL Google Ads]編輯器。

## 設定[!DNL Google Ads]最高成效行銷活動的步驟

您可以從[!UICONTROL Campaigns] > [!UICONTROL Campaigns]檢視個別設定最高成效行銷活動。

1. [使用行銷活動型別&#x200B;**[!UICONTROL Performance Max]**&#x200B;建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)。

   指定[!UICONTROL Campaign Details]、[!UICONTROL Budget Options]、[!UICONTROL Campaign Targeting]和[!UICONTROL URL Options]。 選擇性地輸入[!UICONTROL Negative Keywords]、輸入[!UICONTROL Negative Websites]和/或覆寫[!UICONTROL Campaign Tracking]選項。

1. 為行銷活動建立資產群組及上傳資產：

   1. 在行銷活動設定底部，按一下&#x200B;**[!UICONTROL Manage Asset Groups]**。

   1. 指定第一個資產群組的設定，並上傳資產群組的影像、標誌和選用影片。

      請參閱資產群組設定[&#128279;](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)的說明，瞭解需求和規格。

   1. 視需要新增其他資產群組。

1. 按一下&#x200B;**[!UICONTROL Post]**。

1. （選用）將行銷活動新增至混合專案組合以進行最佳化。
