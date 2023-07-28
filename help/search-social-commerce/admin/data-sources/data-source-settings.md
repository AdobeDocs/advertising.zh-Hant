---
title: 『[!DNL Google Analytics] 資料來源設定
description: 參考以下專案的必要設定： [!DNL Google Analytics] 資料來源。
role: User, Admin
exl-id: 531351b4-07f1-43ef-a3d2-892a49ffb5ca
feature: Search Data Sources
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# [!DNL Google Analytics] 資料來源設定

| 章節 | 引數 | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | 的ID [!DNL Google Analytics] 從中提取資料的帳戶。 提取資料的所有API使用方式都會向指定帳戶計費。 帳戶必須提供指定電子郵件地址的「讀取和分析」許可權。<br><br>若要尋找您的ID，請登入 [!DNL Google Analytics]. 在左上方，按一下 **[!DNL All accounts]** 以開啟您的帳戶清單。 每個帳戶的ID都位於帳戶名稱下。 |
| | [!UICONTROL Google Analytics Login] | 指定用來存取此資料來源資料的登入/電子郵件地址。 登入必須註冊到 [!DNL Google] 帳戶並擁有的「讀取和分析」許可權 [!DNL Google Analytics] 帳戶。 請參閱 [在中指派使用者許可權的說明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).<br><br><b>注意：</b> 如果您變更此登入帳戶的密碼，則會關閉與該帳戶的所有開啟連線。 若要繼續同步資料，請返回此頁面並 [重新驗證](data-source-reauthenticate.md). |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （唯讀；僅限已連線的帳戶）帳戶名稱。 |
| | [!UICONTROL Google Analytics Property] | 從中收集資料的屬性（網站、行動應用程式或裝置）。 [!DNL Google Analytics] 帳戶。<br><br> 若要整合多個屬性的量度，請為每個屬性設定個別的資料來源。 |
| | [!UICONTROL Google Analytics View] | 包含您要存取之資料集的檢視。 如果屬性有多個檢視，請考慮從包含所有資料的最高層級提取未篩選的檢視。<br><br>若要為相同屬性的多個檢視整合量度，請為每個檢視設定個別的資料來源。 請確定檢視不含重疊資料。 |
| | [!UICONTROL Google Analytics Dimension] | 此 [!DNL Google Analytics] 以Adobe Advertising「ef_id」查詢字串引數值填入的自訂維度。 如果您未看到列出的正確維度，請聯絡您的 [!DNL Google Analytics] 實作團隊。<br><br>&quot;ef_id&quot;會作為傳遞資料的主要金鑰，從 [!DNL Google Analytics] 以Adobe Advertising。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定的所有可用量度 [!DNL Google Analytics] 未針對資料來源匯入的屬性和檢視，依類別組織。 此清單包含匯入的易記名稱和後端名稱（以「ga」開頭）。 用於每個量度。 此 [!UICONTROL Refresh] 按鈕會以中的任何新量度重新整理清單 [!DNL Google Analytics].<br><br>若要匯入可用的量度，請將其拖曳至 [!UICONTROL Selected Metrics] 區段。<br><br>請參閱&quot;[可用 [!DNL Google Analytics] Advertising Cloud中的量度](data-source-ga-metrics.md).」 |
| | 選取的量度 | 指定的所有量度 [!DNL Google Analytics] 為資料來源匯入的屬性和檢視，以及每個量度的驗證狀態。 此清單包含匯入的易記名稱和後端名稱（以&quot;開頭）`ga.`&quot;)作為每個量度的。 每個資料來源可以包含四個您無法移除的預設流量量度([!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]、和 [!UICONTROL Session Duration])以及最多16個其他有效量度或沒有資料的量度。 您可以隨時編輯量度清單。<br><br>若要匯入量度，請在 [!UICONTROL Available Metrics] 窗格並拖曳到這裡。<br><br><b>注意：</b> [!DNL Google Analytics] 在單一資料摘要中最多可允許10個量度。 搜尋、Social和Commerce中的每個資料來源最多可包含兩個摘要，總計20個量度，但使用第二個摘要會將您的API呼叫加倍 [!DNL Google Analytics]. 如果您有許多量度，請僅選取您想在最佳化目標中使用的量度。 您可在以下位置檢視此專案的配額： [此 [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 檢視更多關於 [的API請求配額和呼叫限制 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).<br><br><b>附註：</b><br><ul><li>易記名稱會匯入為中量度的顯示名稱 [!UICONTROL Admin] > [!UICONTROL Transactions Properties] 檢視並附加&quot;<code>_ga：&lt;metric_tag configured=&quot;&quot; in=&quot;&quot; the=&quot;&quot; metric=&quot;&quot; tag=&quot;&quot; field=&quot;&quot;></code>&quot; （例如&quot;Pageviews_ga：UK&quot;）。 您可以選擇編輯自訂目標和自訂量度的顯示名稱，但所有常見量度的顯示名稱每天都會以中的易記名稱覆寫 [!DNL Google Analytics]，並附加指定的標籤。</li><li>頁面檢視、工作階段、跳出率（以跳出/工作階段來計算）和工作階段持續時間會自動納入產品組合競標演演算法中。 您可以手動將任何其他量度新增至投資組合目標。</li><li>當您從資料來源移除量度時，Adobe Advertising會根據正常情況保留歷史資料 [資料保留原則](/help/search-social-commerce/reports/data-used-for-reports.md).</li></ul> |
| 量度標籤 | 量度標籤 | 要附加到每個所選專案的標籤 [!DNL Google Analytics] Adobe Advertising中的量度，開頭為&quot;<code>_ga：</code>&quot; (例如&quot;Pageviews_ga：&lt;metric_tag>「)。 標籤可以是2-5個英數字元，且對廣告商而言必須是唯一的。<br><br>此標籤可協助您識別每個量度的資料來源。 當您設定多個資料來源時，此標籤尤其重要，因為每個資料來源都包含一些相同的量度名稱(包括 [!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]、和 [!UICONTROL Session Duration]，並可能包含其他量度)。 附加不同的量度標籤可防止量度名稱重複。<br><br>例如，如果您為UK屬性和JP屬性設定個別的整合，您可能會使用「UK」和「JP」作為量度標籤。 此 [!UICONTROL Pageviews] 這兩個屬性的量度會在Adobe Advertising中適當顯示為「Pageviews_ga：UK」和「Pageviews_ga：JP」。 |

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定的先決條件 [!DNL Google Analytics] 資料來源](data-source-prerequisites.md)
>* [設定 [!DNL Google Analytics] 以資料來源檢視](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停資料來源的同步處理](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
