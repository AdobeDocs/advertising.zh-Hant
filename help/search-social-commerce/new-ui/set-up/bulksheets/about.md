---
title: （新UI）關於使用大量表單管理行銷活動資料
description: 瞭解廣告網路、大量表單工作流程可用的大量表單功能，以及新搜尋、社交和Commerce UI中的錯誤處理。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 772
ht-degree: 0%

---

# （新UI）關於使用大量表單管理行銷活動資料

大量表單是包含特定格式之行銷活動資料的檔案，可用來快速建立或修改行銷活動和廣告群組結構資料及文字廣告。 您可以針對一或多個帳戶、特定行銷活動和廣告群組，或甚至特定文字廣告、版位和產品群組，產生（下載）大量表單。 您可以使用大量表單來管理大型資料集或進行小型變更。 每個廣告網路都需要不同的資訊欄。

您可以產生含有所需資料量的大量工作表，也可以選擇手動建立大量工作表並上傳。 如需檔案格式需求，請參閱[大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)中必要的和包含的資料，以及如需廣告網路支援的作業，請參閱[您可以在大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)中執行的作業。

建立大量表單後，您可以識別任何需要修正的損壞登陸頁面，或新增或編輯的其他資料。 接著，您可以編輯檔案，並將其上傳至Search、Social和Commerce，或排程立即或稍後發佈至相關廣告網路。 您也可以立即或稍後張貼可用的大量表單。

所有大量表單、登陸頁面驗證錯誤檔案和其他錯誤檔案，都會在建立後30天自動刪除，除非您先前將其刪除。

## 依廣告網路區分的功能 {#bulksheet-functionality-by-network}

* **下載、上傳和張貼：** [!DNL Baidu]、[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yandex]帳戶

* **僅下載和上傳：** [!DNL Naver]帳戶

  您可以上傳[!DNL Naver]資料以供搜尋、社交和Commerce使用，但無法將其張貼至廣告網路。 您也可以下載現有（未同步的）資料。

* **僅下載資料：** [!DNL Pinterest]、[!DNL Yahoo DSP]、[!DNL Yahoo Native]帳戶

  您可以下載現有（未同步的）資料。

## 使用Bulksheets概述

將大量表單用於已同步帳戶的標準步驟如下：

1. [將一或多個帳戶、行銷活動或廣告群組的資料下載到Bulksheet檔案](download.md)。 您可以選擇手動填入廣告網路專屬大量表單並上傳檔案。

1. [驗證基礎（最終） URL或檔案中的目的地URL中的登入頁面](validate-landing-pages.md)。

1. 當您需要新增資料或進行更正時：

   1. 將檔案匯出至案頭，並在[!DNL Microsoft Excel]中進行編輯。

   1. [手動將編輯的檔案](upload.md)上傳至Search、Social和Commerce。

1. （針對手動上傳的檔案） [上傳檔案](post.md)時或稍後將檔案發佈到廣告網路。

1. （如有必要）下載任何新的錯誤檔案、更正列，然後重新張貼檔案。

## 管理上傳和發佈行銷活動資料的錯誤

搜尋、Social和Commerce會儘可能從行銷活動大量表單上傳和發佈多列資料，包括必要時產生的追蹤URL。

當大量表單作業期間發生錯誤時，會產生下列兩種錯誤檔案之一：

* **[!UICONTROL EF Errors]：**&#x200B;當檔案或檔案中的個別資料列無法上傳或處理時，會建立名為`<uploaded file name>_ef_errors.<extension used for the bulksheet>`的錯誤檔案。 如果問題與個別列有關，則會包含這些列，並附上每個錯誤的說明，以便進行更正。

* **[!UICONTROL SE Errors]：**&#x200B;當已張貼檔案，但廣告網路不接受部分或全部資料時，就會建立名為`<uploaded file name>_se_errors.<extension used for the bulksheet>`的錯誤檔案。 接受部分而非全部列時，錯誤檔案會顯示未發佈的列以及每個錯誤的說明，以便進行更正。 錯誤訊息會顯示在每一列的最後三欄。

>[!NOTE]
>
>如果您張貼任何[!DNL Google Ads]個違反廣告網路的廣告政策，但可能有資格獲得劐免的廣告，這些廣告會自動以劐免請求重新張貼。 如果劐免請求失敗，則錯誤檔案中會包含違規的相關資訊。

您可以下載任一型別的錯誤檔案，直接在列中進行更正，然後重新上傳並張貼檔案。

錯誤檔案會在30天後自動刪除，除非您先前將其刪除。

## 每個檔案的相關資訊

可從[!UICONTROL Setup] \> [!UICONTROL Bulksheets]取得所有已下載的資料檔案、已上傳檔案和錯誤檔案。

每個檔案的資訊包括目前任務狀態以及完成任務的百分比、建立日期、（適用時）張貼至指定廣告網路的日期、排程的刪除日期，以及起始任務之使用者的登入名稱。

>[!MORELIKETHIS]
>
>* [ （新UI）下載/建立Bulksheet檔案](download.md)
>* [（新使用者介面）上傳大量表單或已修正的錯誤檔案](upload.md)
>* [ （新UI）張貼大量表單或已修正的錯誤檔案](post.md)
>* [（新UI）驗證Bulksheet檔案中的登入頁面](validate-landing-pages.md)
>* [（新UI）刪除已上傳的大量工作表和錯誤檔案](delete.md)
>* [（新UI）停止進行中的大量表單工作](stop-job.md)
