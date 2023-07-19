---
title: 上傳轉換量度至 [!DNL Google Ads]
description: 瞭解如何將搜尋、社交和商務追蹤的轉換量度上傳至 [!DNL Google Ads].
exl-id: 88db66c2-12db-41cf-b6c4-ed821cb3b8ea
source-git-commit: 00f9e5e3892be305f5d7c69161bdb7609f13f1bf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# 上傳轉換量度至 [!DNL Google Ads]

*廣告商使用 [!DNL Google Ads] 僅限帳戶*

搜尋、社交和商務可選擇上傳至 [!DNL Google Ads] 其追蹤的所有轉換量度 [!DNL Google Ads] 使用Adobe Analytics同步的Adobe Advertising轉換追蹤服務和轉換量度的行銷活動。 此選項無法讓轉換可用於混合最佳化。 如果您想要將Adobe轉換用於混合最佳化，請參閱&quot;[啟用上傳目標至廣告網路](objective-upload-to-networks.md).」

每日上傳包括追蹤的 `gclid` 值、使用廣告商層級歸因模型定義的轉換值，以及時間戳記。 如果更新歸因模型，則下次上傳時會使用新模型，但不會更新過去的資料以使用新模型。

>[!NOTE]
>
>上傳內容不包含從摘要檔案上傳至Adobe Advertising的轉換量度。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Upload Conversions to Google Ads]**.

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 於 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](objective-upload-to-networks.md)
