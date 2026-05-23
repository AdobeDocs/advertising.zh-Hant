---
title: （新UI）管理自訂警報
description: 瞭解如何建立、設定、暫停、啟用、刪除、檢視和匯出自訂警報和警報範本。
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# （新UI）管理自訂警報

建立警報範本，以識別任何投資組合、行銷活動或廣告群組在指定期間符合特定條件（例如績效量度）的情況，然後產生警報。 警示功能適用於單一廣告商。 警示包含相關預設檢視中的所有欄。 例如，行銷活動層級警示包含預設[!UICONTROL Campaigns]檢視中的所有欄。

您可以從[!UICONTROL Custom Alerts]面板的[!UICONTROL Alert Templates]標籤或任何頁面頂端建立警報範本。

觸發警示範本的警示執行個體時：

* 指定的收件者會收到電子郵件通知。 當警示最多包含1000筆記錄時，電子郵件通知會包含含有警示資料的[CSV](/help/search-social-commerce/glossary.md#c-d)檔案，其中包含觸發警示之所有實體的資料。

* 警示列在[!UICONTROL Custom Alert Templates]面板的[!UICONTROL Triggered Alerts]標籤中。<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## [!UICONTROL Custom Alerts]檢視

若要開啟[!UICONTROL Custom Alerts]面板，請按一下右上角的![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報")。

[!UICONTROL Custom Alerts]面板包含[!UICONTROL Alert Templates]檢視，其中列出為帳戶建立的所有警報範本，您可從其中建立、編輯、暫停、重新啟用和刪除警報範本。 [!UICONTROL Triggered Alerts]檢視會列出產生的警示執行個體。

## 可用動作

* [檢視觸發的警報](#alert-view)

* [檢視自訂警報範本](#alert-template-view)

* [建立自訂警報範本](#alert-template-create)

* [編輯自訂警報範本](#alert-template-edit)

* [暫停自訂警報範本](#alert-template-pause)

* [啟動自訂警報範本](#alert-template-activate)

* [刪除自訂警報範本](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## 檢視觸發的警報 {#alert-view}

1. 按一下任何頁面右上角的![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報")。

1. 按一下「**[!UICONTROL Triggered Alerts]**」標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

## 檢視自訂警報範本 {#alert-template-view}

1. 在任何頁面的右上角，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報")，這會開啟至[!UICONTROL Alert Templates]索引標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

1. （選擇性）若要檢視警示範本的所有條件，請按一下條件數目（例如![範例自訂警示條件按鈕](/help/search-social-commerce/assets/custom-alert-criteria.png "範例自訂警示條件按鈕")）。

## 建立自訂警報範本 {#alert-template-create}

新通知範本的狀態為&quot;[!UICONTROL Active]&quot;。

1. 執行下列任一項作業：

   * 在任何頁面的右上方，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL Create Custom Alert]**。

   在任何頁面的右上方，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL View Custom Alerts]**，這會開啟至[!UICONTROL Alert Templates]索引標籤。 按一下&#x200B;**[!UICONTROL Create Alert]**。

1. 在&#x200B;**[!UICONTROL Entity]**、**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**&#x200B;和&#x200B;**[!UICONTROL Scheduling and Delivery]**&#x200B;索引標籤上指定[警示設定](#alert-template-settings)。

   您可以按一下索引標簽名稱（例如「篩選器」）或按一下右下角的&#x200B;**[!UICONTROL Next]**，在索引標籤之間移動。

1. 在[!UICONTROL Summary]索引標籤上，按一下&#x200B;**[!UICONTROL Create Alert]**。

## 編輯自訂警報範本 {#alert-template-edit}

1. 在右上角，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL View Custom Alerts]**，這會開啟至[!UICONTROL Alert Templates]索引標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

1. 在範本名稱旁邊，按一下![編輯](/help/search-social-commerce/assets/edit-new.png "編輯")。

1. 在[!UICONTROL Edit Custom Alert]視窗中，編輯&#x200B;**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**&#x200B;和&#x200B;**[!UICONTROL Scheduling and Delivery]**&#x200B;索引標籤上的[警示設定](#alert-template-settings)。

   您可以按一下索引標簽名稱（例如「篩選器」）或按一下右下角的&#x200B;**[!UICONTROL Next]**，在索引標籤之間移動。

1. 在[!UICONTROL Summary]索引標籤上，按一下&#x200B;**[!UICONTROL Update Alert]**。

## 暫停自訂警報範本 {#alert-template-pause}

1. 在右上角，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL View Custom Alerts]**，這會開啟至[!UICONTROL Alert Templates]索引標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

1. 在範本列中，選取&#x200B;*[!UICONTROL Paused]*。

## 啟動自訂警報範本 {#alert-template-activate}

1. 在右上角，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL View Custom Alerts]**，這會開啟至[!UICONTROL Alert Templates]索引標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

1. 在範本列中，選取&#x200B;*[!UICONTROL Active]*。

## 刪除自訂警報範本 {#alert-template-delete}

您只能刪除您建立的警示範本。

1. 在右上角，按一下![自訂警報](/help/search-social-commerce/assets/custom-alert.png "自訂警報") > **[!UICONTROL View Custom Alerts]**，這會開啟至[!UICONTROL Alert Templates]索引標籤。

1. （可選）篩選清單以包含特定實體型別的警示，或搜尋範本名稱中的文字字串。 搜尋查詢不區分大小寫。

1. 在範本列中，按一下![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

1. 在確認訊息方塊中，按一下&#x200B;**[!UICONTROL Delete]**。

## 自訂警報範本設定 {#alert-template-settings}

| 標籤 | 引數 | 說明 |
|--- |--- |--- |
|  | [!UICONTROL Name] | 警示名稱。 它必須至少包含五個字元。 |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | 要評估的實體型別： <i>[!UICONTROL Portfolio]</i>、<i>[!UICONTROL Campaign]</i>或<i>[!UICONTROL Ad Group]</i>。 |
| [!UICONTROL Date Range] | [!UICONTROL Period] | 要評估警示條件的日期範圍。 量度會在日期範圍內以彙總方式評估。 選項範圍從&#x200B;*[!UICONTROL Yesterday]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 |
| [!UICONTROL Filters] | \[定義的篩選器\] | 在[!UICONTROL Scheduling and Delivery]標籤上指定的時間觸發警示的條件。 可用的欄會因圖元型別而異。 所有篩選器都使用布林函式AND連結，這表示必須符合所有指定的條件。<ul><li><p>若要新增篩選器，請執行下列動作：<p><ol><li><p>（選擇性）若要依文字字串篩選欄名稱，請在[!UICONTROL ADD FILTER]輸入欄位中輸入搜尋字串。</p></li><li><p>在欄清單中，選取欄名稱。</p></li><li><p>在欄上定義篩選器：</p></li><ul><li><p>（沒有輸入欄位的篩選器）按一下第二個功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭頭")，然後選取要包含的每個值旁的核取方塊。</p></li><li><p>（具有輸入欄位的所有其他篩選器）從第二個功能表選取運運算元，然後輸入適用的值。</p><p>例如，如果您已選取「點按」欄，且只想傳回點按超過100次的列，則選取「大於」並在輸入欄位中輸入100。</p><p>根據資料型別，可用的運運算元可能包括<i>大於</i>、<i>小於</i>、<i>等於</i>、<i>包含</i>、<i>不包含</i>、<i>開頭為</i>、<i>結尾為</i>、<i>無值</i>、<i>具有值</i>、<i>在</i>之前、<i>在</i>之後，或<i>無日期</i>。</p><p>**注意：**&#x200B;文字值不區分大小寫。 例如，如果您依名稱含有「貸款」的行銷活動進行篩選，結果可能包含「消費者貸款」和「貸款申請」。</p></li></ol><li><p>若要移除篩選器，請按一下篩選器定義旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[when\] | 警報檢查指定條件篩選器的頻率，並在符合所有條件時傳送電子郵件通知：<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*星期*> &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*第NN*>天&lt;*NN*> `[AM\|PM]`]</p></li></ul>**注意：**&#x200B;此值不會影響評估期間。 |
|  | [!UICONTROL Email Recipients] | （只有警報範本的建立者可編輯；其他所有人只能唯讀）觸發警報時，要傳送通知的已註冊搜尋、社交和Commerce使用者。 依預設，會選取使用者帳戶的名稱。 可選擇新增或移除有權存取廣告商資料的使用者。<br><br>當警示包含最多1000筆記錄時，會將CSV版本的警示附加至電子郵件訊息。 |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
