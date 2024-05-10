---
title: 啟用上傳目標至廣告網路
description: 瞭解如何將混合投資組合的目標上傳至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 啟用上傳目標至廣告網路

*廣告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 僅限帳戶*

*僅針對混合最佳化啟用的廣告商*

搜尋、社交和Commerce可上傳廣告商帳戶的產品組合目標至 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 以便將其用於混合最佳化。 您上傳的目標可做為帳戶層級和促銷活動層級自訂轉換目標的轉換動作。

啟用此選項會自動觸發上傳產品組合中的目標，其中包含具有智慧競標策略的行銷活動。 搜尋、社交和Commerce會在廣告網路上為每個適用的目標建立轉換。 轉換代表目標中的所有加權轉換量度。 每個轉換都有以下其中一個名稱：

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  位置 `<network_ID>` 是Search、Social和Commerce用於廣告網路的數值ID， `<objective_id>` 是數值目標ID，且 `<network_account_ID>` 是廣告網路帳戶或管理員帳戶的數值ID。

* （未來將廢止的舊格式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  位置 `<portfolio_id>` 是數值投資組合ID和 `<se_acctid/conversion_manager_se_acctid>` 是廣告網路帳戶或管理員帳戶的數值ID。

  在舊格式淘汰之前，您的Adobe帳戶團隊將與您合作，移轉廣告網路中現有的轉換動作名稱。 在移轉期間，新舊格式的上傳將同時執行。 建模和最佳化不受影響，因為新的轉換動作最初以「次要」（非最佳化）狀態出現，並具有90天的回填資料。

上傳至 [!DNL Google Ads] 在廣告商的時區中每天06:00發生。 上傳至 [!DNL Microsoft® Advertising] 在廣告商的時區中每天09:00發生。

>[!IMPORTANT]
>
>Google Ads和Microsoft Advertising通用事件追蹤(UET)標籤所追蹤的轉換不會重新上傳至廣告網路。 如果您將它們包含在目標中，請將其新增至廣告網路編輯器中的行銷活動目標。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Enable Objective Upload]**.

1. (廣告商使用 [!DNL Google Ads] 在歐洲經濟區(EEA)或英國(UK)做生意的帳戶；選擇性)如果您已向EEA和英國使用者收集同意，同意他們上傳資料以供廣告用途，請選取「 」旁的核取方塊 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

每日上傳完成後，您可以確認轉換動作會出現在廣告網路中。

>[!MORELIKETHIS]
>
>* [關於管理廣告商的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [上傳轉換量度至 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
