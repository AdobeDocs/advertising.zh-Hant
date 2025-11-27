---
title: 清查摘要何時建立或刪除帳戶元件？
description: 瞭解當您發佈詳細目錄摘要時，在哪些情況下會建立和刪除帳戶元件。
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# 清查摘要何時建立或刪除帳戶元件？

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

透過範本傳播清查摘要檔案時，會依照以下方式建立和刪除帳戶元件。

>[!NOTE]
>
>廣告群組中絕對不會建立重複的廣告。

| 情境 | 範例 | 動作 |
|----|----|----|
| 摘要資料包含在行銷活動名稱、廣告群組名稱、關鍵字或產品群組中使用的欄新值。 | 先前的檔案：<br>Campaign=Hats<br>Campaign=Gloves<br><br>新檔案：<br>Campaign=Shoes | 如果廣告網路上不存在新的行銷活動、廣告群組、關鍵字或產品群組，則會建立該行銷活動。 |
| 摘要資料包含在廣告中使用的欄的新值。 | 上一個檔案：廣告包含的價格=20<br><br>新檔案：對於相同的廣告，價格=10 | 當[!DNL Microsoft Advertising]個展開的文字廣告、[!DNL Yahoo! Japan ads]或[!DNL Yandex]個廣告的廣告文案變更時，現有的廣告會遭到刪除並建立新的廣告。<br><br>當其他廣告型別的廣告復本已變更，或廣告中的[!DNL Google Ads]廣告引數（{param1}或{param2}）使用了適用的欄時，則會更新現有的廣告。 |
| 自上次傳播以來，行銷活動、廣告群組、關鍵字或產品群組的範本設定已變更。 | 先前的設定:Keyword=[關鍵字]<br><br>新設定： Keyword=&lt;Color>[關鍵字] | 如果廣告網路上不存在新的行銷活動、廣告群組、關鍵字或產品群組，則會建立該行銷活動。 |
| 自上次傳播後，廣告的範本設定已變更。 | 先前的設定：廣告說明=&quot;立即購買[類別]&quot;。<br><br>新設定：廣告說明=「立即購買[品牌]」。 | 當[!DNL Microsoft Advertising]個展開的文字廣告、[!DNL Yahoo! Japan ads]或[!DNL Yandex]個廣告的廣告文案變更時，現有的廣告會遭到刪除並建立新的廣告。<br><br>當其他廣告型別的廣告復本有所變更，或此變更反映廣告中用於單一[!DNL Google Ads]廣告引數（{param1}或{param2}）的欄位有所變更，則會更新現有的廣告。 |
| 新的摘要資料不包含現有行銷活動或廣告群組的列。 | 不適用 | 現有行銷活動和廣告群組維持不變。 |
| 新的摘要資料不包含現有廣告群組、廣告、關鍵字或產品群組的列。 | 不適用 | 根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)，現有的廣告群組、廣告、關鍵字或產品群組會維持原狀、暫停或刪除。 |
| 現有父產品群組的新摘要資料不包含其現有子產品群組的列。 | 不適用 | 根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)，現有的父級產品群組會維持原狀或被刪除。 <b>注意：</b>如果摘要資料設定是設定為暫停遺漏的行專案，則父產品群組仍會被刪除，因為您無法暫停產品群組。 |
| 新摘要資料中包含的廣告群組、廣告、關鍵字或產品群組列，在先前的資料中為a)但b)此後已省略，並根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)暫停。 | 不適用 | 現有的廣告群組、廣告、關鍵字或產品群組會重新啟用，而不會遺失任何歷史記錄或品質分數。 |
| 新摘要資料中包含的廣告群組、廣告、關鍵字或產品群組列，在先前的資料中為a)，但在之後已省略b)，且已根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)刪除。 | 不適用 | 會建立新的廣告群組、廣告、關鍵字或產品群組。 |
| 您已對「[!UICONTROL Delete negative keywords when omitted from list]」停用行銷活動或廣告群組層級選項。 | 負面關鍵字清單包括「coupe」和「sport car」。<br><br>廣告群組已經包含負關鍵字「SUV」。 | 任何不在清單上的現有負面關鍵字都會維持原狀。 |
| 您已將行銷活動或廣告群組層級選項啟用為「[!UICONTROL Delete negative keywords when omitted from list]」，且存在不在清單中的負面關鍵字。 | 負面關鍵字清單包括「coupe」和「sport car」。<br><br>廣告群組已經包含負關鍵字「SUV」。 | 當摘要檔案透過範本傳播時，會刪除先前使用範本建立的任何未指定的負關鍵字。 不過，使用其他方法建立的任何未指定的負面關鍵字（例如在普通大量表單、[!UICONTROL Campaigns]檢視或在廣告網路的廣告編輯器中）都會維持不變。 |
| 已發佈摘要檔案之元件的排程結束日期發生。 | 不適用 | 現有行銷活動維持不變。 根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)，現有的廣告群組、廣告和關鍵字會維持原狀、暫停或刪除。 |
| 專案的庫存量會降到低於[摘要資料設定](feed-settings-manage.md#feed-data-settings)中指定的最小值。 | 上一個檔案： stock=10<br><br>新檔案： stock=0 | 現有行銷活動維持不變。 根據[摘要資料設定](feed-settings-manage.md#feed-data-settings)，現有的廣告群組、廣告、關鍵字和產品群組會暫停或刪除。 |
| 專案的庫存等級會回到[摘要資料設定](feed-settings-manage.md#feed-data-settings)中指定的最小值以上。 | 上一個檔案： stock=0<br><br>新檔案： stock=10 | 暫停現有廣告、關鍵字或產品群組時，它們會重新啟用，而不會失去任何歷史記錄或品質分數。 當沒有廣告、關鍵字或產品群組存在時（例如，如果先前因為庫存等級低於最低值而刪除了這些廣告、關鍵字或產品群組），則會建立新的廣告、關鍵字或產品群組。 |

>[!MORELIKETHIS]
>
>* [關於使用詳細目錄摘要自動化廣告管理](inventory-feeds-about.md)
