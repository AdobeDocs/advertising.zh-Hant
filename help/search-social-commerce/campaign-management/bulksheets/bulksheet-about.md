---
title: 關於使用大量表單管理行銷活動資料
description: 瞭解廣告網路、大量表單工作流程和錯誤處理可用的大量表單功能。
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# 關於使用大量表單管理行銷活動資料

大量表單是包含特定格式之行銷活動資料的檔案，可用來快速建立或修改行銷活動和廣告群組結構資料及文字廣告。 您可以針對一或多個帳戶、特定行銷活動和廣告群組，或甚至特定文字廣告、版位和產品群組，產生（下載）大量表單。 您可以使用大量表單來管理大型資料集或進行小型變更。 每個廣告網路都需要不同的資訊欄。

您可以產生含有所需資料量的大量工作表，也可以選擇手動建立並上傳這些工作表（請參閱有關「大量工作表中必要/包含的資料」的章節）。

建立大量表單後，您可以識別任何需要修正的損壞登陸頁面，或新增或編輯的其他資料。 接著，您可以編輯檔案，並將其上傳至Search、Social和Commerce，或排程立即或稍後發佈至相關廣告網路。 您也可以立即或稍後張貼可用的大量表單。

您可以選擇將大量表單檔案上傳到指定的FTP帳戶，以進行擷取和自動發佈。 目錄每小時掃描一次，新檔案會依接收順序張貼到搜尋網路。

所有大量表單、登陸頁面驗證錯誤檔案和其他錯誤檔案，都會在建立後30天自動刪除，除非您先前將其刪除。

## 依廣告網路的功能

* **下載、上傳和張貼：**  [!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yandex] 帳戶

* **僅下載和上傳：** [!DNL Naver] 帳戶

  您可以上傳 [!DNL Naver] 用於搜尋、社交和Commerce的資料，但無法張貼至廣告網路。 您也可以下載現有（未同步的）資料。

* **僅下載資料：**  [!DNL Pinterest]， [!DNL Yahoo Native]、和 [!DNL Yahoo! Display Network] 帳戶

  您可以下載現有（未同步的）資料。

## 使用Bulksheets概述

針對已同步帳戶使用大量表單的標準步驟如下：

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [將一或多個帳戶、行銷活動或廣告群組的資料下載到大量表單檔案中](bulksheet-download.md). 您可以選擇手動填入廣告網路專屬大量表單並上傳檔案。

1. [驗證登入頁面](bulksheet-validate-landing-pages.md) 在檔案中的基礎（最終） URL或目的地URL中。

1. 當您需要新增資料或進行更正時：

   1. [匯出檔案](bulksheet-export.md) 到您的案頭並在中進行編輯 [!DNL Microsoft Excel].

   1. [手動上傳已編輯的檔案](bulksheet-upload.md) 搜尋、社交和Commerce，或 [將檔案上傳至指定的FTP帳戶](bulksheet-ftp-account.md) 以自動過帳。

1. （針對手動上傳的檔案） [發佈檔案](bulksheet-post.md) 上傳時或稍後上傳至廣告網路。

1. （如有必要）下載任何新的錯誤檔案、更正列，然後重新張貼檔案。

## 管理上傳和發佈行銷活動資料的錯誤

搜尋、Social和Commerce會儘可能從行銷活動大量工作表上傳和發佈多列資料，包括必要時產生的追蹤URL。

當大量表單作業期間發生錯誤時，會產生下列兩種錯誤檔案之一：

* **[!UICONTROL EF Errors]：**  當檔案或檔案中的個別列無法上傳或處理時，名為的錯誤檔案 `<uploaded file name>_ef_errors.<extension used for the bulksheet>` 「 」已建立。 如果問題與個別列有關，則會包含這些列，並附上每個錯誤的說明，以便進行更正。

* **[!UICONTROL SE Errors]：**  發佈檔案但廣告網路不接受部分或全部資料時，出現名為的錯誤檔案 `<uploaded file name>_se_errors.<extension used for the bulksheet>` 「 」已建立。 接受部分而非全部列時，錯誤檔案會顯示未發佈的列以及每個錯誤的說明，以便進行更正。 錯誤訊息會顯示在每一列的最後三欄。

>[!NOTE]
>
>如果您張貼任何 [!DNL Google Ads] 違反廣告網路的廣告政策，但可能有資格獲得劐免的廣告，這些廣告就會自動以劐免請求重新上傳。 如果劐免請求失敗，則錯誤檔案中會包含違規的相關資訊。

您可以下載任一型別的錯誤檔案，直接在列中進行更正，然後重新上傳並張貼檔案。

錯誤檔案會在30天後自動刪除，除非您先前將其刪除。

## 每個檔案的相關資訊

所有下載的資料檔案、上傳的檔案和錯誤檔案都可從取得 [!UICONTROL Search] > [!UICONTROL Bulksheets].

每個檔案的資訊包括目前任務狀態以及完成任務的百分比、建立日期、（適用時）張貼至指定廣告網路的日期、排程的刪除日期，以及起始任務之使用者的登入名稱。

>[!MORELIKETHIS]
>
>* [下載/建立Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [上傳大量表單或已修正的錯誤檔案](bulksheet-upload.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)
>* [匯出產生或上傳的大量表單檔案](bulksheet-export.md)
