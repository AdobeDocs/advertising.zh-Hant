---
title: 關於同步 [!DNL Google Analytics] 轉換量度
description: 瞭解如何同步 [!DNL Google Analytics] 轉換量度以最佳化及報告。
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# 關於同步[!DNL Google Analytics]轉換量度

搜尋、社交和Commerce可以同步特定[!DNL Google Analytics]帳戶、屬性和檢視組合的轉換量度，以最佳化及報告。 [頁面檢視次數](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews)、[工作階段](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions)、[跳出率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) （以跳出數/工作階段數計算）以及[工作階段持續時間](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration)會自動納入。 每個資料來源最多可包含16個額外的量度。

>[!NOTE]
>
>Advertising DSP使用者可將轉換量度作為自訂目標和報表使用。

所有資料傳輸的API使用量皆已評估至適用[!DNL Google Analytics]帳戶中的專案。 您可以在[&#x200B; [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)中檢視此專案的配額。 請參閱[!DNL Google Analytics]檔案以取得報告API要求[的](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)配額和呼叫限制的相關資訊。

下列步驟概述從[!DNL Google Analytics]同步轉換資料的程式。

1. [執行先決條件工作](data-source-prerequisites.md)

   * 在登陸頁面URL中為所有適用的Advertising帳戶實作Adobe Advertising Token （`ef_id`查詢字串引數）。

   * 在`ef_id`的[!DNL Custom Dimension]中擷取Adobe Advertising Token （[!DNL Google Analytics]查詢字串引數）。

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
