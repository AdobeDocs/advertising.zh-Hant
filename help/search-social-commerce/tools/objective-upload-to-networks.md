---
title: 啟用物鏡上傳至 廣告
description: 瞭解如何將混合產品組合的目標上傳到 [!DNL Google Ads] 和 [!DNL Microsoft Advertising]。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 啟用物鏡上傳至 廣告

*僅擁有 [!DNL Google Ads] 帳號的廣告 [!DNL Microsoft Advertising] 商*

*僅啟用混合優化的廣告商*

Search、Social和商務可以將廣告商 帳戶投資組合的目標上傳，[!DNL Google Ads][!DNL Microsoft Advertising]因此您可以使用它們進行混合優化。您上傳的目標可作為帳戶級和行銷活動級自定義轉換目標的轉換操作。

啟用此選項會自動觸發包含採用智慧出價策略的廣告系列的組合中目標上傳。 Search、Social &amp; Commerce 為每個適用的目標建立廣告網路轉換。 轉換代表目標中的所有加權轉換量度。 每個轉換都有以下名稱之一：

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  其中，Search、Social &amp; Commerce 用於廣告網路的數值 ID，`<objective_id>`是`<network_ID>`數值目標 ID，`<network_account_ID>`並且是廣告網路 帳戶或經理帳戶的數值 ID。

* （日後將淘汰的舊格式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  其中 `<portfolio_id>` 是數值 作品集 ID， `<se_acctid/conversion_manager_se_acctid>` 是廣告網路 帳戶或经理帳戶的數值 ID。

  Adobe Systems 帳戶團隊將與您合作，在棄用舊格式之前在 廣告網路 內遷移現有的 轉換 操作名稱。 在遷移期間，新舊格式上傳將並行運行。 建模和優化不受影響，因為新轉換操作最初顯示為「輔助」 （未優化） 狀態，並具有 90 天的回填數據。

上傳將在 [!DNL Google Ads] 廣告商時區的每日 06：00 進行。 上傳將在 [!DNL Microsoft Advertising] 廣告商時區的每日 09：00 進行。

>[!IMPORTANT]
>
>Google Ads 和 Microsoft Advertising 通用事件跟踪 （UET） 標記跟蹤的轉化不會重新上傳到廣告網络。 如果您將這些维度包含在目標中，請將它們添加到廣告網路編輯者中的行銷活動目標中。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. 在主選單中，按下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**。

1. 選中 旁邊的 **[!UICONTROL Enable Objective Upload]**&#x200B;複選框。

1. （擁有 [!DNL Google Ads] 在歐洲經濟區 （EEA） 或英國 （UK） 開展業務的帳戶的廣告商;可選） 如果您已徵得EEA和英國使用者的同意，可以出於廣告目的上傳其數據，請選中 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 按兩下 **[!UICONTROL Save]**。

1. （如果您是在經理帳戶層級追踪您的轉化） [在> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**為您的**[!UICONTROL Search]&#x200B;經理帳戶](/help/search-social-commerce/admin/manager-accounts.md)添加憑據。

1. 確認每個目標（已命名 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` ）在兩天內出現在廣告網路上。

   在 [!DNL Google Ads] 編輯者中，查找您的 [轉換操作](https://support.google.com/google-ads/answer/11461796)。 在編輯者 [!DNL Microsoft Advertising] 中，查找您的 [轉換目標](https://help.ads.microsoft.com/#apex/ads/en/56709)。

   如有必要，請更新日期範圍以包含上傳日期。

## 目標缺失疑難解答

如果某個投資組合的目標（指定 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` ）未顯示在廣告網路上，請檢查以下內容：

* （[!DNL Google Ads]） 檢查是否應將轉換上載至帳戶或管理員層級。 如果它們應在管理員級別上傳：

   * 檢查 > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**中**[!UICONTROL Search]&#x200B;是否提供了管理器帳戶的憑據[!DNL Google Ads]。如有必要， [請添加管理器帳戶](/help/search-social-commerce/admin/manager-accounts.md)的憑據。

   * 檢查廣告網路 帳戶是否已包含相同的量度名稱。 如果是這樣，請重命名量度，以便可以創建正確的管理器級屬性。

* 檢查是否已選取作品集的「混合」選項，以及目標是否收入有效。

>[!MORELIKETHIS]
>
>* [關於管理廣告商轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [轉換量度上傳至 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
