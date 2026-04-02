---
title: 從Adobe Analytics [!DNL eVars] 和Prop建立轉換量度
description: 使用 [!DNL eVar]和 [!DNL prop]層級資料設定自訂成功事件量度。
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
TQID: https://experienceleague.adobe.com/DRwNcYJ4-tv6CWhaIHc-qZ-xNsM8sSqoSNkG8AaYI2c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2: id: cfd751d4-ee56-4323-8fd1-dc174b031709id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# 從Adobe Analytics [!DNL eVars]和[!DNL props]建立轉換量度

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

您可以使用成功事件量度，根據最符合您品牌目標的DSP網站資料來最佳化Adobe Analytics套件和搜尋、社交和Commerce行銷活動。 您可以將[[!DNL Analytics] [!DNL eVars]和](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)層級資料匯入事件，根據現有的[[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html)和[!DNL eVar][!DNL prop]設定自訂成功事件量度。 其他[!DNL Analytics]個量度（包括標準、自訂和保留的轉換量度及流量量度）可自動在DSP和Search、Social及Commerce中使用。

![使用範例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用範例")

下列大部分工作必須由[!DNL Analytics]系統管理員或其他使用者執行。 如果您需要協助，請聯絡您的Adobe客戶團隊。

1. 在[!DNL Analytics]中，[建立預留位置成功事件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event)。

   使用下列其他引數：

   **型別：** `Counter`

   **極性：** `Up is Good`或`Up is Bad`

   **可見度：** `Visible Everywhere`

   **不重複事件錄製：** `Always Record Event`

   **參與率：** `Enabled`

   您不需要在品牌網站上實作新事件，因為它使用已擷取的現有資料。

1. 在[!DNL Analytics]中建立及驗證處理規則：

   >[!NOTE]
   >
   >只有[!DNL Analytics]帳戶管理員可以建立處理規則，除非他們已授予非管理員許可權。

   1. [使用下列組態建立處理規則](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)：

      * 對於必須符合的條件，請指定必要的[!DNL eVars]或[!DNL props]。

        您可以視需要設定其他詳細程度等級，以確保建立最精確的事件。

        >[!TIP]
        >
        >最佳實務是隻使用一個[!DNL eVar]或[!DNL prop]。

      * 針對動作，選取&#x200B;**設定事件**&#x200B;並選取預留位置事件。

   1. 在[!DNL Analytics] [!DNL Analysis Workspace]中，[建立專案](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)並將新事件提取至自由表格，以確保資料已填入[!DNL eVar]或[!DNL prop]量度。

1. 請聯絡您的Adobe客戶團隊，以將新量度同步至Adobe Advertising。

量度可用後，您就可以用它來建立目標，然後將其指派給搜尋、社交和Commerce產品組合，或用作DSP套件的[自訂目標](/help/dsp/optimization/custom-goal.md)。

如需有關建立目標的詳細資訊，請參閱有關「目標」的「最佳化指南」章節，此章節可從「搜尋」、「社交」和「Commerce」中取得

>[!MORELIKETHIS]
>
>* Adobe Advertising中的[[!DNL Analytics] 資料](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [檢視為廣告商追蹤的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
