---
title: 將 [!DNL Google Analytics] 檢視設定為資料來源
description: 瞭解如何從 [!DNL Google Analytics] 檢視設定資料來源。
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 將[!DNL Google Analytics]檢視設定為資料來源

*僅限代理管理員、代理帳戶管理員、Adobe帳戶管理員和管理員*

您可以為每個[!DNL Google Analytics]帳戶、屬性和檢視組合建立一個資料來源。

若要整合多個屬性的量度或單一屬性的多個檢視，請分別為每個屬性設定個別的資料來源。

1. [執行整合 [!DNL Google Analytics] 帳戶](data-source-prerequisites.md)的所有必要條件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 在[!UICONTROL Deployment Prerequisites]對話方塊中，選取核取方塊以確認已在[!DNL Google Analytics]帳戶中實作必要的自訂維度「ef_id」，然後按一下&#x200B;**[!UICONTROL Continue]**。

   貴組織中的其他角色可能已執行某些先決條件。 如果您對先決條件有任何疑問，請洽詢您的Adobe客戶團隊。

1. 輸入[資料來源設定](data-source-settings.md)：

   1. 在&#x200B;**[!UICONTROL Connect to [!DNL Google Analytics]]**&#x200B;區段中，執行下列動作。

      1. 輸入[!DNL Google Analytics]帳戶的數值ID。

      1. 輸入用來存取此資料來源資料的電子郵件地址。 電子郵件地址必須註冊到[!DNL Google]帳戶，並且擁有[!DNL Google Analytics]帳戶的「讀取和分析」許可權。 請參閱 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587)中指派使用者許可權的[指示。

         >[!TIP]
         >
         >若要確保Adobe Advertising中只有特定的[!DNL Google Analytics]屬性和檢視可供使用，請使用只能存取這些屬性和檢視的電子郵件地址登入。

         >[!NOTE]
         >
         >如果您稍後變更此電子郵件帳戶的密碼，則會關閉所有與電子郵件帳戶開啟的連線。 若要繼續同步處理資料，請返回此頁面，然後[重新驗證](data-source-reauthenticate.md)。

      1. 選取核取方塊以授權Adobe Advertising存取帳戶的量度。

      1. 按一下&#x200B;**[!UICONTROL Authenticate]**。

   1. 在[!UICONTROL Account Details]區段中，指定要匯入之量度的屬性和檢視。 此外，請指定以「ef_id」查詢字串引數值填入的自訂維度。

   1. 在[!UICONTROL Import Metrics]區段中，指定要包含在摘要中的量度。

      您無法移除自動包含的[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]或[!UICONTROL Session Duration]。 您最多可以新增16個其他有效量度或沒有資料的量度。

      >[!WARNING]
      >
      >[!DNL Google Analytics]在單一資料摘要中最多允許10個量度。 搜尋、社交和Commerce最多可支援兩個摘要，總共20個量度，但使用第二個摘要會將您的API呼叫加倍為[!DNL Google Analytics]。 如果您有許多量度，請僅選取您想在最佳化目標中使用的量度。 檢視有關 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)之API要求的配額和呼叫限制的[詳細資訊。

   1. 在[!UICONTROL Metric Tag]區段中，輸入要附加至資料來源之每個量度的標籤名稱。

1. 按一下右上角的&#x200B;**[!UICONTROL Post]**。

   資料來源命名為「AccountName > PropertyName > ViewName」，且會自動啟動。 若要暫停資料來源，請參閱「[暫停來自資料Source的摘要](data-source-pause.md)」。

   每日資料同步作業於廣告商時區的05:00開始，完成後，第二天即可使用這些量度。 量度可用後，即可在[[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)中看到。 每個新的轉換量度都命名為「`ga:backEndMetricName_propertyID_viewID`」，其中「backEndMetricName」是API使用的量度名稱。 每個新轉換量度的顯示名稱是&quot;`friendlyMetricName_ga:MetricTag`&quot;，其中&quot;friendlyMetricName&quot;是出現在[!DNL Google Analytics]中的量度名稱，而&quot;MetricTag&quot;是在資料來源設定中定義的[!UICONTROL Metric Tag]。

   您可以直接將量度新增至行銷活動管理和產品組合管理檢視、報表和最佳化目標。

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
