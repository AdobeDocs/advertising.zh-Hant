---
title: 使用案例
description: 瞭解與Audience Manager共用您的Advertising DSP媒體資料的使用案例
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 在Adobe Audience Manager中擷取媒體曝光資料的使用案例

*僅使用Advertising DSP的廣告商*

*僅整合Adobe Advertising-Adobe Audience Manager的廣告商*

以下是一些讓您從Audience Manager中擷取Advertising DSP媒體曝光度資料<!-- ad impression data? -->中獲益的方法。

## 使用間隔和頻率管理

擷取Audience Manager中的曝光資料，可讓您建立已接觸到特定廣告或行銷活動的使用者區段，藉此增強頻率管理。 如果您想要提高頻率，可以將這些區段用於廣告目標定位，或者如果您想要限制頻率，則將其用於廣告隱藏。

此外，透過Audience Manager[!DNL Segment Builder]，您可以將[造訪間隔和頻率控制項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html)套用至任何包含可操作訊號的[規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)。 舉例來說，這可讓您限制使用者在媒體促銷活動中展示特定創意內容的次數。 閱讀「[即時跨裝置隱藏](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)」以瞭解如何執行此動作。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 順序訊息

透過擷取曝光資料，您可以建立已曝光於促銷活動或廣告的使用者區段，並使用此區段進行循序傳訊或隱藏。 例如，您可以顯示創意內容`456`，重新鎖定看到創意內容`123`但未點按或轉換的使用者。

若要以Audience Manager執行此範例，請依照下列步驟執行：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 建立特徵來擷取看過該創意的使用者。

   例如，若要為特徵命名`Creative Trait 123`，請使用下列特徵規則：

   ```
   d_creative == 123 AND d_event == imp
   ```

1. 建立特徵來擷取按一下或轉換的使用者。

   例如，若要命名此特徵`Click and Converter`，請使用下列特徵規則：

   ```
   d_event == click OR d_event=conv
   ```

1. 建立名為`Retarget Users`的區段，以填入看到創意`123`但未點按或轉換的使用者。 使用以下特徵規則：

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. 將區段`Retarget Users`對應到目的地，並以創意專案`456`定位目的地中的使用者。

## [!DNL Adobe Audience Analytics]和行銷活動曝光資料

一旦行銷活動的曝光次數和點選次數資料可用於Audience Manager，您就可以建立接觸到或互動特定行銷活動或策略的使用者特徵和區段。 透過[[!DNL Audience Analytics] 整合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，您的Audience Manager區段可以與[!DNL Analytics]同步以供進一步分析。 潛在的使用案例包括：

* **DSP與[!DNL Advertising Search, Social, & Commerce]廣告之間的互動分析：**&#x200B;標準[[!DNL Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)未提供有關DSP與[!DNL Search, Social, & Commerce]之間互動的深入分析，因為兩個管道使用的AMO ID都遵循AMO ID歸因規則，搜尋點按會覆寫顯示檢視。 藉由在Audience Manager中建立DSP曝光度區段，您可以使用[!DNL Audience Analytics]來分析[!DNL Analytics]中DSP與[!DNL Search, Social, & Commerce]個廣告之間的互動。

* **頻率分析：**&#x200B;您可以根據使用者接觸到特定廣告或行銷活動的次數，在Audience Manager中建立區段。 接著，您可以分析Analytics中的不同曝光區段，瞭解使用者行為如何隨著DSP曝光次數而改變。

## [!DNL Audience Optimization Reports]

您可以運用[Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html)，找出行銷活動中區段的潛在績效機會。 這些報表結合行銷活動曝光次數、點按次數和轉換資料與區段量度，以提供以區段為中心的最佳化和有效的管道組合。

### 相關Audience Optimization報表的型別

| 報告 | 說明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance]報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 依曝光次數和轉換率比較對應和未對應的區段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis]報告]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 針對廣泛的廣告維度，傳回曝光數、點進率和轉換率等資料。 |
| [[!UICONTROL Optimal Frequency]報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 協助您在提供的曝光次數和轉換次數之間取得最佳平衡。 它可讓您在開始看到遞減的傳回之前，先調整要顯示的曝光數。 |
| [[!UICONTROL Unique User Reach]報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 泡泡圖，其中每個泡泡的大小均與所選維度的不重複使用者人數成正比。 |

### 考量事項

* 如果[!DNL Audience Optimization Reports]使用者具有角色型存取控制(RBAC)，則[!DNL Adobe Customer Care]必須設定廣告商ID與組織的Audience Manager資料來源整合代碼之間的對應。 然後，管理員使用者可以向不同的使用者提供RBAC許可權。

* [!DNL Audience Optimization Reports]中的轉換報表需要一般使用者進行一些設定。 使用者必須填入中繼資料檔案。

* [!DNL Audience Optimization Reports]不支援變更行銷活動中繼資料（例如行銷活動名稱或位置名稱）。

* 搜尋廣告的點選數只有在和曝光數相關聯時才包含在[!DNL Audience Optimization Reports]中。 換言之，搜尋點按會被視為閱聽後的轉換。 因此，許多搜尋點按可能不會包含在[!DNL Audience Optimization Reports]中。

>[!MORELIKETHIS]
>
>* [傳送DSP媒體曝光資料給Adobe Audience Manager的總覽](overview.md)
>* [收集來自Advertising DSP行銷活動的點按和曝光資料](collect.md)
