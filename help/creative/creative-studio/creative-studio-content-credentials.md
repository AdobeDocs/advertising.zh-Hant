---
title: Creative Studio中的C2PA中繼資料
description: 瞭解C2PA中繼資料如何自動附加至在Creative Studio中使用產生AI產生或編輯的內容。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# [!UICONTROL Creative Studio]中的C2PA中繼資料

[!UICONTROL Creative Studio]會自動將C2PA中繼資料附加到使用產生AI產生或編輯的內容中，以便將您的廣告內容的來源記錄為持久且隱藏的中繼資料。 中繼資料遵循[內容來源與真偽聯盟](https://c2pa.org/) (C2PA)的標準。

## 內容型別及其範圍 {#cc-content-types}

| 內容型別 | 支援？ | 產生內容的AI服務 | 產生認證的模型 |
| --- | --- | --- | --- |
| 影像 | 是。 使用產生AI產生或編輯影像時，會附加C2PA中繼資料，並透過AI助理執行的裁切和調整大小操作來保留。 | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## 附加C2PA中繼資料的動作

下表總結了根據[!UICONTROL Creative Studio] AI助理中執行的影像動作，附加C2PA中繼資料的時間。

| 動作 | 說明 | 要附加C2PA中繼資料嗎？ | 使用案例範例 |
| --- | --- | --- | --- |
| **產生影像** | 使用文字提示建立新影像 | 一律如此，因為影像是由產生式AI產生。 | 您可以使用文字提示來產生廣告範本的新背景影像或標誌。<br><br>您使用文字提示，以資料庫上傳的資產取代廣告概念中的預設影像。<br><br>您使用文字提示來產生廣告範本中背景影像的變化。 |

## 內容移動時會有什麼影響？ {#cc-content-moves}

當使用者下載影像檔案或傳送來源鏈以提供廣告時，則會保留完整的來源鏈。

## C2PA中繼資料包含什麼？

對於每次GenAI的產生或變更，C2PA中繼資料中都包含下列專案。 如果資產多次變更，則每個作業都會顯示在C2PA中繼資料中。

* 使用的AI系統的名稱和版本資訊([!DNL Adobe Firefly C2PA])
* 已使用的AI模型([!DNL Gemini Flash])
* 使用方式：是否使用GenAI產生或編輯
* 使用創作AI工具建立和/或修改內容的時間和日期
* 唯一識別碼（可用來區分Generative AI的每種用法）

## 如何檢視影像的C2PA中繼資料？

若要檢視影像的完整資產歷史記錄，

* 在內容真實性檢查工具（例如https://contentauthenticity.adobe.com/inspect或https://verify.contentauthenticity.org/）中開啟影像檔案。

* 檢視影像中繼資料。

* 使用瀏覽器的程式碼檢查工具檢視影像程式碼（通常稱為[!DNL Inspect]）。

![影像的C2PA中繼資料範例](/help/creative/assets/cs-content-credentials-example.png "影像的C2PA中繼資料")

## 其他資源

* [[!DNL Adobe]創作AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [關於Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
