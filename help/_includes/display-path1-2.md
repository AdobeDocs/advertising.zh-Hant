---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# 某些廣告設定中的「顯示路徑1」和「顯示路徑2」欄位

**[!UICONTROL Display Path 1]**， **[!UICONTROL Display Path 2]：** （選用）新增至顯示URL的文字，會自動從最終URL擷取。 URL中的每個路徑前面都有一個正斜線(`/`)。 路徑不能包含正斜線(`/`)或新行(`\n`)個字元。 每個路徑的長度上限為15個字元或7個雙位元組字元。

若要插入廣告自訂程式，請使用以下格式，其中 `Default text` 是當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

例如，如果顯示路徑1是「交易」，而顯示路徑2是「本機」，則顯示URL會是 `<display URL>/deals/local`，例如www.example.com/deals/local。
