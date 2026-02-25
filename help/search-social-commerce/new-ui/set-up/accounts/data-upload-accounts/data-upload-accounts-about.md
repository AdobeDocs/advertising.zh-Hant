---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 關於上傳用於報告和模擬的帳戶資料

<!-- Move all related files into one page? -->

如果您使用搜尋、社交和Commerce不提供API支援的線上廣告網路，您可以上傳行銷活動內容和離線成本、點選次數和轉換資料，供帳戶用於報表和效能模擬。 具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商也可以在Adobe Analytics中檢視其帳戶的資料。

此功能適用於遵循標準三層級行銷活動結構的廣告網路(行銷活動、廣告群組或廣告集，以及競標單位（廣告或關鍵字）)。 對於Adobe DSP，此功能適用於指派給套件的套件和刊登版位，但不適用於具有刊登版位層級步調的行銷活動或刊登版位。

下列網路提供立即可用的支援： <!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

此功能不支援搜尋、社交和Commerce點選追蹤以及Adobe Advertising轉換追蹤。

## 搜尋、社交和Commerce中可用的功能

* 追蹤與報告：

   * 在行銷活動管理檢視中，將唯讀行銷活動元件向下調整至競標單位層級。

   * 行銷活動管理檢視和自訂報表中的效能資料，低至廣告群組層級<!-- verify the entity level -->。 具有[!DNL Adobe Analytics for Advertising]的廣告商)還會在為廣告商指定的Adobe Analytics報表套裝中，取得低至廣告群組層級<!-- verify the entity level -->的效能資料。&lt;！ — 確認資料型別是否受限 — 成本、點選、顯示曝光數、收入？—>

* 將行銷活動新增至產品組合時的效能模擬。<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  搜尋、Social和Commerce不會針對產品組合中這些型別的行銷活動最佳化任何內容，甚至不會進行投標。

## 設定離線帳戶的工作流程

<!-- subtitle wording? -->

1. [設定虛擬帳戶記錄](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)。

1. 為單一帳戶<!--  in what file format? -->建立資料檔案，包括行銷活動、廣告群組和廣告的日層級狀態。

資料必須符合廣告網路的資料要求，因此每個實體的資料欄位可能會因廣告網路而異。

1. <!-- For all ad networks (excluding DSP), -->以下列其中一種方式上傳單一帳戶的初始資料：

* 從您的裝置或網路手動上傳檔案。

* 將資料上傳至[!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])貯體中的搜尋、社交和Commerce指派資料夾。

  >[!PREREQUISITES]
  >
  >* 請聯絡您的Adobe帳戶團隊，為您的搜尋、社交和Commerce廣告商帳戶啟用帳戶資料上傳。 團隊將協助在[!DNL S3]儲存貯體中建立組織特定的資料夾，並在完成時通知您。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* 擷取您帳戶的[!DNL S3]雲端儲存路徑、存取金鑰ID和機密存取金鑰。 組織的所有資料上傳<!-- naming convention?-->帳戶都使用相同的存取金鑰識別碼和機密存取金鑰。

1. 繼續每日上傳新資料檔案。

1. 上傳30天的資料後，您可以選擇將行銷活動新增至<!--what type? how should we refer to them? -->產品組合併產生模擬。

您可以[檢視每個資料上傳](upload-log.md)的記錄檔以檢視其狀態。 此外，如果您啟動上傳作業，但上傳作業未完全成功，則系統會根據您的通知設定，透過[通知中心](/help/search-social-commerce/notifications/notification-about.md)傳送錯誤通知。

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [關於上傳用於報告和模擬的帳戶資料](data-upload-accounts-about.md)
>* [將帳戶資料上傳至 [!DNL Amazon] [!DNL S3]貯體](upload-data-from-s3-bucket.md)
>* [手動上傳帳戶資料](upload-data-manually.md)
>* [檢視已上傳帳戶資料檔的記錄](upload-log.md)
>* [管理資料上傳的廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
