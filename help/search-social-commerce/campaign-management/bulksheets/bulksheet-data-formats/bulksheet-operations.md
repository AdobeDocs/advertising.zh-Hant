---
title: 可在大量表單中執行的作業
description: 參考使用大量表單新增、編輯和刪除行銷活動資料的一般資訊。
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 可在大量表單中執行的作業

您可以透過大量表單新增、編輯和刪除行銷活動資料 [支援的廣告網路](../bulksheet-about.md#bulksheet-functionality-by-network).

為您要新增、編輯或刪除的每個行銷活動元件（行銷活動、廣告群組、關鍵字或文字廣告）或其屬性加入個別的資料行。 例如，如果您想要建立一個行銷活動，包含一個廣告群組、一個關鍵字和一個廣告（總共四個元件），則需要四個個別的資料行。 若要編輯 [!UICONTROL Ad Group Name] 但是，對於廣告群組（一個元件），您只需要一行。 同樣地，若要編輯一個廣告群組（一個元件）的四個不同屬性，您只需要一行。

下列規則適用於使用行銷活動元件及其屬性。

* 新增：

   * 若要新增元件，請包含新增該元件所需的所有欄位，以及選擇性地包含任何元件屬性的欄位。

   * 為現有的元件新增屬性，例如 [!UICONTROL Ad Group End Date] 對於廣告群組，請包含編輯該元件（廣告群組）所需的所有欄位，加上屬性的欄位([!UICONTROL Ad Group End Date])。

* 若要編輯現有元件的屬性，請包含編輯該元件所需的所有欄位，以及屬性的欄位。

  如果您將屬性欄位保留為空白，則會保留現有值。

* 正在刪除：

   * 若要刪除現有元件，請包含編輯該元件並將其狀態變更為所需的所有欄位 [!UICONTROL Deleted]. 例如，若要刪除 [!DNL Google Ads] 廣告群組，您必須包含 [!UICONTROL Campaign Name]， [!UICONTROL Ad Group Name]， [!UICONTROL Ad Group Status] ，值為 <i>[!UICONTROL Deleted]</i>、和 [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1]， [!UICONTROL Param2]、和 [!UICONTROL Param3] （僅限值）若要刪除現有 [!DNL paramN] 關鍵字的值，包含編輯關鍵字所需的所有欄位，並刪除現有的欄位 [!DNL paramN] 輸入值來計算值 `[delete]` （包括括弧）於對應欄位中。

   * （允許的屬性欄位）若要刪除元件的現有屬性值，請包含編輯該元件所需的所有欄位，也可輸入值來刪除屬性值 `[delete]` （包括括弧）。 允許的欄位包括：

      * ([!UICONTROL Google Ads] 僅限) [!UICONTROL Description Line 1]， [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 僅限) [!UICONTROL Product Scope Filter]， [!UICONTROL Base URL/Final URL]， [!UICONTROL Tracking Template]

>[!NOTE]
>
>當您在不適用於動作的欄位中包含值時，在欄位中輸入的任何值都會被忽略。

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](../bulksheet-about.md)
>* [支援的大量表單檔案格式](bulksheet-file-formats.md)
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
