---
title: （新UI）關於廣告網路帳戶
description: 瞭解新的搜尋、社交和Commerce UI中的廣告網路帳戶。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# （新UI）關於廣告網路帳戶

搜尋、社交和Commerce可以在支援的廣告網路上追蹤任何廣告商帳戶。 若要啟用帳戶追蹤，您必須建立對應的帳戶記錄。 您必須為任何型別的帳戶設定帳戶詳細資料，無論Search、Social和Commerce是否與其同步，或最佳化其廣告的出價和預算。

## 透過API同步的帳戶

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （先前為[!DNL Bing Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和現有的[!DNL Baidu]帳戶*

搜尋、Social和Commerce會同步（*同步*）支援的廣告網路帳戶，以便您可以追蹤、報告和視覺化廣告的效能。 對於[!DNL Yahoo! Display Network]以外的所有廣告網路，您可以選擇在Search、Social和Commerce中管理您帳戶的行銷活動；[!DNL Yahoo! Display Network]，行銷活動為唯讀。 針對所有廣告網路，您可以允許最佳化功能，將行銷活動新增至產品組合，以最佳化受管理帳戶中行銷活動的出價、行銷活動預算及行銷活動競標策略目標。

若要啟用帳戶同步處理，帳戶記錄必須包含帳戶存取認證，並且必須啟用（作用中）。

同步期間，搜尋、Social和Commerce會提取廣告商的促銷活動結構和支援的促銷活動實體，包括其在Search、Social和Commerce中管理或報告的大部分屬性。 其中不包含點按資料，也不包含在Search、Social和Commerce外部輸入的競標和競標修飾詞，這些資料會單獨收集。 搜尋、Social和Commerce會每天自動同步一次您的廣告網路帳戶，每當在其中一個廣告網路偵測到新促銷活動時，也會進行同步。 此外，它會立即將所有從「搜尋」、「社交」和「Commerce」內所做的行銷活動資料變更傳送至廣告網路。 您可以視需要選擇要求手動同步。

如需建立和編輯同步化行銷活動的詳細資訊，請參閱「行銷活動管理」一章。

## 手動上傳資料的帳戶

針對Search、Social和Commerce不提供API支援的線上廣告網路，您可以上傳行銷活動內容和離線成本、點按次數和轉換資料，以用於報表和效能模擬。 搜尋、Social和Commerce不會將資料與廣告網路同步、提供自動競標，也不會提供任何型別的最佳化，但可讓您簡化跨管道分析，並找出手動最佳化的機會。

## 以範本為基礎的僅限追蹤帳戶

*僅供現有[!DNL Naver]帳戶使用*

追蹤行銷活動可讓您追蹤、報告並視覺化您直接從廣告網路購買之廣告的績效。 搜尋、Social和Commerce不會將資料與廣告網路同步、提供自動競標，也不會提供任何型別的最佳化或模擬。

若要允許搜尋、社交和Commerce將轉換歸因於點選，請在帳戶記錄中設定追蹤選項並啟用帳戶記錄。 然後，您可以使用大量表單產生廣告和關鍵字的追蹤URL，並在[!DNL Naver]廣告管理員中手動新增追蹤URL。

您無法在Search、Social和Commerce中設定新的[!DNL Naver]帳戶。 請參閱[!DNL Naver]只追蹤行銷活動的詳細資訊，請參閱[實作 [!DNL Naver] 只追蹤帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)。

>[!MORELIKETHIS]
>
>* [透過API連線管理廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [管理資料上傳的廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [僅管理 [!DNL Naver] 追蹤帳戶](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [管理商家中心帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
