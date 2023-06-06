---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# 帳戶和行銷活動設定中的重新導向型別欄位

**[!UICONTROL Redirect Type]：** (適用於 [!UICONTROL EF Redirect] 僅限)將一般使用者重新導向至最終URL或目的地URL的方法。 選取的選項適用於帳戶或行銷活動中的所有廣告、關鍵字和位置。 預設帳戶層級設定繼承自廣告商的追蹤設定，而預設行銷活動層級設定繼承自帳戶設定。

* *[!UICONTROL Standard]：* 將一般使用者重新導向至指定的URL。

* *[!UICONTROL Token]：* 若要將一般使用者重新導向至URL，並記錄點選的搜尋、社交和商務ID (`ef_id`)作為查詢字串引數，此引數會當作Token使用。 如果您要報告離線交易、希望Search、Social和Commerce與Adobe Analytics交換資料，或希望追蹤內發生的所有轉換，請選擇此選項 [!DNL Apple Safari] 瀏覽器。

**附註：**

* 如果您從 [!UICONTROL Standard] 至 [!UICONTROL Token]，反之亦然，則您必須重新產生帳戶的追蹤URL。
* 您可以在行銷活動層級覆寫帳戶層級設定。
