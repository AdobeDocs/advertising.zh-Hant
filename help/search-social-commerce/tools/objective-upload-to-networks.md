---
title: 啟用上傳目標至廣告網路
description: 瞭解如何將混合投資組合的目標上傳至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
exl-id: 75a1a804-ad6a-4dbc-9cde-30fe54476162
feature: Search Tools
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 啟用上傳目標至廣告網路

*廣告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 僅限帳戶*

*僅針對混合最佳化啟用的廣告商*

如果您的廣告商帳戶設定為使用混合最佳化，則Adobe Advertising可選擇上傳帳戶的產品組合目標至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 做為轉換，以便用於混合最佳化。

啟用此選項會自動觸發上傳包含具有智慧競標策略之行銷活動的產品組合。 搜尋、社交和商務會在廣告網路上為每個適用的產品組合和目標組合建立轉換。 每次轉換都有名稱 `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`，其中 `<portfolio_id>` 是數值投資組合ID和 `<se_acctid/conversion_manager_se_acctid>` 是廣告網路帳戶或管理員帳戶的數值ID。 轉換代表目標中的所有加權轉換量度。

上傳至 [!DNL Google Ads] 在廣告商的時區中每天06:00發生。 上傳至 [!DNL Microsoft® Advertising] 在廣告商的時區中每天09:00發生。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Enable Objective Upload]**.

   僅當您的廣告商帳戶設定為使用混合最佳化時，此選項才可用。 若要啟用混合最佳化，請聯絡您的Adobe客戶團隊。

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [關於管理廣告商的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [上傳轉換量度至 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
