---
title: 實作 [!DNL Google Ads] 最高成效行銷活動
description: 瞭解設定的工作流程 [!DNL Google Ads] 最高成效行銷活動。
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 實作 [!DNL Google Ads] 最高成效行銷活動

在 [!DNL Google Ads] 最高成效行銷活動，您不需要設定廣告群組、廣告或關鍵字。 反之，在行銷活動設定中，您需指定一或多個資產群組，包括標題、說明以及上傳的影像、標誌和 [!DNL YouTube videos]. [!DNL Google Ads] 自動結合資產，以根據管道提供廣告(例如 [!DNL YouTube]， [!DNL Gmail]，或 [!DNL Search])。

您可以在下列位置檢視現有的最高成效行銷活動，以表格和趨勢圖表格式呈現成效資料： [!DNL Campaigns] 檢視；資料在較低層級無法使用。 行銷活動層級的成效資料也可在報告和Adobe Analytics中使用(適用於具有 [Analytics整合](/help/integrations/analytics/overview.md). 若要檢視最高成效行銷活動的績效資料，請 [!DNL Analytics]，行銷活動必須使用 [已升級s_kwcid追蹤程式碼](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) （會追蹤促銷活動ID和廣告群組ID）。

>[!NOTE]
>
>* 您必須手動上傳所有影像檔案。 連結至 [!DNL Google Merchant Center] 不支援產品摘要。
>* 只有必要的設定可供使用。 如需選擇性的設定，請登入 [!DNL Google Ads] 編輯者。
>* 不支援列出群組。 若要管理和檢視清單群組的資料，請登入 [!DNL Google Ads] 編輯者。

## 設定步驟 [!DNL Google Ads] 最高成效行銷活動

您可以從以下網址個別設定最高成效行銷活動： [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 檢視。

1. [建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 使用行銷活動型別 **[!UICONTROL Performance Max]**.

   指定 [!UICONTROL Campaign Details]， [!UICONTROL Budget Options]， [!UICONTROL Campaign Targeting]、和 [!UICONTROL URL Options]. 選擇性地輸入 [!UICONTROL Negative Keywords]，輸入 [!UICONTROL Negative Websites]，和/或覆寫 [!UICONTROL Campaign Tracking] 選項。

1. 為行銷活動建立資產群組及上傳資產：

   1. 在行銷活動設定底部，按一下 **[!UICONTROL Manage Asset Groups]**.

   1. 指定第一個資產群組的設定，並上傳資產群組的影像、標誌和選用影片。

      另請參閱 [資產群組設定的說明](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) 以瞭解需求與規格。

   1. 視需要新增其他資產群組。

1. 按一下 **[!UICONTROL Post]**.

1. （選用）將行銷活動新增至混合專案組合以進行最佳化。
