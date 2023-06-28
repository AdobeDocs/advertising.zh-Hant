---
title: 設定 [!DNL Google Analytics] 以資料來源檢視
description: 瞭解如何從設定資料來源 [!DNL Google Analytics] 檢視。
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 設定 [!DNL Google Analytics] 以資料來源檢視

*僅限代理公司管理員、代理公司帳戶管理員、Adobe帳戶管理員及管理員*

您可以為每個使用者建立一個資料來源 [!DNL Google Analytics] 帳戶、屬性和檢視組合。

若要整合多個屬性的量度或單一屬性的多個檢視，請為每個屬性設定個別的資料來源。

1. [執行整合的所有先決條件 [!DNL Google Analytics] 帳戶](data-source-prerequisites.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 在 [!UICONTROL Deployment Prerequisites] 對話方塊中，選取核取方塊以確認必要的自訂維度「ef_id」已實作於 [!DNL Google Analytics] 帳戶，然後按一下 **[!UICONTROL Continue]**.

   貴組織中的其他角色可能已執行某些先決條件。 如果您對先決條件有任何疑問，請洽詢您的Adobe客戶團隊。

1. 輸入 [資料來源設定](data-source-settings.md)：

   1. 在 **[!UICONTROL Connect to [!DNL Google Analytics]]** 章節，請執行下列動作。

      1. 輸入數值ID [!DNL Google Analytics] 帳戶。

      1. 輸入用於存取此資料來源資料的電子郵件地址。 電子郵件地址必須註冊到 [!DNL Google] 帳戶並擁有的「讀取和分析」許可權 [!DNL Google Analytics] 帳戶。 請參閱 [在中指派使用者許可權的說明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >若要確保僅特定於 [!DNL Google Analytics] 屬性和檢視可在Adobe Advertising中使用，使用只能存取這些屬性和檢視的電子郵件地址登入。

         >[!NOTE]
         >
         >如果您稍後變更此電子郵件帳戶的密碼，則會關閉與電子郵件帳戶的所有開啟連線。 若要繼續同步資料，請返回此頁面並 [重新驗證](data-source-reauthenticate.md).

      1. 選取核取方塊以授權Adobe Advertising存取帳戶的量度。

      1. 按一下 **[!UICONTROL Authenticate]**.

   1. 在 [!UICONTROL Account Details] 區段，指定要匯入量度的屬性和檢視。 此外，指定填入「ef_id」查詢字串引數值的自訂維度。

   1. 在 [!UICONTROL Import Metrics] 區段，指定要包含在摘要中的量度。

      您無法移除 [!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]，或 [!UICONTROL Session Duration]，這些引數會自動包含在內。 您最多可以新增16個其他有效量度或沒有資料的量度。

      >[!WARNING]
      >
      >[!DNL Google Analytics] 在單一資料摘要中最多允許10個量度。 Search、Social和Commerce最多可支援兩個摘要，總共20個量度，但使用第二個摘要會將您的API呼叫加倍 [!DNL Google Analytics]. 如果您有許多量度，請僅選取您想在最佳化目標中使用的量度。 檢視更多關於 [API要求的配額和呼叫限製為 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. 在 [!UICONTROL Metric Tag] 區段，輸入要附加至資料來源之每個量度的標籤名稱。

1. 在右上角，按一下 **[!UICONTROL Post]**.

   資料來源命名為「AccountName > PropertyName > ViewName」，且會自動啟動。 若要暫停資料來源，請參閱「[暫停來自資料來源的摘要](data-source-pause.md).」

   每日資料同步作業於廣告商時區的05:00開始，完成後的隔天便可使用量度。 量度可供使用後，即會顯示於 [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). 每個新的交易屬性都命名為「`ga:backEndMetricName_propertyID_viewID`，」其中，「backEndMetricName」是API使用的量度名稱。 每個新交易屬性的顯示名稱是&quot;`friendlyMetricName_ga:MetricTag`，其中「friendlyMetricName」是出現在中的量度名稱 [!DNL Google Analytics] 而「MetricTag」是 [!UICONTROL Metric Tag] 定義於資料來源設定中。

   您可以將這些量度直接新增至行銷活動管理和產品組合管理檢視、報告和最佳化目標。

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定的必要條件 [!DNL Google Analytics] 資料來源](data-source-prerequisites.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停資料來源的同步處理](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
