---
title: 自訂警報範本設定
description: 瞭解自訂警報範本的設定。
exl-id: c9cff26b-e6be-4dad-ac3a-b5a53387c4e6
feature: Search Alerts
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 0%

---

# 自訂警報範本設定

| 標籤 | 引數 | 說明 |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | 要評估警示條件的日期範圍。 量度會在日期範圍內以彙總方式評估。 選項範圍從&#x200B;*[!UICONTROL Yesterday]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 |
| [!UICONTROL Filters] |  | 在[!UICONTROL Scheduling and Delivery]標籤上指定的時間觸發警示的條件。 可用的欄會依實體型別（例如行銷活動或關鍵字）而有所不同。 所有篩選器都使用布林函式AND連結，這表示必須符合所有指定的條件。<ul><li><p>若要新增篩選器，請按一下![新增](/help/search-social-commerce/assets/add.png "新增") **[!UICONTROL ADD FILTER]**&#x200B;旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭頭")，然後執行下列動作：</p></li><ol><li><p>（選擇性）若要依文字字串篩選欄名稱，請在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;輸入欄位中輸入搜尋字串。</p></li><li><p>從欄功能表中選取欄名稱。</p></li><li><p>在欄上定義篩選器：</p></li><ul><li><p>（沒有輸入欄位的篩選器）按一下第二個功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭頭")，然後選取要包含的每個值旁的核取方塊。</p></li><li><p>（您要追蹤其值在指定日期範圍與上一期間之間增加或減少的量度資料行）對於運運算元，請選取&#x200B;*增加*&#x200B;或&#x200B;*減少*，然後輸入臨界值。</p><p>例如，如果您已選取&quot;[!UICONTROL Cost]&quot;欄，且希望在任何行銷活動的成本增加21%時收到警報，則選取&quot;[!UICONTROL increases by]&quot;並在輸入欄位中輸入21。 在[!UICONTROL Date Comparison Format]欄位中，表示您對百分比變更感興趣（而非貨幣單位變更）。</p><p>選取此選項時，會為每個一般資料欄新增兩個額外的欄。 例如，報表不只包含一欄中的「點選數」，而包括「點選數R1」（適用於範圍1）、「點選數R2」（適用於範圍2）以及「點選數差異」或「點選數差異(%)」的欄，視指定的[!UICONTROL Date Comparison Format]而定（請參閱下文）。</p><p>**附註：**</p><ul><li><p>系統不會為衍生量度填入差異欄。<p></li><li><p>此功能不適用於轉換量度、ID或標籤分類欄。</p></li><li><p>比較大型日期範圍的報表可能需要更長的時間才能產生。</p></li></ul></ul><li><p>（具有輸入欄位的所有其他篩選器）從第二個功能表選取運運算元，然後輸入適用的值。</p><p>例如，如果您已選取「點按」欄，且只想傳回點按超過100次的列，則選取「大於」並在輸入欄位中輸入100。</p><p>根據資料型別，可用的運運算元可能包括<i>大於</i>、<i>小於</i>、<i>等於</i>、<i>包含</i>、<i>不包含</i>、<i>開頭為</i>、<i>結尾為</i>、<i>無值</i>、<i>具有值</i>、<i>在</i>之前、<i>在</i>之後，或<i>無日期</i>。</p><p>**注意：**&#x200B;文字值不區分大小寫。 例如，如果您依名稱含有「貸款」的行銷活動進行篩選，結果可能包含「消費者貸款」和「貸款申請」。</p></li></ol><li><p>若要移除篩選器，請按一下篩選器定義旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。</p></li></ul> |
|  | [!UICONTROL Comparing] | （當警報追蹤一或多個量度欄中的增加或減少時可用；唯讀）比較資料的兩個日期範圍。 |
|  | [!UICONTROL Date Comparison Format] | （當警報追蹤一或多個量度欄中的增加或減少時可用）如何表示兩個日期範圍中的資料差異：<ul><li><p><i>[!UICONTROL Variance]</i> （預設） — 將差異顯示為數值。</p></li><li><p><i>[!UICONTROL % Change]</i>  — 以百分比顯示差異。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | 警示名稱。 它必須至少包含五個字元。 |
|  | [!UICONTROL Trigger this Alert] [時間] | 警報檢查指定條件篩選器的頻率，並在符合所有條件時傳送電子郵件通知：<ul><li><p>[!UICONTROL Daily at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AM|PM]]</p></li></ul>**注意：**&#x200B;此值不會影響評估期間。 |
|  | [!UICONTROL Email Recipients] | （僅可由警報範本的建立者編輯；其他人都只能唯讀）產生警報時傳送通知的電子郵件地址。 依預設，會輸入範本建立者的地址。<br><br>若要新增地址，請輸入地址，然後按一下&#x200B;**[!UICONTROL Add]**。 若要指定多個位址，請以逗號或空格加以分隔，或個別新增。<br><br>當警示包含最多1000筆記錄時，會將CSV版本的警示附加至電子郵件訊息。 |

>[!MORELIKETHIS]
>
>* [關於自訂警報](alert-about.md)
>* [建立自訂警示範本](alert-template-create.md)
>* [編輯自訂警示範本](alert-template-edit.md)
>* [暫停自訂警示範本](alert-template-pause.md)
>* [啟動自訂警示範本](alert-template-activate.md)
>* [刪除自訂警示範本](alert-template-delete.md)
>* [檢視自訂警報](alert-view.md)
>* [匯出自訂警示的資料](alert-export-data.md)
