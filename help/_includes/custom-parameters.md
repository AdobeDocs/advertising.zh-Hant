---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# GGL和MS Campaign設定、MS廣告群組設定，以及MS多媒體和回應式廣告設定中的自訂引數欄位

**[!UICONTROL Custom Parameters]：** (選用；僅適用於對象促銷活動 [!DNL Microsoft Advertising])最多三個自訂引數的名稱和值配對。 名稱的長度上限為16個英數字元；值的長度上限為200個字元，包括內嵌引數。

您可以在實體及其子實體的追蹤範本中包含自訂引數名稱。 當使用者按一下相關廣告時，廣告網路會以定義的引數值取代引數名稱。 例如，如果您建立客戶引數 `{_color}=red` 而且您的追蹤範本包含 `http://tracker.example.com/?color={_color}&u={lpurl}`，則當使用者按一下廣告時，「red」會插入color引數中。

廣告群組的自訂引數或([!DNL Microsoft Advertising] 僅限)廣告層級覆寫具有相同名稱的促銷活動層級自訂引數。
