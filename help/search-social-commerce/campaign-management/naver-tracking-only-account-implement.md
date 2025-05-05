---
title: 實作 [!DNL Naver] 僅限追蹤的帳戶
description: 瞭解如何為您的 [!DNL Naver] 帳戶設定追蹤行銷活動，以便您可以追蹤、報告直接從廣告網路購買的廣告，並以視覺效果呈現其成效。
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 實作[!DNL Naver]只追蹤帳戶

僅&#x200B;*[!DNL Naver]個帳戶*

您可以建立[!DNL Naver]帳戶的追蹤行銷活動，以便直接從廣告網路購買廣告的追蹤、報告及視覺化成效。 搜尋、社交和Commerce不會將資料與廣告網路同步、自動上傳追蹤，也不會對帳戶投標。

追蹤行銷活動會復寫您現有的行銷活動、廣告群組和關鍵字。 您在「搜尋」、「社交」和「Commerce」中建立帳戶結構，並將追蹤新增至廣告網路內的原始行銷活動後，就可以上傳關鍵字或廣告的每日網路流量量度。 然後搜尋、Social和Commerce可以將您的轉換歸因於廣告和關鍵字。

您可以追蹤所有行銷活動以及任何個別行銷活動、廣告群組或關鍵字/廣告的績效量度。 您也可以在最基本、進階和協助報表中包含這些報表的相關資訊，以及其他廣告網路的資料。 不支援將量度匯出至Adobe Analytics，但搜尋、社交和Commerce可將您在 [!DNL Analytics][&#128279;](/help/integrations/analytics/analytics-data-in-advertising.md)中追蹤的量度同步至搜尋、社交和Commerce。

>[!NOTE]
>
>您無法將追蹤行銷活動新增至產品組合以進行最佳化。

1. 在搜尋、社交和Commerce中建立追蹤行銷活動：

   1. 建立[虛擬網路帳戶詳細資料](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)。 如果您在單一廣告網路中有多個帳戶，請在[!UICONTROL Accounts]檢視中將它們合併為一個帳戶。

      [!DNL Naver]不提供API支援，無法上傳追蹤引數至廣告網路。 不過，您可以使用大量表單產生追蹤引數，並在廣告網路中手動新增這些引數（步驟2）。 若要產生追蹤引數，您必須使用&quot;[!UICONTROL EF Redirect]&quot;追蹤方法。 您可以選擇新增任何想要的附加引數。

      搜尋、Social和Commerce會自動將引數`ev_cl={ef_uniqueid}`納入其為帳戶大量表單內產生的任何追蹤URL中。 此唯一ID可用來比對促銷活動資料與任何費用，以及您上傳的點選資料。

   1. 設定要追蹤的行銷活動：

      1. 在廣告網路中，建立大量表單檔案，其中包含您希望Search、Social和Commerce追蹤帳戶的所有實體及其必要的父實體。

         您可以包含關鍵字的相關資料，包括父促銷活動和廣告群組。

      1. 如有必要，請編輯大量表單檔案，使其遵循 [!DNL Naver] 帳戶[&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)所需的Search、Social和Commerce 大量表單格式。

      1. 在「搜尋」、「社交」和「Commerce」中，[上傳Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)。

         >[!NOTE]
         >
         >注意：搜尋、社交和Commerce不會將資料發佈至廣告網路帳戶。

1. 設定行銷活動的追蹤：

   1. 在搜尋、社交和Commerce中，[使用「[!UICONTROL Generate Tracking URLs]」的選項，下載新的Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)。

   使用&quot;[!UICONTROL Generate Tracking URLs]&quot;選項會以[!UICONTROL Base URL]值為首碼的搜尋、社交和Commerce追蹤程式碼，填入每個關鍵字的[!UICONTROL Destination URL]欄位。

   以下是含有追蹤的目的地URL範例：

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. 將下載的Bulksheet檔案中的[!UICONTROL Destination URL]值複製到網路上的相關關鍵字設定中。

      您可以將檔案上傳至廣告網路編輯器中的網路，藉此將URL新增至相關實體。 在這種情況下，您可能需要根據網路的資料需求移除一些欄。 否則，您必須在網路上手動輸入URL。

1. 定期從廣告網路下載您正在追蹤的關鍵字或廣告群組層級品牌廣告的每日累計點按和成本資料，然後以[必要格式](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)將點按和成本資料[&#128279;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)上傳到Search， Social， &amp; Commerce。

   包含完整的帳戶階層以及您要包含的任何量度。 搜尋、Social和Commerce會將上傳的資料與現有行銷活動中的資料比對。

1. （可選）如果您在網頁中使用Adobe Advertising轉換追蹤服務標籤來追蹤未在廣告網路上追蹤的轉換，則傳送包含每日彙總轉換資料的摘要檔案，以新增至您的追蹤行銷活動。

   如需詳細資訊，請聯絡您的Adobe客戶團隊。

在[!UICONTROL Accounts]、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]和[!UICONTROL Keywords]檢視中，所有已上傳的追蹤資料都可從[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]取得。 它也適用於[!UICONTROL Insights & Reports]檢視中的報告。

>[!MORELIKETHIS]
>
>* [附錄 —  [!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)的必要大量表單資料
>* [上傳 [!DNL Naver] 僅限追蹤帳戶](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)的流量和轉換量度
>* [僅追蹤帳戶 [!DNL Naver] 的量度資料需求](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的點選追蹤格式
