---
title: 啟用上傳目標至廣告網路
description: 瞭解如何將混合投資組合的目標上傳至 [!DNL Google Ads] 和 [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: aaad3eb6cd33f4342c46ffb244227a00fbcb4e44
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# 啟用上傳目標至廣告網路

*廣告商使用 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 僅限帳戶*

*僅針對混合最佳化啟用的廣告商*

搜尋、社交和Commerce可上傳廣告商帳戶的產品組合目標至 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 以便將其用於混合最佳化。 您上傳的目標可做為帳戶層級和促銷活動層級自訂轉換目標的轉換動作。

啟用此選項會自動觸發上傳產品組合中的目標，其中包含具有智慧競標策略的行銷活動。 搜尋、社交和Commerce會在廣告網路上為每個適用的目標建立轉換。 轉換代表目標中EF ID （點選ID）層級的所有加權轉換量度。 的 [!DNL Google Ads] 按一下，EF ID就是 [!DNL Google Ads] `gclid`；用於 [!DNL Microsoft Advertising] 按一下，EF ID就是 [!DNL Microsoft Advertising] `msclkid`. 由於此點按ID，轉換資料可以對應至特定關鍵字，然後點按時間。

每個上傳的轉換都有以下其中一個名稱：

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  位置 `<network_ID>` 是Search、Social和Commerce用於廣告網路的數值ID， `<objective_id>` 是數值目標ID，且 `<network_account_ID>` 是廣告網路帳戶或管理員帳戶的數值ID。

* （未來將廢止的舊格式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  位置 `<portfolio_id>` 是數值投資組合ID和 `<se_acctid/conversion_manager_se_acctid>` 是廣告網路帳戶或管理員帳戶的數值ID。

  在舊格式淘汰之前，您的Adobe帳戶團隊將與您合作，移轉廣告網路中現有的轉換動作名稱。 在移轉期間，新舊格式的上傳將同時執行。 建模和最佳化不受影響，因為新的轉換動作最初以「次要」（非最佳化）狀態出現，並具有90天的回填資料。

上傳至 [!DNL Google Ads] 在廣告商的時區中每天06:00發生。 上傳至 [!DNL Microsoft Advertising] 在廣告商的時區中每天09:00發生。

>[!IMPORTANT]
>
>Google廣告和Microsoft Advertising通用事件追蹤(UET)標籤追蹤的轉換不會重新上傳至廣告網路。 如果您將它們包含在目標中，則必須將它們新增至廣告網路編輯器中的行銷活動目標。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 選取旁邊的核取方塊 **[!UICONTROL Enable Objective Upload]**.

1. (廣告商使用 [!DNL Google Ads] 在歐洲經濟區(EEA)或英國(UK)做生意的帳戶；選擇性)如果您已向EEA和英國使用者收集同意，同意他們上傳資料以供廣告用途，請選取「 」旁的核取方塊 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 按一下 **[!UICONTROL Save]**.

1. （如果在經理帳戶層級追蹤您的轉換） [為您的管理員帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 確認每個目標 — 已命名 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`  — 會在廣告網路的兩天內顯示。

   在 [!DNL Google Ads] 編輯者，查詢您的 [轉換動作](https://support.google.com/google-ads/answer/11461796). 在 [!DNL Microsoft Advertising] 編輯者，查詢您的 [轉換目標](https://help.ads.microsoft.com/#apex/ads/en/56709).

   如有必要，請更新日期範圍以包含上傳日期。

## 如何計算加權目標

傳遞至廣告網路的加權目標為所收集的所有量度值的總和，但不包括由追蹤的轉換 [!DNL Google Ads] 或由 [!DNL Microsoft Advertising] 通用事件追蹤(UET)標籤。 此值是使用為廣告商的Search、Social和Commerce帳戶設定的歸因方法來計算。

例如，假設目標的目標量度是權重為25的購物車新增次數，而您的協助量度包括權重為1的GGL_Lead和收入，以及權重為0.5的下載次數。

![加權目標的範例](/help/search-social-commerce/assets/objective-example.png "加權目標的範例")

假設關鍵字導致專案組合執行下列動作：

* 10個購物車新增
* 收入$500
* 下載50次
* 5 GGL_Lead

GGL_Lead不會包含在計算/上傳中，因為這是Google的廣告追蹤量度。 因此，加權目標值的計算方式為((10 x 25) + (500 x 1) + (50 x 0.5)) = 775。

>[!TIP]
>
>您可以在廣告網路的報表中檢視Adobe Advertising加權收入資料。 根據最佳實務，比較加權收入與 [!DNL Google Ads] 「全部同意 (由conv. 時間)」量度或 [!DNL Microsoft Advertising] 量度「全部」 收入」，區段至O_ACS_OBJ*量度。<!--clarify -->

在廣告網路的編輯器中

## 疑難排解缺少的目標

如果目標 — 已命名 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`  — 如果您的其中一個產品組合未出現在廣告網路上，請檢查下列專案：

* ([!DNL Google Ads])檢查轉換是否應上傳至客戶或經理層級。 若應在管理員層級上傳：

   * 檢查的認證 [!DNL Google Ads] 經理帳戶提供於 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. 如有需要， [新增管理員帳戶的認證](/help/search-social-commerce/admin/manager-accounts.md).

   * 檢查廣告網路帳戶是否已包含相同的量度名稱。 如果有，則重新命名量度，以便建立正確的管理員層級屬性。

* 檢查是否已選取產品組合的「混合」選項，以及目標是否具有有效的收入。

>[!MORELIKETHIS]
>
>* [關於管理廣告商的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [上傳轉換量度至 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
