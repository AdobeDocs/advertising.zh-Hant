---
title: 實作 [!DNL Google Ads] 動態搜尋廣告
description: 瞭解設定 [!DNL Google Ads] 動態搜尋廣告的工作流程。
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# 實作[!DNL Google Ads]動態搜尋廣告

*[!DNL Google Ads]只搜尋含有創意層級或關鍵字及創意層級追蹤的行銷活動*

動態搜尋廣告會使用您網站的內容（而非關鍵字）來決定何時顯示您的廣告。 您可以為廣告群組設定個別的動態搜尋目標，或選擇行銷活動層級設定，使用您的網站內容來鎖定您的廣告，藉此定義網站中內容用於鎖定動態搜尋廣告的頁面。

您可以個別設定動態搜尋廣告，也可以使用大量表單來設定。 下列指示包含建立個別實體的連結。

## 設定[!DNL Google Ads]動態搜尋廣告的步驟

1. [為動態搜尋廣告建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)：

   1. 一開始會將行銷活動預算設為每日搜尋行銷活動支出的10%。

      您可以在廣告證實其價值後增加預算。

   1. （如果您希望[!DNL Google Ads]根據網站內容顯示您的動態搜尋廣告）請在行銷活動設定的[!UICONTROL DSA Options]區段中，指定根網域和網域的語言。

      >[!NOTE]
      >
      >您的網域必須由[!DNL Google Ads]有機搜尋索引編制索引，才能定位。 此外，如果網域包含多種語言的頁面，而您想要鎖定所有頁面，請針對每種語言建立個別的行銷活動。

      如果您未使用網站網域來鎖定您的廣告，請為每個廣告群組建立動態搜尋目標（請參閱步驟4）。 您可以個別建立目標[&#128279;](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)，或使用[大量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

   1. 請確定行銷活動目標是搜尋頻道，而且只鎖定了[!DNL Google Ads]搜尋網路（不是顯示網路）。 這些設定可從[!UICONTROL Networks and Devices]標籤取得。

   1. （選擇性）在[!UICONTROL Negatives]索引標籤上排除關鍵字。

   1. （可選）設定行銷活動層級的追蹤範本，以覆寫帳戶層級的追蹤範本，但可以在較低層級覆寫。

      (使用Adobe Analytics且沒有伺服器端追蹤的廣告商)如果您想要在Analytics中加入搜尋、Social和Commerce反向摘要的追蹤，請將AMO ID追蹤程式碼新增至帳戶層級的附加引數，如此可將程式碼新增至最終URL。 檢視 [!DNL Analytics][&#128279;](/help/integrations/analytics/ids.md)使用的Adobe AdvertisingID。

1. [在行銷活動中建立廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，包括以下步驟：

   1. 將[!UICONTROL Ad Group Type]設為&#x200B;**[!UICONTROL Search Dynamic].**

   1. 設定所有廣告的預設競標。

      您可以覆寫個別動態搜尋目標的預設競標（如果設定）。

   1. （可選）設定廣告群組層級追蹤範本，以覆寫較高層級的任何追蹤範本，但可在廣告層級覆寫。

      如果您已在行銷活動層級新增Adobe Analytics追蹤，且想要將其納入廣告群組，請在此處新增。 請參閱步驟1e。

1. [在廣告群組中建立每個動態搜尋廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)。

   [!DNL Google Ads]會動態產生每個廣告的標題、顯示URL和登陸頁面URL。 您可以選擇將重新導向與追蹤新增至廣告層級追蹤範本，以覆寫較高層級的追蹤範本。
若要以廣告層級追蹤覆寫較高層級的任何Adobe Analytics追蹤，請在此處新增該追蹤。 請參閱步驟1e和2c。

1. （當您未在行銷活動設定的DSA選項區段中納入根網域和網域的語言時，此為必要專案；否則為選用專案）為廣告群組建立[動態搜尋目標](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)。 您可以選擇使用目標層級競標來覆寫廣告群組層級競標。

   目標會定義廣告網路是使用您網站中的所有頁面還是頁面子集來鎖定您的動態搜尋廣告。 若要最佳追蹤效能，請為每個動態搜尋目標設定一個廣告群組的行銷活動，並包含以所有條件為目標的廣告群組。

1. 必要時，[編輯行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)以調整行銷活動預算，並透過從行銷活動中排除其他關鍵字來調整流量。
