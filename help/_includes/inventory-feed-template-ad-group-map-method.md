---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# 文字廣告範本 — 廣告群組對應方法

**[!UICONTROL Map Method]：** (當 [!UICONTROL Map Only] 已為廣告群組啟用；所有廣告網路除外 [!DNL Yandex])新關鍵字和廣告對應至現有廣告群組的方法：

* *[!UICONTROL Contains Anywhere]：* 將資料新增至其名稱包含指定字串的現有廣告群組（如果存在）。

* *[!UICONTROL Contains Exactly]：* 將資料新增至其名稱包含指定字串的現有廣告群組（如果存在）。

* *[!UICONTROL Exactly Matches]* （預設值）：將資料新增至具有相同名稱的現有廣告群組（如果存在）。

找不到相符專案時，會忽略廣告群組的所有資料。 如果摘要中的廣告群組資料不包含行銷活動資料，則廣告群組會對應至任何行銷活動中具有相同名稱的廣告群組（如果存在）。 如果找到多個相符的廣告群組，則關鍵字和廣告會對映至所有關鍵字和廣告。
