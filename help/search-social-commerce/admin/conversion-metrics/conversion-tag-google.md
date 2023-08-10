---
title: 建立轉換標籤 [!DNL Google Ads]
description: 瞭解如何建立 [!DNL Google Ads] 轉換標籤。
feature: Conversions
source-git-commit: 395421c69214c3b0370523909047a924af23ea55
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 建立轉換標籤 [!DNL Google Ads]

您可以針對要個別追蹤的新轉換，建立轉換標籤 [!DNL Google Ads] 帳戶，不會在經理帳戶層級追蹤。

若要產生現有轉換的轉換標籤，請使用廣告網路的編輯器。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 指定 [轉換標籤設定](#conversion-tag-settings-google).

   1. 選取帳戶，然後選取轉換型別。

   1. 按一下 **[!UICONTROL Next]**.

   1. 指定轉換選項。

   1. 按一下 **[!UICONTROL Generate]**.

1. 複製轉換標籤，並在您要追蹤轉換量度的網站上實作。

   請參閱「安裝 [!DNL Google] 標籤」 [!DNL Google Ads] 「的說明[2. 設定您的Google標籤](https://support.google.com/google-ads/answer/12215519).」

1. 按一下 **[!UICONTROL Done].**

將標籤新增至您的網站並開始引發後， [!DNL Google Ads] 會記錄網站上的轉換。 搜尋、社交和商務會每天同步轉換。 如需已同步資料的詳細資訊，請參閱&quot;[[!DNL Google Ads] 搜尋、社交和商務中的轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## 轉換標籤設定 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]：** 適用的Google Ads帳戶。

**[!UICONTROL Type of Conversion]：** 要追蹤的轉換型別： *[!UICONTROL Click on a webpage element]*， *[!UICONTROL Calls to a phone number on your website]*，或 *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]：** 轉換量度的唯一名稱。

**\[轉換類別\]：** 轉換類別。 可用的類別因轉換型別而異。 的 *[!UICONTROL Calls to a phone number on your website]* 和 *[!UICONTROL Clicks to your number on your mobile website]*， &quot;[!UICONTROL Phone Call Lead]已依預設選取「 」。

**\[動作型別\]：** 目標是否為 *[!UICONTROL Primary action used for bidding optimization]* 或 *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]：** 如何測量 [每次轉換的值](https://support.google.com/google-ads/answer/3419241)：

* *[!UICONTROL Use the same value for each conversion]，* 這要求您選取貨幣並輸入每次轉換的值。

* *[!UICONTROL Use a different value for each conversion]，* 這要求您選取貨幣，並為每次轉換輸入預設值。 在特定網頁上實作標籤時，您可以使用交易特定的值來變更標籤中的預設值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次點按或互動要計數的轉換次數](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* 或 *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]：** 記錄轉換的廣告互動後的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取 **[!UICONTROL Custom]** 並輸入數字。

**[!UICONTROL View Through Conversion Window]：** 使用者檢視您的廣告後記錄瀏覽轉換的最大天數。 對於搜尋、顯示和購物行銷活動，期間可以是1至90天。 選取數字或選取 **[!UICONTROL Custom]** 並輸入數字。

**[!UICONTROL Attribution Model]：** [每個廣告互動獲得多少評分](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*， *[!UICONTROL Last click]*， *[!UICONTROL First click]*， *[!UICONTROL Linear]*， *[!UICONTROL Time decay]*，或 *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] 搜尋、社交和商務中的轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
