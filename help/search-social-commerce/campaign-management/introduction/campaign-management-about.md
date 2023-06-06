---
title: 關於Search、Social和Commerce中的促銷活動管理
description: 瞭解Search、Social和Commerce中的促銷活動管理功能。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 關於Search、Social和Commerce中的促銷活動管理

搜尋、Social和Commerce可讓您在一個位置追蹤和/或管理您的搜尋、顯示/內容、社交、購物、對象和最高成效行銷活動。 根據廣告網路和促銷活動型別，可用功能可能包括與廣告網路同步、建立及編輯功能、追蹤和轉換歸因、報告，以及競標和預算最佳化。 如需每個廣告網路可用功能的詳細資訊，請參閱「[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md).」

當您新增及編輯行銷活動資料時， [!UICONTROL Campaigns] 檢視、搜尋、社交和商務會立即將資料變更推送至廣告網路。 搜尋、Social和Commerce也會提取行銷活動結構資料，以及每天從同步的廣告網路帳戶點按資料一次（或在偵測到新行銷活動時更頻繁），並根據請求進行點按。

## 設定對您的廣告網路帳戶的存取權

若要追蹤廣告商廣告網路帳戶中的廣告成效（並可能針對廣告投標），Adobe帳戶團隊 [建立對應的帳戶記錄](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) 在「搜尋」、「社交」和「商務」中。 帳戶記錄包含追蹤選項。

對於透過廣告網路的API同步的帳戶，帳戶記錄也包含帳戶存取認證。 帳戶啟用後，系統會使用廣告網路從提取帳戶資料。 然後，您可以檢視現有的帳戶資料，以及建立和編輯行銷活動結構和廣告資料。

## 點按追蹤可將點按連結至轉換

如果您使用Adobe廣告轉換追蹤服務，則必須在登入頁面尾碼、追蹤範本和廣告的最終/目的地URL、關鍵字、位置、網站連結和產品清單中包含Search、Social和Commerce點選追蹤程式碼。 對象 [支援的廣告網路和行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md) 其行銷活動設定包括&quot;[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動附加自己的重新導向和追蹤程式碼，因此您不需要手動新增。 否則，您必須手動將程式碼新增至您的追蹤範本或最終URL。

如需追蹤的詳細資訊，請參閱「追蹤」一章。

## 自動化投標和預算管理

對象 [支援的廣告網路和行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)，您可以將行銷活動分組到產品組合中，每個產品組合都有特定的業務目標和特定的預算或績效目標。 在標準產品組合中，「搜尋」、「Social」和「Commerce」會最佳化CPC關鍵字競標和促銷活動預算。 混合產品組合結合來自搜尋、Social和Commerce的最佳化技術以及您的廣告網路。

如需有關可用投資組合選項以及如何設定投資組合的詳細資訊，請參閱最佳化指南中「管理Portfolio」一章，此章節可從「搜尋、社交和商務」中取得。<!-- verify convention for referencing Optimization Guide here -->

## 行銷活動管理檢視

行銷活動管理檢視可讓您監控和管理您的搜尋帳戶。 可使用下列檢視：

* **[!UICONTROL Campaigns]**  — 此 [!UICONTROL Campaigns] 檢視會顯示每個已連線廣告網路帳戶的資料。 您可以檢視所有廣告網路帳戶以及個別帳戶、行銷活動、廣告群組、關鍵字、廣告、購物產品群組、位置、自動目標（動態搜尋目標）、對象、廣告擴充功能程式庫及其相關帳戶實體的成本、點選、曝光和收入資料。 對象 [支援的廣告網路上的支援行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)，您可以直接在介面中建立和編輯個別行銷活動和行銷活動元件的資料。 您可以選擇將大多數子檢視中的資料匯出至試算表檔案。

   >[!NOTE]
   >
   >廣告層級資料不可用於 [!DNL Google Ads] 動態搜尋廣告(DSA)、最高效能、智慧購物和 [!DNL YouTube] 行銷活動。

* **[!UICONTROL Products]**  — 此 [!UICONTROL Products] 檢視顯示每個專案的資料 [[!DNL Google] or [!DNL Microsoft] 已同步的商家中心帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 預設 [!UICONTROL Accounts] 子檢視會列出所有已同步的帳戶；有些使用者型別可以從此檢視新增帳戶。 此 [!UICONTROL Products] 子檢視會列出帳戶內的每個產品。

* **[!UICONTROL Advanced (ACM)]**  — 從 [!DNL Advanced] ([!DNL AMC]，針對進階Campaign Management)檢視，您可以設定自動化流程以建立 [以詳細目錄中每個專案為目標的動態廣告和關鍵字](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 根據您建立的廣告網路專屬廣告範本及其內容 [!DNL Google Merchant Center] 您上傳至FTP位置的帳戶或詳細目錄資料檔案。 子檢視會顯示廣告商的每個摘要範本的詳細資訊，以及摘要中包含的每個促銷活動、廣告群組、關鍵字和廣告（透過摘要範本傳播但未發佈至廣告網路）。

* **[!UICONTROL Bulksheets]**  — 使用 [!UICONTROL Bulksheets] 檢視以建立 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 針對上的帳戶，包含您想要的資料量 [支援的廣告網路](/help/search-social-commerce/introduction/supported-inventory.md)，然後張貼至廣告網路。

* **[!UICONTROL Audiences]** — [此 [!UICONTROL Audiences] 檢視](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) 列出您的所有 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 從各種型別的使用者清單產生的對象。 您可以建立 [!DNL Google Ads] 來自您現有Adobe Experience Cloud對象和客戶電子郵件清單的對象。 您也可以檢視和管理您的對象目標和排除專案 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 廣告。

* **[!UICONTROL Label Classifications]**  — 使用此檢視來建立和刪除 [標籤分類](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)，可協助您將標籤分組為有意義的集合。

>[!MORELIKETHIS]
>
>* [實作廣告網路帳戶和行銷活動的概觀](campaign-implemention-overview.md)
>* [監控及管理廣告網路行銷活動的效能](monitor-performance-campaigns.md)
>* [搜尋、社交和商務中的Google Ads轉換資料](google-conversion-data.md)

