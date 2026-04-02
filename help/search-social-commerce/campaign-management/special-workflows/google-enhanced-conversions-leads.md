---
title: 對潛在客戶實作 [!DNL Google Ads] 增強型轉換
description: 瞭解為潛在客戶設定 [!DNL Google Ads] 增強型轉換的工作流程。
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
TQID: https://experienceleague.adobe.com/yFJJ662wcsm2KLzCIpxXo6F8nPsklVItHMTBk1h6wHg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 0%

---

# 對潛在客戶實作[!DNL Google Ads]增強型轉換

僅&#x200B;*[!DNL Google Ads]個帳戶*

潛在客戶的[[!DNL Google Ads] 增強型轉換](https://support.google.com/google-ads/answer/9888656)可讓您使用第一方轉換資料，將使用者對應至離線轉換。 在無法使用點選ID的環境中對潛在客戶使用增強型轉換，例如追蹤網站潛在客戶導致的電話或電子郵件銷售。

在「搜尋」、「社交」和「Commerce」中，您可以：

* 檢視潛在客戶的現有增強型轉換。

  搜尋、社交和Commerce會在廣告商時區的每日05:00同步潛在客戶的現有增強型轉換。

* 為潛在客戶建立增強的轉換。

* 上傳第一方離線轉換資料，以對應至潛在客戶的增強型轉換。

* 將潛在客戶的增強型轉換作為量度納入報表，並將加權量度納入最佳化目標。

若要使用此功能，請完成下列步驟。 建立轉換追蹤標籤與建立轉換動作的步驟可選擇性地予以回覆。

1. 在[!DNL Google Ads]內，選擇加入潛在客戶的增強型轉換：

   1. 開啟帳戶的轉換設定。

   1. 選取潛在客戶增強型轉換的選項，並接受服務條款。

   1. 選取要使用[!DNL Google]標籤或[!DNL Google Tag Manager]建立轉換標籤。

1. 設定並實作標籤以追蹤轉換動作。

   如需指示，請參閱[!DNL Google Ads]說明，為使用[標籤 [!DNL Google] 的銷售機會](https://support.google.com/google-ads/answer/11021502)或使用[ [!DNL Google Tag Manager]的](https://support.google.com/google-ads/answer/11347292)建立增強型轉換的標籤。

1. 為[搜尋、社交和Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)或[Google廣告](https://support.google.com/google-ads/answer/12216226)中的潛在客戶建立增強型轉換的轉換動作。

   如果您在Search、Social和Commerce中建立轉換動作，請將&#x200B;**轉換型別**&#x200B;指定為&#x200B;*匯入轉換*&#x200B;或&#x200B;*匯入。*

1. 視需要時常上傳第一方資料（包括雜湊電子郵件地址或電話號碼），以歸因於指定帳戶的轉換。 您可以從[搜尋、社交和Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)中或使用[!DNL Google Data Manager]完成此步驟。

   * 在「搜尋」、「社交」和「Commerce」中，您可以下載[!DNL Microsoft Excel]格式的範本、輸入轉換資料並將檔案儲存在本機，然後上傳編輯的檔案。 範本包含欄，以指出是否針對上傳資料至[!DNL Google]的廣告目的和廣告個人化目的給予使用者同意。

     所有上傳的資料已即時同步至[!DNL Google Ads]。

   * 如需使用[!DNL Google Data Manager]上傳資料的詳細資訊，請參閱&quot;[關於資料管理員](https://support.google.com/google-ads/answer/14639041)&quot;。

>[!MORELIKETHIS]
>
>* [為潛在客戶 [!DNL Google Ads] 增強型轉換建立轉換動作](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [上傳離線轉換資料以進行增強型轉換](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
