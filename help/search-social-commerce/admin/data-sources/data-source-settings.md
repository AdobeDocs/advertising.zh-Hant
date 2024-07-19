---
title: '[!DNL Google Analytics]資料來源設定'
description: 參考 [!DNL Google Analytics] 資料來源的必要設定。
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# [!DNL Google Analytics]資料來源設定

| 章節 | 引數 | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | 從中提取資料的[!DNL Google Analytics]帳戶識別碼。 提取資料的所有API使用方式都會向指定帳戶計費。 帳戶必須提供指定電子郵件地址的「讀取和分析」許可權。<br><br>若要尋找您的識別碼，請登入[!DNL Google Analytics]。 按一下左上角的&#x200B;**[!DNL All accounts]**&#x200B;以開啟您的帳戶清單。 每個帳戶的ID都位於帳戶名稱下。 |
| | [!UICONTROL Google Analytics Login] | 指定用來存取此資料來源資料的登入/電子郵件地址。 登入必須註冊到[!DNL Google]帳戶，並且擁有[!DNL Google Analytics]帳戶的「讀取和分析」許可權。 請參閱 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587)中指派使用者許可權的[指示。<br><br><b>注意：</b>如果您變更這個登入帳戶的密碼，則所有與該帳戶開啟的連線都會關閉。 若要繼續同步處理資料，請返回此頁面，然後[重新驗證](data-source-reauthenticate.md)。 |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （唯讀；僅限已連線的帳戶）帳戶名稱。 |
| | [!UICONTROL Google Analytics Property] | 要從中收集[!DNL Google Analytics]帳戶資料的屬性（網站、行動應用程式或裝置）。<br><br>若要整合多個屬性的量度，請為每個屬性設定個別的資料來源。 |
| | [!UICONTROL Google Analytics View] | 包含您要存取之資料集的檢視。 如果屬性有多個檢視，請考慮從包含所有資料的最高層級提取未篩選的檢視。<br><br>若要為相同屬性的多個檢視整合量度，請為每個檢視設定個別的資料來源。 請確定檢視不含重疊資料。 |
| | [!UICONTROL Google Analytics Dimension] | 以Adobe Advertising「ef_id」查詢字串引數值填入的[!DNL Google Analytics]自訂維度。 如果您沒有看到列出的正確維度，請聯絡您的[!DNL Google Analytics]實作團隊。<br><br>使用&quot;ef_id&quot;作為從[!DNL Google Analytics]傳遞資料給Adobe Advertising的主索引鍵。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定[!DNL Google Analytics]屬性和檢視的所有可用量度（未針對資料來源匯入），依類別組織。 此清單包含匯入的易記名稱和後端名稱（以「ga」開頭）。 用於每個量度。 [!UICONTROL Refresh]按鈕會以[!DNL Google Analytics]中的任何新度量重新整理清單。<br><br>若要匯入可用的量度，請將其拖曳至[!UICONTROL Selected Metrics]區段。<br><br>檢視Advertising Cloud中的[可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)。 |
| | 選取的量度 | 針對資料來源匯入的指定[!DNL Google Analytics]屬性和檢視的所有量度，以及每個量度的驗證狀態。 清單包含每個量度的匯入好記名稱和後端名稱（以「`ga.`」開頭）。 每個資料來源可以包含四個您無法移除的預設流量量度（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]和[!UICONTROL Session Duration]），以及最多16個沒有資料的其他有效量度或量度。 您可以隨時編輯量度清單。<br><br>若要匯入量度，請在[!UICONTROL Available Metrics]窗格中選取該量度，並將其拖曳到這裡。<br><br><b>警告：</b> [!DNL Google Analytics]在單一資料摘要中最多允許10個量度。 搜尋、社交和Commerce中的每個資料來源最多可包含兩個摘要，總共20個量度，但使用第二個摘要時，您的API呼叫會加倍為[!DNL Google Analytics]。 如果您有許多量度，請僅選取您想在最佳化目標中使用的量度。 您可以在[ [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)中檢視此專案的配額。 檢視有關 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)之API要求的配額和呼叫限制的[詳細資訊。<br><br><b>附註：</b><br><ul><li>易記名稱會匯入為[!UICONTROL Admin] > [!UICONTROL Transactions Properties]檢視中量度的顯示名稱，且會附加「<code>_ga：&lt;在量度標籤欄位中設定的metric_tag」</code>&quot; （例如&quot;Pageviews_ga：UK&quot;）。 您可以選擇編輯自訂目標和自訂量度的顯示名稱，但所有一般量度的顯示名稱每天都會以[!DNL Google Analytics]中的好記名稱覆寫，並附加指定的標籤。</li><li>頁面檢視、工作階段、跳出率（以跳出/工作階段來計算）和工作階段持續時間會自動納入產品組合競標演演算法中。 您可以手動將任何其他量度新增至投資組合目標。</li><li>當您從資料來源移除量度時，Adobe Advertising會根據一般的[資料保留原則](/help/search-social-commerce/reports/data-used-for-reports.md)保留歷史資料。</li></ul> |
| 量度標籤 | 量度標籤 | 附加至每個所選[!DNL Google Analytics]量度(Adobe Advertising)的標籤，前面加上&quot;<code>_ga：</code>&quot; （例如&quot;Pageviews_ga：&lt;metric_tag>&quot;）。 標籤可以是2-5個英數字元，且對廣告商而言必須是唯一的。<br><br>此標籤可協助您識別每個量度的資料來源。 當您設定多個資料來源時，此標籤尤其重要，因為每個資料來源都包含某些相同的量度名稱（包括[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]和[!UICONTROL Session Duration]，還有可能包含其他量度）。 附加不同的量度標籤可防止量度名稱重複。<br><br>例如，如果您為UK屬性和JP屬性設定個別的整合，您可能會使用「UK」和「JP」作為量度標籤。 這兩個屬性的[!UICONTROL Pageviews]量度會在Adobe Advertising中相應地顯示為「Pageviews_ga：UK」和「Pageviews_ga：JP」。 |

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
