---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# 文字廣告範本 — 摘要篩選

**\[摘要篩選器\]：** 要在摘要檔案中傳播哪些列：

* *[!UICONTROL Propagate all rows found in feed:]* （預設）為所有列傳播資料。

* *[!UICONTROL Propagate rows that meet certain conditions:]* 只傳輸符合十個指定條件的資料列的資料。 指定要套用的篩選器：

   1. 選取要用於所有篩選器的布林運算：  **[!UICONTROL AND]** 或 **[!UICONTROL OR]**.

   1. 從第一個功能表選取欄名稱，再從第二個功能表選取運運算元，然後輸入適用的值或將輸入欄位保留空白以傳輸無條件的資料列資料。

   欄清單包含摘要中所有可用的欄。

   可用的運運算元包括 *[!UICONTROL contains]*， *[!UICONTROL does not contain]*， *[!UICONTROL =]*， *[!UICONTROL <>]* （不等於）， *[!UICONTROL in]*， *[!UICONTROL not in]*， *[!UICONTROL less than]*、和 *[!UICONTROL greater than]*. 當您選取運運算元時»[!UICONTROL in]，」您可以輸入逗號分隔的值清單；如果記錄符合任何指定的值，則會傳播這些列的資料。 對於所有其他運運算元，僅輸入一個值。 值不區分大小寫。

   例如，如果您選取「product_type」欄，而只想傳回包含「shoes」的產品名稱列，則選取「**[!UICONTROL contains]**」並輸入 `shoes` 在輸入欄位中。

   1. （若要套用最多九個額外的篩選器）對於每個額外的篩選器，請按一下 **[!UICONTROL Add Condition]**，然後指定每個步驟2的其他篩選器。
