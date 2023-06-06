---
title: 關於廣告網路帳戶
description: 瞭解Search、Social和Commerce中的廣告網路帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 關於廣告網路帳戶

*僅限代理商帳戶管理員、Adobe帳戶管理員和管理員使用者角色*

搜尋、Social和Commerce可以在支援的廣告網路上追蹤任何廣告商帳戶。 若要啟用帳戶追蹤，您必須建立對應的帳戶記錄。 您必須為任何型別的帳戶設定帳戶詳細資料，無論是Search、Social還是Commerce與其同步還是最佳化其廣告上的競標和預算。

## 透過API同步的帳戶

*[!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising] (先前稱為 [!DNL Bing Ads])， [!DNL Yahoo! Display Network]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] 帳戶*

搜尋、Social和Commerce同步(*同步*)廣告網路帳戶，以便追蹤、報告及視覺化廣告效能。 適用於所有廣告網路，但不包括 [!DNL Yahoo! Display Network]，您可以選擇在Search、Social和Commerce中管理您帳戶的促銷活動； [!DNL Yahoo! Display Network]，促銷活動為唯讀。 對於所有廣告網路，您可以透過將最佳化功能新增至產品組合，以最佳化受管理帳戶中廣告的競標。

若要啟用帳戶同步處理，帳戶記錄必須包含帳戶存取認證並啟用（作用中）。

在同步期間，「搜尋」、「社交」和「商務」會提取廣告商的促銷活動結構和支援的促銷活動實體，包括其在「搜尋」、「社交」和「商務」中管理或報告的大部分屬性。 其中不包含點按資料，也不包含在Search、Social和Commerce外部輸入的競標和競標修飾元（會單獨收集）。 搜尋、Social和Commerce會每天自動同步一次您的廣告網路帳戶，並且每當您在其中一個廣告網路上偵測到新行銷活動時，也會同步一次。 此外，它會立即將搜尋、社交和商務內對行銷活動資料所做的所有變更傳送至廣告網路。 您可以視需要選擇要求手動同步。

如需建立和編輯同步化行銷活動的詳細資訊，請參閱「Campaign Management」一章。

## 僅限追蹤的帳戶

*[!DNL Naver]帳戶*

追蹤行銷活動可讓您追蹤、報告並視覺化您直接從廣告網路購買之廣告的績效。 Search、Social和Commerce不會將資料與廣告網路同步、對帳戶投標，也不會提供任何型別的最佳化或模擬。

若要允許搜尋、社交和商務將轉換歸因於點選，請在帳戶記錄中設定追蹤選項並啟用帳戶記錄。 然後，您可以使用大量表單產生廣告和關鍵字的追蹤URL，並在 [!DNL Naver] 廣告管理員。

檢視更多關於「 」的資訊 [!DNL Naver] 僅限追蹤的行銷活動，請參閱&quot;[實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).」

>[!MORELIKETHIS]
>
>* [管理廣告網路帳戶](ad-network-account-manage.md)
>* [管理商家中心帳戶](merchant-account-manage.md)
>* [更新的s\_kwcid追蹤程式碼 [!DNL Google Ads] 帳戶](update-skwcid-google.md)

