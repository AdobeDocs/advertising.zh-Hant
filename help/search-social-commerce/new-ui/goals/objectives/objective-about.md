---
title: （新UI）關於目標
description: 瞭解符合您業務目標的目標。
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# （新UI）關於目標

*Beta功能*

目標為廣告商為實現其業務目標而設定的目標，例如最大化利潤或達成特定銷售目標。 Advertising Search、Social和Commerce以及Advertising DSP都使用目標：

* 每個搜尋、社交和Commerce產品組合都必須有目標，以便最佳化功能可以為該產品組合建立點按和收入模型。

* 在DSP中，目標會顯示為連結至「搜尋」、「社交」和「Commerce」帳戶的DSP帳戶的自訂目標。 每個使用最佳化目標「最高廣告投資報酬率(ROAS)」或「最低每次收購成本(CPA)」的套件都必須包含可協助達成整體最佳化目標的自訂目標。

目標包含要追蹤和最佳化的轉換量度，以及這些量度的相對權重。 例如，假設一個線上雜誌有兩個線上訂閱層級和一個列印訂閱層級，並且目標「利潤最大化」有三個量度：價值20美元的「基本線上訂閱」、價值40美元的「進階線上訂閱」和價值30美元的「列印訂閱」。 如果雜誌想要根據訂閱的一次性貨幣值給予權重，則量度的相對權重將分別為1、2和1.5。

對於目標中的每個量度，您可以：

* 為來自行動裝置的轉換設定個別權重。

* 將度量標示為[!UICONTROL Goal]度量或[!UICONTROL Assist]度量。

* 將權重建議套用至量度。

>[!NOTE]
>* (搜尋、社交和Commerce)當您[建立投資組合](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md)或稍後[修改投資組合設定](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md)時，您可以將目標與投資組合建立關聯。
>* (具有連結至Search、Social和Commerce帳戶的DSP帳戶的廣告商)在Advertising DSP中，您可以選取目標作為[自訂最佳化目標](/help/dsp/campaign-management/packages/package-settings.md)，以用於具有套件層級步調的套件。
>* 您可以對多個搜尋、社交和Commerce產品組合及/或多個DSP套件使用相同的目標。
>* [!UICONTROL Objectives]檢視中每個目標的量度不包含DSP的資料。

## 可用量度

您可以在目標中包含下列任一專案：

* Adobe Advertising使用[Adobe Advertising轉換追蹤畫素](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)追蹤的量度。

* [來自轉換摘要檔案的廣告商追蹤量度](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* （具有[!DNL Adobe Analytics for Advertising]的廣告商） [從Adobe Analytics](/help/integrations/analytics/overview.md)同步的轉換和網站參與量度。

  在搜尋、社交和Commerce中，下列[網站參與量度](/help/integrations/analytics/analytics-data-in-advertising.md)會自動納入投資組合競標演演算法中： `timespent_secs_1stvisit`、`timespent_secs_total`、`pageviews_1stvisit`、`pageviews_total`和`bounces`。

* [!DNL Google]個量度：<!-- Search only, or might DSP-only clients also have these? -->

   * 已從同步的[[!DNL Google Ads]帳戶追蹤](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)個轉換[!DNL Google Ads]。

   * （具有[[!DNL Google Analytics] 整合](/help/search-social-commerce/admin/data-sources/data-source-about.md)的廣告商）頁面檢視、工作階段、跳出率（以跳出數/工作階段數計算）和工作階段持續時間。

     在搜尋、社交和Commerce中，這些量度會自動納入投資組合競標演演算法中。

## 上傳目標至廣告網路的選項

您可以選擇將帳戶產品組合的目標[上傳至 [!DNL Google Ads] 和/或 [!DNL Microsoft Advertising] 作為轉換](/help/search-social-commerce/tools/objective-upload-to-networks.md)，以便將其用於行銷活動或廣告群組最佳化。 啟用選項後，Search、Social和Commerce會每天將EF ID （按一下ID）層級的加權收入資料傳遞至廣告網路。 它會忽略任何廣告網路追蹤量度。

>[!MORELIKETHIS]
>
>* [建立目標](objective-create.md)
>* [編輯目標](objective-edit.md)
>* [刪除目標](objective-delete.md)
>* [將加權建議套用至目標](objective-apply-weight-recommendations.md)
>* [目標設定](objective-settings.md)
