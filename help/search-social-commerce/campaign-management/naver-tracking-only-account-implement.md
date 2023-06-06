---
title: 實作 [!DNL Naver] 僅限追蹤的帳戶
description: 瞭解如何為設定追蹤行銷活動 [!DNL Naver] 帳戶，以便您可以追蹤、報告並視覺化您直接從廣告網路購買之廣告的績效。
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# 實作 [!DNL Naver] 僅限追蹤的帳戶

*[!DNL Naver]僅限帳戶*

您可以為您的建立追蹤行銷活動 [!DNL Naver] 帳戶，以便您可以追蹤、報告並視覺化您直接從廣告網路購買之廣告的績效。 搜尋、Social和Commerce不會將資料與廣告網路同步、自動上傳追蹤，也不會對帳戶投標。

追蹤行銷活動會復寫您現有的行銷活動、廣告群組和關鍵字。 您在「搜尋」、「Social」和「Commerce」中建立帳戶結構，並將追蹤新增至廣告網路內的原始行銷活動後，您就可以上傳關鍵字或廣告的每日網路流量量度。 然後搜尋、Social和Commerce可以將您的轉換歸因於廣告和關鍵字。

您可以追蹤所有行銷活動以及任何個別行銷活動、廣告群組或關鍵字/廣告的效能量度。 您也可以在最基本、進階和協助報表中包含這些廣告網路的相關資訊，以及其他廣告網路的資料。 不支援將量度匯出至Adobe Analytics，但搜尋、社交和商務可以同步 [您正在追蹤的量度 [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) 至搜尋、社交和商務。

>[!NOTE]
>
>您無法將追蹤行銷活動新增至產品組合以進行最佳化。

1. 在Search、Social和Commerce中建立追蹤行銷活動：

   1. 建立 [虛擬網路帳戶詳細資料](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). 如果您在單一廣告網路中有多個帳戶，請在中將它們整合到一個帳戶中 [!UICONTROL Accounts] 檢視。

      [!DNL Naver] 不提供API支援來上傳追蹤引數至廣告網路。 不過，您可以使用Bulksheets產生追蹤引數，並在廣告網路中手動新增這些引數（根據步驟2）。 若要產生追蹤引數，您必須使用&quot;[!UICONTROL EF Redirect]&quot;追蹤方法。 您可以選擇新增任何您想要的附加引數。

      搜尋、社交和商務會自動包含引數 `ev_cl={ef_uniqueid}` 在帳戶的大量表單中產生的任何追蹤URL中。 此唯一ID可用來比對促銷活動資料與任何費用，以及您上傳的點選資料。

   1. 設定要追蹤的行銷活動：

      1. 在廣告網路中，建立大量表單檔案，其中包含您希望Search、Social和Commerce追蹤帳戶的所有實體及其必要的父實體。

         您可以包含關鍵字的相關資料，包括父促銷活動和廣告群組。

      1. 如有必要，請編輯Bulksheet檔案，使其遵循「搜尋、社交和商務」指令 [需要大量工作表格式，用於 [!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. 在搜尋、社交和商務， [上傳大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >注意： Search、Social和Commerce不會將資料發佈至廣告網路帳戶。

1. 設定行銷活動的追蹤：

   1. 在搜尋、社交和商務， [下載新的Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) 將選項用於&quot;[!UICONTROL Generate Tracking URLs].」
   使用&quot;[!UICONTROL Generate Tracking URLs]「選項會填入 [!UICONTROL Destination URL] 每個關鍵字的欄位，其搜尋、社交和商務追蹤程式碼的前置詞為 [!UICONTROL Base URL] 值。

   以下是含有追蹤的目標URL範例：

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. 複製 [!UICONTROL Destination URL] 將下載的bulksheet檔案中的值轉換為網路上的相關關鍵字設定。

      您可以上傳檔案至廣告網路編輯器中的網路，將URL新增至相關實體。 在這種情況下，您可能需要根據網路的資料需求移除一些欄。 否則，您必須在網路上手動輸入URL。


1. 定期下載每日從廣告網路針對您正在追蹤的關鍵字或廣告群組層級品牌廣告彙總的點選和成本資料，然後 [上傳點選數和成本資料](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) 在中搜尋、社交和商務 [必要格式](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   包含完整的帳戶階層以及您要包含的任何量度。 搜尋、Social和Commerce會將上傳的資料與現有行銷活動中的資料相符。

1. （可選）如果您在網頁中使用Adobe廣告轉換追蹤服務標籤來追蹤未在廣告網路上追蹤的轉換，則傳送包含每日彙總轉換資料的摘要檔案，以新增至您的追蹤促銷活動。

   如需詳細資訊，請聯絡您的Adobe客戶團隊。

所有上傳的追蹤資料都可從取得 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 在 [!UICONTROL Accounts]， [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]、和 [!UICONTROL Keywords] 檢視。 它也可用於中的報告 [!UICONTROL Insights & Reports] 檢視。

>[!MORELIKETHIS]
>
>* [附錄 — 必要的大量表單資料 [!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [上傳的流量和轉換量度 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [的量度資料需求 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

