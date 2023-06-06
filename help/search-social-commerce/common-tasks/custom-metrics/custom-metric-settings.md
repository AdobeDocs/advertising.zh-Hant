---
title: 自訂量度設定
description: 參考自訂量度的設定，自訂量度是根據標準量度計算而得。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# 自訂量度設定

自訂量度設定在介面的不同部分稍有不同。

## 行銷活動管理檢視中的自訂量度設定

| 引數/區段 | 說明 |
|----|----|
| 自訂量度名稱 | 測量結果的名稱，顯示為欄名稱。 <b>秘訣：</b> 使用有意義的量度名稱，但請考量名稱較長會讓欄更寬。 |
| 插入量度 | 用來計算新量度的數學公式(例如 [成本]/[註冊]：<ul><li>若要從流量和收入量度清單插入量度，請將游標放在您要插入量度的位置，然後從清單中選取量度，或手動輸入量度並將其括在方括弧中(例如， `[CPC]`)。</li><li>若要插入運運算元，請將游標放在要插入運運算元的位置，然後按一下按鈕或手動輸入符號。 可用的數學運運算元： `+ - * / ( ) ()`</li></ul><b>注意：</b> 複雜的自訂量度需要較長時間才能計算，而包含這些量度的報表和檢視需要較長時間才能產生，尤其是當它們包含用於點進和檢視轉換的單獨欄時。 |
| 格式 | 如何呈現此量度的資料： *[!UICONTROL Currency]* （貨幣值）， *[!UICONTROL Number to 2 Decimal Points]*， *[!UICONTROL Number to 3 Decimal Points]*， *[!UICONTROL Number w/out Decimal Points]*，或 *[!UICONTROL Percentage]* （具有兩個小數點的百分比）。<br><br><b>注意：</b> 如果您使用格式建立衍生量度 [!UICONTROL Number w/out Decimal Points] （會將資料顯示為整數），並將其納入使用加權轉換歸因規則的檢視或報表中([!UICONTROL Weight First Event More]， [!UICONTROL Weight Last Event More]，或 [!UICONTROL Even Distribution])，則輸出會以整數顯示，而非小數。 因此，個別資料欄位可能不正確，即使總計正確。 例如，如果順序平均分配到三個事件，則一個順序（而不是0.33順序）會歸因於三個事件的每個。 為避免此問題，請使用量度格式 [!UICONTROL Number to 2 Decimal Points]. |

## 自訂量度設定(在報表和報表範本中以及 [!UICONTROL Portfolios] 檢視

| 引數/區段 | 說明 |
|----|----|
| 自訂量度名稱 | 測量結果的名稱，顯示為欄名稱。 <b>秘訣：</b> 使用有意義的量度名稱，但請考量名稱較長會讓欄更寬。 |
| 格式 | 如何呈現此量度的資料： *[!UICONTROL Currency]* （貨幣值）， *[!UICONTROL Number to 2 Decimal Points]*， *[!UICONTROL Number to 3 Decimal Points]*， *[!UICONTROL Number w/out Decimal Points]*，或 *[!UICONTROL Percentage]* （具有兩個小數點的百分比）。<br><br><b>注意：</b> 如果您使用格式建立衍生量度 [!UICONTROL Number w/out Decimal Points] （會將資料顯示為整數），並將其納入使用加權轉換歸因規則的檢視或報表中([!UICONTROL Weight First Event More]， [!UICONTROL Weight Last Event More]，或 [!UICONTROL Even Distribution])，則輸出會以整數顯示，而非小數。 因此，個別資料欄位可能不正確，即使總計正確。 例如，如果順序平均分配到三個事件，則一個順序（而不是0.33順序）會歸因於三個事件的每個。 為避免此問題，請使用量度格式 [!UICONTROL Number to 2 Decimal Points]. |
| 插入量度 | 可從中建立公式的現有量度清單。<br><br>若要在公式輸入欄位中插入量度，請將游標放在要插入量度的位置，然後從清單中選取量度，或手動輸入量度並將其括在方括弧中(例如， `[CPC]`)。 |
| 插入運運算元 | 可用的數學運運算元： `+ - x / ( )`<br><br>若要在公式輸入欄位中插入運運算元，請將游標置於要插入運運算元的位置，然後按一下按鈕或手動輸入符號。 |
| [量度的公式輸入欄位] | 用來根據一或多個現有屬性或標準量度(例如 `[Cost]/[Registrations]`. 其中可包含量度和運運算元的任何組合。<br><br><b>注意：</b> 複雜的自訂量度需要較長時間才能計算，而包含這些量度的報表和檢視需要較長時間才能產生，尤其是當它們包含用於點進和檢視轉換的單獨欄時。 |

>[!MORELIKETHIS]
>
>* [關於自訂量度](custom-metric-about.md)
>* [建立自訂量度](custom-metric-create.md)
>* [編輯自訂量度](custom-metric-edit.md)
>* [刪除自訂量度](custom-metric-delete.md)

