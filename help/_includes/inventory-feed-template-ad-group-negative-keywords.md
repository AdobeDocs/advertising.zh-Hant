---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# 文字廣告範本 — 廣告群組層級負面關鍵字設定

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex以外的所有廣告網路；選擇性）刪除先前使用範本建立但尚未在下方清單中指定的現有廣告群組層級負面關鍵字。 **注意：**&#x200B;使用其他方法建立的負面關鍵字（例如在普通大量表單、[!UICONTROL Campaigns]檢視或在廣告網路的廣告編輯器中）永遠不會使用範本移除。

**[!UICONTROL Apply these negatives]：** （除[!DNL Yandex]以外的所有廣告網路；選擇性）要新增的任何靜態廣告群組層級負關鍵字。 若要為相同關鍵字指定多個關鍵字或多個相符型別，請在不同的行中輸入它們。 請使用下列語法，不含減號：

* 負值廣泛比對： `keyword` （不受[!DNL Microsoft Advertising]支援）
* 負面字詞相符： `"keyword"`
* 完全相符的負值： `[keyword]`

當您透過範本傳播摘要資料時，產生的大量表單會使用詞句和完全相符型別的慣用語法。 **注意：**&#x200B;您無法在[!UICONTROL Keywords]索引標籤或[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]檢視中看到負關鍵字。
