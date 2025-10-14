---
title: 關於同步 [!DNL Google Analytics] 轉換量度
description: 瞭解如何同步 [!DNL Google Analytics] 轉換量度以最佳化及報告。
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 關於同步[!DNL Google Analytics]轉換量度

搜尋、社交和Commerce可以同步特定[!DNL Google Analytics]帳戶、屬性和檢視組合的轉換量度，以最佳化及報告。 [頁面檢視次數](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews)、[工作階段](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions)、[跳出率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) （以跳出數/工作階段數計算）以及[工作階段持續時間](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration)會自動納入。 每個資料來源最多可包含16個額外的量度。

>[!NOTE]
>
>Advertising DSP使用者可將轉換量度作為自訂目標和報表使用。

所有資料傳輸的API使用量皆已評估至適用[!DNL Google Analytics]帳戶中的專案。 您可以在[&#x200B; [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)中檢視此專案的配額。 請參閱[!DNL Google Analytics]檔案以取得報告API要求[&#128279;](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)的配額和呼叫限制的相關資訊。

下列步驟概述從[!DNL Google Analytics]同步轉換資料的程式。

1. [執行先決條件工作](data-source-prerequisites.md)

   * 在登陸頁面URL中為所有適用的Advertising帳戶實作Adobe Advertising權杖（`ef_id`查詢字串引數）。

   * 在[!DNL Google Analytics]的[!DNL Custom Dimension]中擷取Adobe Advertising權杖（`ef_id`查詢字串引數）。

1. （僅限代理帳戶管理員、代理帳戶管理員、[!DNL Adobe]帳戶管理員和管理員使用者） [針對每個 [!DNL Google Analytics] 帳戶、屬性和檢視組合，建立一個資料來源](data-source-configure.md)。

   若要整合多個屬性的量度或單一屬性的多個檢視，請分別為每個屬性設定個別的資料來源。

   設定資料來源後，Search、Social和Commerce會每天從廣告商時區的05:00開始提取資料。 量度可用後，您就可以將其納入行銷活動和產品組合管理檢視及報告中，並視需要用於最佳化目標。

>[!MORELIKETHIS]
>
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
