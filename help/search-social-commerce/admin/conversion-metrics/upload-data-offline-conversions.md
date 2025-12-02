---
title: 上傳離線轉換資料以增強轉換
description: 瞭解如何上傳第一方離線轉換資料，以對應至 [!DNL Google Ads] 潛在客戶的增強型轉換和 [!DNL Microsoft Advertising] 增強型轉換。
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# 上傳離線轉換資料以增強轉換

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

您可以上傳第一方離線轉換資料（包括雜湊電子郵件地址和電話號碼），以對應至潛在客戶的現有[[!DNL Google Ads] 增強型轉換](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)和[[!DNL Microsoft Advertising] 增強型轉換](https://help.ads.microsoft.com/#apex/ads/en/60178)。 所有上傳的資料都會即時同步至廣告網路。

## 上傳資料以增強轉換

1. 在主功能表中，按一下「**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**」，然後按一下「**[!UICONTROL Upload]**」標籤。

1. 選取廣告網路，然後選取帳戶。

1. （選擇性）若要以[格式下載包含所有](#enhanced-conversions-leads-data)必要資料欄位[!DNL Microsoft Excel]的範本，請按一下&#x200B;**[!UICONTROL View Template]**，然後依照瀏覽器的正常程式下載檔案。

   您可以編輯檔案以包含您的資料並儲存變更，然後在下一個步驟中上傳檔案。

1. 按一下&#x200B;**[!UICONTROL Choose File]**，然後選取要從裝置或網路上傳的檔案。

## 已上傳檔案的必要資料 {#enhanced-conversions-leads-data}

### 表格上方的資料

`Parameters:TimeZone=insert_timezone`

請在此位置或在每一列的&quot;[!UICONTROL Conversion Time]&quot;欄中輸入帳戶的時區。 使用a\) ([!DNL Google Ads only]) [支援的時區ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b\) GMT時差，如+或 — 和4位數時間差（例如，紐約為–0500，柏林為+0100，格林威治標準時間為+000）。

### [!DNL Google Ads]的資料表資料行與值

| 欄 | 說明 |
| ------ | ----------- |
| 電子郵件 | 使用者的電子郵件地址，必須使用SHA-256演演算法執行雜湊處理。 每一列都必須包含電子郵件值或電話號碼值。 |
| 電話號碼 | 使用者電話號碼，必須使用SHA-256演演算法執行雜湊處理。 它必須包含國碼，而且可能包含破折號和其他符號。 每一列都必須包含電子郵件值或電話號碼值。 |
| 轉換名稱 | （必要）轉換動作的名稱。 |
| 轉換時間 | （必要）轉換事件發生的時間採用[支援的時間格式](https://support.google.com/google-ads/answer/7014069#prepare_data)。 如果您未在資料表格上方的`Parameters:TimeZone=insert_timezone`行中加入帳戶的時區ID，請使用a\) [支援的時區ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b\) GMT時差（以+或 — 表示）和4位數的時間差（例如，紐約為–0500，柏林為+0100，格林威治標準時間為+000），來加入每列的時區。 |
| 轉換值 | （必要）數值轉換值。 |
| 轉換貨幣 | 轉換事件的貨幣代碼。 |
| 廣告使用者資料 | (適用於歐洲經濟區(EEA)或英國(UK)的使用者相關資料)指出是否針對傳送使用者資料至[!DNL Google]以進行廣告個人化目的而授予使用者同意。 值可包含`Granted`、`Denied`或\[null\] （會以[!DNL Google Ads]形式傳送至`Unspecified`）。 **注意：** [!DNL Google Ads]目前並未針對潛在客戶的增強型轉換強制同意，但日後可能會強制同意。 |
| 廣告Personalization | (適用於歐洲經濟區(EEA)或英國(UK)的使用者相關資料)指出是否針對傳送使用者資料至[!DNL Google]以用於廣告目的而授予使用者同意。 值可包含`Granted`、`Denied`或\[null\] （會以[!DNL Google Ads]形式傳送至`Unspecified`）。 **注意：** [!DNL Google Ads]目前並未針對潛在客戶的增強型轉換強制同意，但日後可能會強制同意。 |

### [!DNL Microsoft Advertising]的資料表資料行與值

如需使用範本的詳細指示，請參閱[https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852)。

| 欄 | 說明 |
| ------ | ----------- |
| 轉換名稱 | （必要）轉換目標的名稱。 |
| 轉換時間 | （必要）轉換事件發生時的時間。 如果您未在資料表格上方的`Parameters:TimeZone=insert_timezone`行中加入帳戶的時區ID，則請使用GMT時差包含每列的時區，如+或 — 和4位數的時間差（例如，紐約為–0500，柏林為+0100，格林威治標準時間為+000）所示。 如需各城市的時區清單，請參閱[https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones)，但請確定您使用此處指定的格式，而非時區清單中的格式。 |
| 轉換值 | （必要）數值轉換值。 |
| 轉換貨幣 | 轉換事件的貨幣代碼。 |
| Microsoft點按ID | 關聯的唯一[!DNL Microsoft]點按識別碼(MSCLKID)。 對於增強的離線轉換，此欄位可能為空白。 |
| 雜湊電子郵件地址 | 使用者的電子郵件地址，必須使用SHA-256演演算法執行雜湊處理。 若要增強離線轉換，每一列必須包含雜湊電子郵件地址值或雜湊電話號碼值。 |
| 雜湊電話號碼 | 使用者電話號碼，必須使用SHA-256演演算法執行雜湊處理。 它必須包含國碼，而且可能包含破折號和其他符號。 若要增強離線轉換，每一列必須包含雜湊電子郵件地址值或雜湊電話號碼值。 |

>[!MORELIKETHIS]
>
>* [針對潛在客戶 [!DNL Google Ads] 實作](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)增強型轉換
>* [實作 [!DNL Microsoft Advertising] 增強的離線轉換](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [為潛在客戶 [!DNL Google Ads] 增強型轉換建立轉換動作](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [將搜尋、社交和Commerce追蹤的轉換量度上傳至 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
