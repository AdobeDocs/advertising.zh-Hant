---
title: 自訂量度設定
description: 參考自訂量度的設定，自訂量度會從標準量度計算。
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 自訂量度設定

自訂量度設定在介面的不同部分稍有不同。

## 大多數管理檢視中的自訂量度設定

| 引數/區段 | 說明 |
|----|----|
| 自訂量度名稱 | 測量結果的名稱，會顯示為資料欄名稱。 <b>提示：</b>請使用有意義的量度名稱，但請考量名稱較長會讓欄位更寬。 |
| 插入量度 | 用於計算新量度的數學公式(例如[成本]/[註冊]：<ul><li>若要從流量和收入量度清單插入量度，請將游標放在您要插入量度的位置，然後從清單中選取量度，或手動輸入量度並將其括在方括弧中（例如`[CPC]`）。</li><li>若要插入運運算元，請將游標置於要插入運運算元的位置，然後按一下按鈕或手動輸入符號。 可用的數學運運算元： `+ - * / ( ) ()`</li></ul><b>注意：</b>複雜的自訂量度需要更長的時間才能計算，而包含這些量度的報表和檢視（尤其是當它們包含用於點進和檢視轉換的個別欄時）需要更長的時間才能產生。 |
| 格式 | 如何呈現此量度的資料： *[!UICONTROL Currency]* （貨幣值）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]*&#x200B;或&#x200B;*[!UICONTROL Percentage]* （具有兩個小數點的百分比）。<br><br><b>警告：</b>如果您建立格式為[!UICONTROL Number w/out Decimal Points]的衍生量度（將資料顯示為整數），並將它包含在使用加權轉換歸因規則（[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More]或[!UICONTROL Even Distribution]）的檢視或報表中，則輸出會以整數顯示，而非小數。 因此，即使總計正確，個別資料欄位也可能不正確。 例如，如果順序平均分配給三個事件，則一個順序（而不是0.33順序）會歸因於三個事件的每一個。 若要避免此問題，請使用量度格式[!UICONTROL Number to 2 Decimal Points]。 |

## 報告和報告範本以及舊版[!UICONTROL Portfolios]檢視中的自訂量度設定

| 引數/區段 | 說明 |
|----|----|
| 自訂量度名稱 | 測量結果的名稱，會顯示為資料欄名稱。 <b>提示：</b>請使用有意義的量度名稱，但請考量名稱較長會讓欄位更寬。 |
| 格式 | 如何呈現此量度的資料： *[!UICONTROL Currency]* （貨幣值）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]*&#x200B;或&#x200B;*[!UICONTROL Percentage]* （具有兩個小數點的百分比）。<br><br><b>警告：</b>如果您建立格式為[!UICONTROL Number w/out Decimal Points]的衍生量度（將資料顯示為整數），並將它包含在使用加權轉換歸因規則（[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More]或[!UICONTROL Even Distribution]）的檢視或報表中，則輸出會以整數顯示，而非小數。 因此，即使總計正確，個別資料欄位也可能不正確。 例如，如果順序平均分配給三個事件，則一個順序（而不是0.33順序）會歸因於三個事件的每一個。 若要避免此問題，請使用量度格式[!UICONTROL Number to 2 Decimal Points]。 |
| 插入量度 | 現有量度的清單，您可從中建立公式。<br><br>若要在公式輸入欄位中插入量度，請將游標放在您要插入量度的位置，然後從清單中選取量度，或手動輸入該量度並將其括在方括弧中（例如，`[CPC]`）。 |
| 插入運運算元 | 可用的數學運運算元： `+ - x / ( )`<br><br>若要在公式輸入欄位中插入運運算元，請將游標置於要插入運運算元的位置，然後按一下按鈕或手動輸入符號。 |
| [量度]的公式輸入欄位 | 用來根據一或多個現有屬性或標準量度（例如`[Cost]/[Registrations]`）計算新量度的數學公式。 其中可包含量度和運運算元的任意組合。<br><br><b>注意：</b>複雜的自訂量度需要更長的時間才能計算，而包含這些量度的報表和檢視（尤其是當它們包含用於點進和檢視轉換的個別欄時）需要更長的時間才能產生。 |

>[!MORELIKETHIS]
>
>* [關於自訂量度](custom-metric-about.md)
>* [建立自訂量度](custom-metric-create.md)
>* [編輯自訂量度](custom-metric-edit.md)
>* [刪除自訂量度](custom-metric-delete.md)
