---
title: 從Adobe Analytics建立轉換量度 [!DNL eVars] 和prop
description: 設定自訂成功事件量度，使用 [!DNL eVar] — 和 [!DNL prop]-level資料。
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 686ca84a34117bcb4f4d5f295ed27bb308e6f287
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 從Adobe Analytics建立轉換量度 [!DNL eVars] 和 [!DNL props]

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

您可以使用成功事件量度，根據最符合您品牌目標的Adobe Analytics網站資料來最佳化DSP套件和搜尋、社交和商務行銷活動。 您可以根據現有的設定自訂成功事件量度 [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 和 [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) 透過漏斗 [!DNL eVar] — 和 [!DNL prop]-level資料匯入事件。 其他 [!DNL Analytics] 量度（包括標準、自訂和保留的轉換量度和流量量度）會自動在DSP和Search、Social和Commerce中使用。

![使用範例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用範例")

下列大部分工作必須由 [!DNL Analytics] 管理員或其他使用者。 如果您需要協助，請聯絡(DSP使用者) DSP技術支援團隊，地址為 `adcloud_support@adobe.com` 或（搜尋、社交和商務使用者）您的Adobe帳戶團隊。

1. 在 [!DNL Analytics]， [建立預留位置成功事件](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   使用下列其他引數：

   **型別：** `Counter`

   **極性：**  兩者之一 `Up is Good` 或 `Up is Bad`

   **可見度：** `Visible Everywhere`

   **獨特事件記錄：** `Always Record Event`

   **參與率：** `Enabled`

   您不需要在品牌網站上實作新事件，因為它使用已擷取的現有資料。

1. 在中建立及驗證處理規則 [!DNL Analytics]：

   >[!NOTE]
   >
   >僅限 [!DNL Analytics] 帳戶管理員可以建立處理規則，除非他們已授予非管理員許可權。

   1. [建立處理規則](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)，使用下列設定：

      * 對於必須符合的條件，指定必要的 [!DNL eVars] 或 [!DNL props].

        您可以視需要設定其他詳細程度等級，以確保建立最精確的事件。

        >[!TIP]
        >
        >最佳實務是隻使用一個 [!DNL eVar] 或 [!DNL prop].

      * 針對動作，選取 **設定事件** 並選取預留位置事件。

   1. 在 [!DNL Analytics] [!DNL Analysis Workspace]， [建立專案](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) 並將新事件提取至自由表格，以確保資料已填入 [!DNL eVar] 或 [!DNL prop] 量度。

1. 請聯絡您的Adobe客戶團隊，以將新量度同步至Adobe Advertising。

量度可用後，您就可以用它來建立目標，然後將其指派給搜尋、社交和商務產品組合，或用作 [自訂目標](/help/dsp/optimization/custom-goal-about.md) 用於DSP套件。

如需有關建立目標的詳細資訊，請參閱「目標」的「最佳化指南」章節，此章節可從「搜尋」、「社交」和「商務」中取得。

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [檢視為廣告商追蹤的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
