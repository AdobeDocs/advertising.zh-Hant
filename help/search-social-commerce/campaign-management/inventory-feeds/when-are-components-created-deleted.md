---
title: 清查摘要何時建立或刪除帳戶元件？
description: 瞭解當您發佈詳細目錄摘要時，在哪些情況下會建立和刪除帳戶元件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# 清查摘要何時建立或刪除帳戶元件？

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

透過範本傳播庫存摘要檔案時，會依照以下方式建立和刪除帳戶元件。

>[!NOTE]
>
>廣告群組中絕不會建立重複的廣告。

| 情境 | 範例 | 動作 |
|----|----|----|
| 摘要資料包含在行銷活動名稱、廣告群組名稱、關鍵字或產品群組中使用的欄的新值。 | 先前的檔案：<br>Campaign=Hats<br>Campaign=Gloves<br><br>新檔案：<br>Campaign=鞋子 | 如果廣告網路上不存在新的行銷活動、廣告群組、關鍵字或產品群組，則會建立該行銷活動。 |
| 摘要資料包含在廣告中使用的欄的新值。 | 上一個檔案：廣告包含的價格=20<br><br>新檔案：若是同一個廣告，價格為10 | 當廣告復本用於 [!DNL Microsoft® Advertising] 展開的文字廣告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 廣告已變更，現有廣告已刪除，並建立新廣告。<br><br>當針對其他廣告型別變更廣告復本，或適用的欄用於 [!DNL Google Ads] 廣告中的廣告引數（{param1}或{param2}），則會更新現有廣告。 |
| 自上次傳播以來，行銷活動、廣告群組、關鍵字或產品群組的範本設定已變更。 | 上一個設定：關鍵字=[關鍵字]<br><br>新設定： Keyword=&lt;color>[關鍵字] | 如果廣告網路上不存在新的行銷活動、廣告群組、關鍵字或產品群組，則會建立該行銷活動。 |
| 自上次傳播後，廣告的範本設定已變更。 | 先前設定：廣告說明=&quot;購買 [類別] 現在。」<br><br>新設定：廣告說明=&quot;購買 [品牌] 現在。」 | 當廣告復本用於 [!DNL Microsoft® Advertising] 展開的文字廣告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 廣告已變更，現有廣告已刪除，並建立新廣告。<br><br>當其他廣告型別的廣告副本變更時，或當變更反映用於單一廣告的欄中的變更時 [!DNL Google Ads] 廣告中的廣告引數（{param1}或{param2}），則會更新現有廣告。 |
| 新的摘要資料不包含現有行銷活動或廣告群組的列。 | 不適用 | 現有行銷活動和廣告群組維持不變。 |
| 新的摘要資料不包含現有廣告群組、廣告、關鍵字或產品群組的列。 | 不適用 | 現有的廣告群組、廣告、關鍵字或產品群組會維持原狀、暫停或刪除，依據為 [摘要資料設定](feed-settings-manage.md#feed-data-settings). |
| 現有父產品群組的新摘要資料不包含其現有子產品群組的列。 | 不適用 | 現有的父項產品群組會維持原狀，或根據 [摘要資料設定](feed-settings-manage.md#feed-data-settings). <b>注意：</b> 如果摘要資料設定是設定為暫停缺少的行專案，則父產品群組仍會遭到刪除，因為您無法暫停產品群組。 |
| 新的摘要資料包含廣告群組、廣告、關鍵字或產品群組的列，這些資料在先前的資料中為a)，但b)在資料後被省略，並根據 [摘要資料設定](feed-settings-manage.md#feed-data-settings). | 不適用 | 現有的廣告群組、廣告、關鍵字或產品群組會重新啟用，而不會遺失任何歷史記錄或品質分數。 |
| 新的摘要資料中包含的廣告群組、廣告、關鍵字或產品群組列，在先前的資料中為a)，但b)自那時起被省略，並根據 [摘要資料設定](feed-settings-manage.md#feed-data-settings). | 不適用 | 會建立新的廣告群組、廣告、關鍵字或產品群組。 |
| 您已停用「 」的行銷活動或廣告群組層級選項[!UICONTROL Delete negative keywords when omitted from list].」 | 負面關鍵字清單包括「coupe」和「sports car」。<br><br>廣告群組已包含負關鍵字「SUV」。 | 任何不在清單上的現有負面關鍵字都會保持原樣。 |
| 您已為「 」啟用行銷活動或廣告群組層級選項[!UICONTROL Delete negative keywords when omitted from list]「 」和不在清單中的負面關鍵字存在。 | 負面關鍵字清單包括「coupe」和「sports car」。<br><br>廣告群組已包含負關鍵字「SUV」。 | 當摘要檔案透過範本傳播時，會刪除先前使用範本建立的任何未指定負面關鍵字。 但是，任何使用其他方法建立的未指定的負面關鍵字(例如在Bulksheets中， [!UICONTROL Campaigns] 檢視或廣告網路的廣告編輯器中的檢視維持不變。 |  | 已發佈摘要檔案之元件的排程結束日期發生。 | 不適用 | 現有行銷活動維持不變。 現有的廣告群組、廣告和關鍵字會維持原狀、暫停或刪除，依據為 [摘要資料設定](feed-settings-manage.md#feed-data-settings). |
| 料號的存貨層次會下降到低於中指定的最小值。 [摘要資料設定](feed-settings-manage.md#feed-data-settings). | 上一個檔案： stock=10<br><br>新檔案： stock=0 | 現有行銷活動維持不變。 現有的廣告群組、廣告、關鍵字及產品群組會根據 [摘要資料設定](feed-settings-manage.md#feed-data-settings). |
| 料號的庫存量會回溯至超過中指定的最小值。 [摘要資料設定](feed-settings-manage.md#feed-data-settings). | 上一個檔案： stock=0<br><br> 新檔案： stock=10 | 暫停現有廣告、關鍵字或產品群組時，它們會重新啟用，而不會失去任何歷程記錄或品質分數。 當不存在廣告、關鍵字或產品群組時（例如，如果先前由於庫存等級低於最低值而刪除了這些廣告、關鍵字或產品群組），則會建立新的廣告、關鍵字或產品群組。 |

>[!MORELIKETHIS]
>
>* [關於使用庫存摘要自動化廣告管理](inventory-feeds-about.md)
>* [使用詳細目錄摘要管理行銷活動資料的工作流程](inventory-feeds-workflow.md)

