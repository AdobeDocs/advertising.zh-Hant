---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# 文字廣告範本 — 摘要篩選

**\[摘要篩選器\]：**&#x200B;摘要檔案中要傳播的列：

* *[!UICONTROL Propagate all rows found in feed:]* （預設）以傳播所有列的資料。

* *[!UICONTROL Propagate rows that meet certain conditions:]*&#x200B;只傳輸符合十個指定條件的資料列的資料。 指定要套用的篩選器：

   1. 選取要用於所有篩選器的布林運算： **[!UICONTROL AND]**&#x200B;或&#x200B;**[!UICONTROL OR]**。

   1. 從第一個功能表選取欄名稱，從第二個功能表選取運運算元，然後輸入適用的值或讓輸入欄位留白，以傳輸無條件的資料列的資料。

  欄清單包含摘要中所有可用的欄。

  可用的運運算元包括&#x200B;*[!UICONTROL contains]*、*[!UICONTROL does not contain]*、*[!UICONTROL =]*、*[!UICONTROL <>]* （不等於）、*[!UICONTROL in]*、*[!UICONTROL not in]*、*[!UICONTROL less than]*&#x200B;和&#x200B;*[!UICONTROL greater than]*。 當您選取運運算元&quot;[!UICONTROL in]&quot;時，可以輸入逗號分隔的值清單；如果記錄符合任何指定的值，則會傳播這些列的資料。 對於所有其他運運算元，僅輸入一個值。 值不區分大小寫。

  例如，如果您選取「product_type」欄，而只想傳回包含「鞋子」之產品名稱的列，則選取「**[!UICONTROL contains]**」並在輸入欄位中輸入`shoes`。

   1. （若要套用最多9個額外的篩選器）對於每個額外的篩選器，請按一下「**[!UICONTROL Add Condition]**」，然後指定每個步驟2的其他篩選器。
