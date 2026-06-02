---
title: （新UI）為潛在客戶的 [!DNL Google Ads] 增強型轉換建立轉換動作
description: 瞭解如何為潛在客戶的增強型轉換建立 [!DNL Google Ads] 轉換動作。
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# （新UI）為潛在客戶的[!DNL Google Ads]增強型轉換建立轉換動作

*Beta功能*

僅&#x200B;*[!DNL Google Ads]個帳戶*

您可以針對要針對個別[!DNL Google Ads]帳戶追蹤的潛在客戶（而不是在經理帳戶層級追蹤的轉換），建立[!DNL Google Ads]增強型轉換的轉換動作。

建立轉換動作並實作轉換追蹤標籤後，您可以[上傳組織擷取的離線轉換資料](conversions-upload-offline-enhanced-conversions.md)，並將其歸因於轉換動作。

[!DNL Microsoft Advertising]帳戶不提供支援。

## 建立轉換動作

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Set up Conversion]**。

1. 指定[轉換動作設定](#conversion-action-settings-google)。

   1. 選取[!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*。

   1. 選取帳戶，然後選取轉換型別： *[!UICONTROL Import conversion]*。

   1. 按一下&#x200B;**[!UICONTROL Next]**。

   1. 指定轉換動作選項。

   1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

   1. 按一下&#x200B;**[!UICONTROL Generate]**。

1. 閱讀如何為潛在客戶的增強型轉換建立追蹤標籤的相關資訊，然後按一下&#x200B;**[!UICONTROL Next]**。

   您必須建立轉換標籤，並視需要在您要追蹤轉換量度的網站上實作。 您還需要啟用潛在客戶的增強型轉換，並同意客戶資料條款與條件。 如需指示，請參閱[!DNL Google Ads]指示，以「[設定 [!DNL Google] 標籤以取得潛在客戶](https://support.google.com/google-ads/answer/11021502)的增強型轉換」。

   若要追蹤交易特定轉換值，請[自訂您的事件片段](https://support.google.com/google-ads/answer/6095947)。

1. 按一下&#x200B;**[!UICONTROL Close].**

## 轉換動作設定 {#conversion-action-settings-google}

### 設定路徑區段

**[!UICONTROL Setup Method]：**&#x200B;動作型別： *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]：**&#x200B;廣告網路： *[!UICONTROL Google]*。

### 「轉換詳細資訊」區段

**[!UICONTROL Select Account]：**&#x200B;適用的[!DNL Google Ads]帳戶。

**[!UICONTROL Type of conversions]：**&#x200B;要追蹤的轉換型別：選取&#x200B;*[!UICONTROL Import conversion]*。 所有其他型別可用來針對其他轉換型別建立轉換追蹤標籤（而非轉換動作）。

### 「轉換設定」區段

**[!UICONTROL Conversion Name]：**&#x200B;轉換動作的唯一名稱。

**[!UICONTROL Goal Category]：**&#x200B;轉換類別，例如&#x200B;*合格的銷售機會*&#x200B;或&#x200B;*註冊*。

**[!UICONTROL Preferred Action optimization]：**&#x200B;目標是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;還是&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Conversion Value]：**&#x200B;如何測量每個轉換的[值](https://support.google.com/google-ads/answer/13064207)：

* *[!UICONTROL Use the same value for each conversion]，*&#x200B;要求您選取貨幣並輸入每次轉換的值。

* *[!UICONTROL Use different values for each conversion]，*，要求您選取貨幣並為每次轉換輸入預設值。 在特定網頁上實作標籤時，您可以使用交易特定的值來變更標籤中的預設值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次點按或互動要計算多少轉換](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*。

**[!UICONTROL Click-Through Conversion Window]：**&#x200B;記錄轉換的廣告互動後的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL View-Through Conversion Window]：**&#x200B;使用者檢視您的廣告後，記錄瀏覽轉換的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL Attribution Model]：** [決定每個廣告互動獲得多少評分的歸因模型](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*&#x200B;或&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [（新使用者介面）上傳增強型轉換的離線轉換資料](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [上傳離線轉換資料以進行增強型轉換](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [針對潛在客戶](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)實作 [!DNL Google Ads] 增強型轉換
