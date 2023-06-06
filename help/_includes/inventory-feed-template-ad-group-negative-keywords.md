---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# 文字廣告範本 — 廣告群組層級負面關鍵字設定

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex以外的所有廣告網路；選擇性）刪除先前使用範本建立、但下列清單中未指定的現有廣告群組層級負面關鍵字。 **注意：** 使用其他方法建立的負面關鍵字(例如，在普通大量表單中， [!UICONTROL Campaigns] 使用範本時，不會移除檢視或廣告網路的廣告編輯器中的檢視。

**[!UICONTROL Apply these negatives]：** (所有廣告網路，除了 [!DNL Yandex]；選用)要新增的任何靜態廣告群組層級負面關鍵字。 若要為相同關鍵字指定多個關鍵字或多個相符型別，請在個別行中輸入它們。 請使用下列語法（不含減號）：

* 負面廣泛符合： `keyword` (不支援 [!DNL Microsoft Advertising])
* 負面字詞相符： `"keyword"`
* 完全相符的負值： `[keyword]`

當您透過範本傳播摘要資料時，會產生大量表單，而片語和完全相符型別的慣用語法會用於該表單中。 **注意：** 您在中看不到負關鍵字 [!UICONTROL Keywords] 標籤或 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 檢視。
