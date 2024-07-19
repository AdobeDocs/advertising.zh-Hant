---
title: ' [!DNL Yahoo! Display Network] 帳戶的Bulksheet資料'
description: 參考 [!DNL Yahoo! Display Network] 帳戶之已下載大量表單中的標題欄位和資料欄位。
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# 附錄 — [!DNL Yahoo! Display Network]帳戶的Bulksheet資料

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

您可以大量下載[!DNL Yahoo! Display Network]帳戶的資料，但無法上傳或張貼大量工作表到廣告網路。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## 可用的資料欄位

| 欄位 | Campaign | 廣告群組 | 廣告 | 說明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 |
| [!UICONTROL Acct  Name] | 若包含 | 若包含 | 若包含 | 可識別廣告網路帳戶的唯一名稱。 |
| [!UICONTROL Campaign Name] | 若包含 | 若包含 | 若包含 | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Ad Group Name] | 不適用 | 若包含 | 若包含 | 可識別廣告群組的唯一名稱。 |
| [!UICONTROL Ad Name] | 不適用 | 不適用 | 若包含 | 在廣告群組中識別廣告的唯一名稱。 長度上限為50個字元。 |
| [!UICONTROL Ad Title] | 不適用 | 不適用 | 若包含 | 廣告的標題。 |
| [!UICONTROL Description Line 1] | 不適用 | 不適用 | 若包含 | 廣告內文的第一行。 |
| [!UICONTROL Description Line 2] | 不適用 | 不適用 | 若包含 | 廣告本文的第二行。 |
| [!UICONTROL Base URL/Final URL] | 不適用 | 不適用 | 若包含 | 使用者按一下您的廣告時，系統會將使用者帶入的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此值是將廣告連結至廣告商網站上的基礎URL/登陸頁面的URL （有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，此值會以您帳戶設定和促銷活動設定中的追蹤引數為基礎。 如果您附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。 |
| \[廣告商特定標籤分類\] | 若包含 | 若包含 | 若包含 | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 |
| [!UICONTROL Constraints] | 若包含 | 若包含 | 不適用 | 指定給圖元的限制。 |
| [!UICONTROL Campaign Status] | 若包含 | 不適用 | 不適用 | 行銷活動的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Status] | 不適用 | 若包含 | 不適用 | 廣告群組的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 若包含 | 關鍵字的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）。 |
| [!UICONTROL Campaign ID] | 若包含 | 若包含 | 若包含 | 可識別現有行銷活動的唯一ID。 |
| [!UICONTROL Ad Group ID] | 不適用 | 若包含 | 若包含 | 可識別現有廣告群組的唯一ID。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 若包含 | 可識別現有關鍵字的唯一ID。 |
| [!UICONTROL AMO ID] | 不適用 | 不適用 | 不適用 | （在產生的大量表單中）同步實體的Adobe產生的唯一識別碼。 |
| [!UICONTROL EF Error Message] | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考）用來顯示來自搜尋、社交和Commerce的錯誤訊息的預留位置，這些錯誤訊息涉及列中的資料；錯誤訊息包含在[!UICONTROL EF Errors]個檔案中。 |

>[!MORELIKETHIS]
>
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
