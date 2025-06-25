---
title: 為潛在客戶的 [!DNL Google Ads] 增強型轉換建立轉換動作
description: 瞭解如何為潛在客戶的增強型轉換建立 [!DNL Google Ads] 轉換動作。
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 為潛在客戶的[!DNL Google Ads]增強型轉換建立轉換動作

僅&#x200B;*[!DNL Google Ads]個帳戶*

您可以針對要針對個別[!DNL Google Ads]帳戶追蹤的潛在客戶（而不是在經理帳戶層級追蹤的轉換），建立[!DNL Google Ads]增強型轉換的轉換動作。

1. 在主功能表中，按一下「**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**」，開啟「**[!UICONTROL Summary]**」索引標籤。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 指定[轉換動作設定](#conversion-action-settings-google)。

   1. 選取帳戶，然後選取轉換型別： *[!UICONTROL Import conversion]*。

   1. 按一下&#x200B;**[!UICONTROL Next]**。

   1. 指定轉換動作選項。

   1. 按一下&#x200B;**[!UICONTROL Generate]**。

1. 閱讀如何為潛在客戶的增強型轉換建立追蹤標籤的相關資訊，然後按一下&#x200B;**[!UICONTROL Next]**。

   建立轉換標籤，並視需要在您要追蹤轉換量度的網站上實作。 如需指示，請參閱下列內容：

   * 若要使用[!DNL Google]標籤，請參閱[為具有 [!DNL Google] 標籤](https://support.google.com/google-ads/answer/11347292)的銷售機會設定增強型轉換[!DNL Google Ads]中「設定[!DNL Google]標籤設定」的說明。

   * 若要使用[!DNL Google Tag Manager]，請參閱「[為具有 [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)的銷售機會設定增強型轉換」中的[!DNL Google Ads]指示，以「設定[!DNL Google]標籤設定」和「驗證您的設定並發佈容器」。

1. 按一下&#x200B;**[!UICONTROL Done].**

建立轉換動作並實施轉換追蹤標籤後，您就可以上傳組織擷取的離線轉換資料，並將其歸因於轉換動作。 請參閱&quot;[上傳離線轉換資料以取得增強型轉換](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)&quot;。

## 轉換動作設定 {#conversion-action-settings-google}

**[!UICONTROL Select an Account]：**&#x200B;適用的Google Ads帳戶。

**[!UICONTROL Type of Conversion]：**&#x200B;要追蹤的轉換型別：選取&#x200B;*[!UICONTROL Import conversion]*。 所有其他型別可用來針對其他轉換型別建立轉換追蹤標籤（而非轉換動作）。

**[!UICONTROL Conversion Name]：**&#x200B;轉換動作的唯一名稱。

**\[轉換類別\]：**&#x200B;轉換類別，例如&#x200B;*合格的銷售機會*&#x200B;或&#x200B;*註冊*。

**\[動作型別\]：**&#x200B;目標是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;或&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Value]：**&#x200B;如何測量每個轉換的[值](https://support.google.com/google-ads/answer/13064207)：

* *[!UICONTROL Use the same value for each conversion]，*&#x200B;要求您選取貨幣並輸入每次轉換的值。

* *[!UICONTROL Use a different value for each conversion]，*，要求您選取貨幣並為每次轉換輸入預設值。 在特定網頁上實作標籤時，您可以使用交易特定的值來變更標籤中的預設值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次點按或互動要計算多少轉換](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]：**&#x200B;記錄轉換的廣告互動後的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL View Through Conversion Window]：**&#x200B;使用者檢視您的廣告後，記錄瀏覽轉換的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL Attribution Model]：** [每個廣告互動獲得多少評分](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*&#x200B;或&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [上傳離線轉換資料以進行增強型轉換](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [針對潛在客戶](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)實作 [!DNL Google Ads] 增強型轉換
