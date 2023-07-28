---
title: 關於同步 [!DNL Google Analytics] 轉換量度
description: 瞭解同步 [!DNL Google Analytics] 最佳化和報告的轉換量度。
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 關於同步 [!DNL Google Analytics] 轉換量度

搜尋、社交和商務可以同步特定轉換量度 [!DNL Google Analytics] 帳戶、屬性和檢視的組合，用於最佳化和報告。 [頁面檢視](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews)， [工作階段](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions)， [跳出率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) （以跳出數/工作階段數計算），以及 [工作階段持續時間](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) 會自動包含在內。 每個資料來源最多可包含16個額外的量度。

>[!NOTE]
>
>Advertising DSP使用者可將轉換量度作為自訂目標並用於報表中。

所有資料傳輸的API使用方式都會在適用的中評估至專案 [!DNL Google Analytics] 帳戶。 您可在以下位置檢視此專案的配額： [此 [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 另請參閱 [!DNL Google Analytics] 檔案，以取得更多關於 [報告API請求的配額和呼叫限制](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

下列步驟概述從同步轉換資料的程式 [!DNL Google Analytics].

1. [執行先決條件工作](data-source-prerequisites.md)

   * 實作Adobe Advertising權杖(`ef_id` 查詢字串引數)，適用於所有適用的Advertising帳戶。

   * 擷取Adobe Advertising權杖(`ef_id` 查詢字串引數) [!DNL Custom Dimension] 在 [!DNL Google Analytics].

1. (代理商帳戶管理員、代理商帳戶管理員、 [!DNL Adobe] 帳戶管理員，僅限管理員使用者) [為每個建立單一資料來源 [!DNL Google Analytics] 帳戶、屬性和檢視組合](data-source-configure.md).

   若要整合多個屬性的量度或單一屬性的多個檢視，請分別為每個屬性設定個別的資料來源。

   設定資料來源後，Search、Social和Commerce會每天從廣告商時區的05:00開始提取資料。 量度可用後，您就可以將其納入行銷活動和產品組合管理檢視及報告中，並視需要用於最佳化目標。

>[!MORELIKETHIS]
>
>* [設定的先決條件 [!DNL Google Analytics] 資料來源](data-source-prerequisites.md)
>* [設定 [!DNL Google Analytics] 以資料來源檢視](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停資料來源的同步處理](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
