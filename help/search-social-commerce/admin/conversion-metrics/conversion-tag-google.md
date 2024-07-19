---
title: 建立 [!DNL Google Ads]的轉換標籤
description: 瞭解如何建立 [!DNL Google Ads] 轉換標籤。
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# 建立[!DNL Google Ads]的轉換標籤

您可以為要針對個別[!DNL Google Ads]帳戶追蹤，而不是在經理帳戶層級追蹤的新轉換建立轉換標籤。

若要產生現有轉換的轉換標籤，請使用廣告網路的編輯器。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 指定[轉換標籤設定](#conversion-tag-settings-google)。

   1. 選取帳戶，然後選取轉換型別。

   1. 按一下&#x200B;**[!UICONTROL Next]**。

   1. 指定轉換選項。

   1. 按一下&#x200B;**[!UICONTROL Generate]**。

1. 複製轉換標籤，並在您要追蹤轉換量度的網站上實作。

   請參閱「[2」的[!DNL Google Ads]說明中的「安裝[!DNL Google]標籤」。 設定您的Google標籤](https://support.google.com/google-ads/answer/12215519)。」

1. 按一下&#x200B;**[!UICONTROL Done].**

將標籤新增至您的網站並開始引發後，[!DNL Google Ads]會在網站上記錄轉換。 搜尋、社交和Commerce會每天同步轉換。 如需同步之資料的詳細資訊，請參閱[[!DNL Google Ads] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)。

## 轉換標籤設定 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]：**&#x200B;適用的Google Ads帳戶。

**[!UICONTROL Type of Conversion]：**&#x200B;要追蹤的轉換型別： *[!UICONTROL Click on a webpage element]*、*[!UICONTROL Calls to a phone number on your website]*&#x200B;或&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*。

**[!UICONTROL Conversion Name]：**&#x200B;轉換量度的唯一名稱。

**\[轉換類別\]：**&#x200B;轉換類別。 可用的類別因轉換型別而異。 對於&#x200B;*[!UICONTROL Calls to a phone number on your website]*&#x200B;和&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*，預設會選取&quot;[!UICONTROL Phone Call Lead]&quot;。

**\[動作型別\]：**&#x200B;目標是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;或&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Value]：**&#x200B;如何測量每個轉換的[值](https://support.google.com/google-ads/answer/3419241)：

* *[!UICONTROL Use the same value for each conversion]，*&#x200B;要求您選取貨幣並輸入每次轉換的值。

* *[!UICONTROL Use a different value for each conversion]，*，要求您選取貨幣並為每次轉換輸入預設值。 在特定網頁上實作標籤時，您可以使用交易特定的值來變更標籤中的預設值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次點按或互動要計算多少轉換](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]：**&#x200B;記錄轉換的廣告互動後的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL View Through Conversion Window]：**&#x200B;使用者檢視您的廣告後，記錄瀏覽轉換的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取&#x200B;**[!UICONTROL Custom]**&#x200B;並輸入數字。

**[!UICONTROL Attribution Model]：** [每個廣告互動獲得多少評分](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*、*[!UICONTROL Last click]*、*[!UICONTROL First click]*、*[!UICONTROL Linear]*、*[!UICONTROL Time decay]*&#x200B;或&#x200B;*[!UICONTROL Position based]*。

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
