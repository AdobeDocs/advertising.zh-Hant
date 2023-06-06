---
title: 啟用上傳目標至廣告網路
description: 瞭解如何將混合投資組合的目標上傳至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 啟用上傳目標至廣告網路

*廣告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 僅限帳戶*

*僅針對混合最佳化啟用的廣告商*

如果您的廣告商帳戶設定為使用混合最佳化，則Adobe廣告可選擇上傳帳戶的產品組合目標至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 作為轉換，以便將其用於混合最佳化。

啟用此選項會自動觸發上傳包含具有智慧競標策略之行銷活動的產品組合。 搜尋、Social和Commerce會在廣告網路上為每個適用的產品組合和目標組合建立轉換。 每個轉換都有名稱 `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`，其中 `<portfolio_id>` 是數值投資組合ID和 `<se_acctid/conversion_manager_se_acctid>` 是廣告網路帳戶或管理員帳戶的數值ID。 轉換代表目標中的所有加權交易屬性。

上傳至 [!DNL Google Ads] 每日06:00 （在廣告商的時區）。 上傳至 [!DNL Microsoft® Advertising] 每日09:00 （在廣告商的時區）。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Enable Objective Upload]**.

   僅當您的廣告商帳戶設定為使用混合最佳化時，此選項才可用。 若要啟用混合最佳化，請聯絡您的Adobe帳戶團隊。

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 於 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [關於管理廣告商的交易屬性](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [上傳轉換量度至 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)

