---
title: 使用大量表單指定分類值給帳戶元件
description: 瞭解如何使用Bulksheets將分類值指派給帳戶元件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# 使用大量表單指定分類值給帳戶元件

您可以使用大量表單將標籤分類與下列搜尋實體的值相關聯：行銷活動、廣告群組、關鍵字、廣告、位置、單位層級產品群組及動態搜尋目標。 每個標籤分類最多可以有2000個值。

每個實體在每個分類中可以有一個標籤值。 例如，Shoes_Campaign的「顏色」值可以是「紅色」，而「地理」值可以是「洛杉磯」，但「顏色」或「地理」不能有多個值。

標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

>[!NOTE]
>
>您對於某些廣告網路和行銷活動型別的關鍵字和廣告文案是 [不可變](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，這表示編輯它們會刪除現有實體並建立新實體。 以這種方式刪除現有實體時，標籤分類未指派給新實體。

1. [下載大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) 包括您想要指派標籤分類值的實體：

   * 於 [!UICONTROL Rows and Columns] 標籤中，展開 [!UICONTROL Campaign] 清單于 [!UICONTROL Bulksheet Columns] 窗格。

   * 展開 [!UICONTROL Label Classification] 清單。

   * 選取每一個要在其大量工作表檔案中包含欄的分類。

      例如，如果您包含標籤分類「顏色」和「地理」，則大量表單會包含「顏色」和「地理」欄。

1. 在編輯器中開啟檔案，並將標籤值新增至要與其產生關聯的實體的標籤分類欄。 每個值的長度上限為100個字元，可包含ASCII和非ASCII字元。

   請參閱下一節中的範例值。

   除了新增值之外，您也可以從相關列移除現有值，以刪除現有值。 若要從父實體及其子實體中移除值，請a)僅包含父實體列並移除現有的分類值，或b)同時包含父實體及其子實體，並從所有父實體與子實體列移除現有的分類值。

1. [上傳檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) 以建立關聯。

上傳的標籤值會顯示在相關實體檢視中。

## 要在大量表單中上傳的標籤分類值範例

此範例包含標籤分類「顏色」和「地理」的欄。 對於您自己的大量表單，請用欄取代您自己的標籤分類名稱。

| 帳戶 | Campaign | 廣告群組 | 關鍵字 | 廣告 | 位置 | 標籤 | 顏色 | 地理 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | 綠色 |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | UK |
| Acct1 | C1 | AG1 | K2 |  |  |  | 紅色 | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | 藍色 | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | 紅色 |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | 紅色 | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | 藍色 | DE |

>[!MORELIKETHIS]
>
>* [關於標籤分類](classification-about.md)
>* [建立標籤分類](classification-create.md)
>* [從行銷活動管理檢視指派分類值給帳戶元件](classification-values-assign-campaign-management.md)
>* [從帳戶元件中移除標籤分類值](classification-values-remove.md)
>* [刪除標籤分類值](classification-values-delete.md)
>* [刪除標籤分類](classification-delete.md)

