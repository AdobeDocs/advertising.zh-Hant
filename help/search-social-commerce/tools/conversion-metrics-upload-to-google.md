---
title: 上傳轉換量度至 [!DNL Google Ads]
description: 瞭解如何將搜尋、社交和商務追蹤的轉換量度上傳至 [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 上傳轉換量度至 [!DNL Google Ads]

*廣告商使用 [!DNL Google Ads] 僅限帳戶*

搜尋、社交和商務可選擇上傳至 [!DNL Google Ads] 其追蹤的所有轉換量度 [!DNL Google Ads] 使用Adobe Advertising轉換追蹤服務的行銷活動。 此選項無法讓轉換可用於混合最佳化。 如果您想將Adobe轉換用於混合最佳化，請參閱&quot;[啟用上傳目標至廣告網路](objective-upload-to-networks.md).」

每日上傳包括追蹤的 `gclid` 值、使用廣告商層級歸因模型定義的轉換值，以及時間戳記。 如果更新歸因模型，下次上傳時將會使用新模型，但不會更新過去的資料以使用新模型。

>[!NOTE]
>
>上傳內容不包含從摘要檔案上傳至Adobe Advertising的轉換量度。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Upload Conversions to Google Ads]**.

1. (在歐洲經濟區(EEA)或英國(UK)經營業務的廣告商；選擇性)如果您已向EEA和英國使用者收集同意，可上傳其資料以供廣告用途，請選取「 」旁的核取方塊 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](objective-upload-to-networks.md)
