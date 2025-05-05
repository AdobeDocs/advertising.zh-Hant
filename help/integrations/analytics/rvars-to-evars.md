---
title: 收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics
description: 瞭解如何在Adobe Analytics中收集保留變數的歷史資料，以便將來在Adobe Customer Journey Analytics中使用
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: 5b78ec0fc4c5ea4742cbb080b992bdb323fc9af3
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# 收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics

*僅使用[!DNL Analytics for Advertising]和Adobe Customer Journey Analytics的廣告商*

如果您使用保留的變數來擷取[AMO ID和EF ID](ids.md)，以進行[!DNL Analytics for Advertising]整合，則您可以儘快將您保留的AMO ID和EF ID變數複製到[standard [!DNL eVars]](https://experienceleague.adobe.com/zh-hant/docs/analytics/components/dimensions/evar)，以準備未來的Adobe Advertising與Adobe新一代[!DNL analytics]解決方案[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-overview/cja-overview)之間的整合。 如此一來，當您完成工作時，便可立即收集AMO ID與EF ID的歷史資料。 如果您使用保留的變數且需要完成此工作，Adobe客戶團隊會通知您。

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## 為什麼需要收集Customer Journey Analytics的歷史資料？

Customer Journey Analytics可讓您將資料從Adobe Experience Platform同步至Adobe Analytics Analysis Workspace。 目前，傳至Experience Platform的[!DNL Analytics Data Connector]並未將保留變數的資料從[!DNL Analytics]傳送至Experience Platform。 因此，由保留變數擷取的AMO ID和EF ID資料，目前在Customer Journey Analytics中無法使用。 <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising正規劃未來的Customer Journey Analytics實作。 在發行實作後，您的[!DNL Analytics for Advertising]整合仍需要您使用[!DNL Analytics]追蹤來收集點進資料<!-- Add back if we implement this:  and (DSP users) view-through data -->，但如果您的組織同時擁有這兩個產品，則可以在1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) -->和2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)-->中檢視您的資料。 當功能發行時，Experience Platform將開始收集您AMO ID和EF ID的資料，以用於Customer Journey Analytics，但發行日期前的歷史資料將不存在。

不過，您可以透過建立簡單的[[!DNL Analytics] 處理規則](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)，將您的AMO ID和EF ID <!-- [!DNL rVars] -->立即複製到[!DNL eVars]，更早開始收集您AMO ID和EF ID <!-- [!DNL rVars] -->的資料。 建立處理規則後，您的AMO ID和EF ID <!-- [!DNL rVars] -->在追蹤新事件時就會開始累積資料。 實施完成後，歷史資料即可在Customer Journey Analytics中使用。

>[!NOTE]
>
>* 自2025年2月28日起，此程式會追蹤點進資料，但不會追蹤檢視資料。
>* 處理規則僅套用至收到的新資料。 他們無法回溯收集過去資料。

## 將您保留的AMO ID與EF ID變數複製到[!DNL eVars]

此步驟是手動的，且必須針對您預計未來要與Adobe Advertising整合之每個追蹤AMO ID和EF ID <!-- [!DNL rVars] -->的報表套裝完成。

1. [使用下列設定建立處理規則](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules)：

   * 選取您要將AMO ID和EF ID <!-- [!DNL rVar] -->資料移轉至Experience Platform以供Customer Journey Analytics使用的報表套裝。

   * 對於[!UICONTROL Rule Title]，請使用描述性名稱，例如「將AMO ID和EF ID複製到eVar」。

   * 在[!UICONTROL Always Execute]區段中，新增兩個動作以建立新的eVar：

      * 針對`AMO ID`：

         1. 選取&#x200B;**覆寫**&#x200B;的值。
         1. 選取&#x200B;*\&lt;新的/未使用的eVar\>*。
         1. 選取&#x200B;**查詢字串引數**。
         1. 輸入`s_kwcid`。

        範例： ```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * 針對`EF ID`：

         1. 選取&#x200B;**覆寫**&#x200B;的值。
         1. 選取&#x200B;*\&lt;新的/未使用的eVar\>*。
         1. 選取&#x200B;**查詢字串引數**。
         1. 輸入`ef_id`。

        範例： `Overwrite the value of rVar11 with Query String Parameter ef_id`

   * 對於[!UICONTROL Reason for rule]，請使用描述性備註，例如「將透過Adobe Analytics Connector將AMO ID和EF ID傳輸至AEP」。

1. 驗證儲存的處理規則。

   儲存處理規則後，`AMO ID`和`AMO EF ID` <!-- the existing reserved variables -->的資料應與其複製到的兩個新eVar的資料相同。

   例如，如果新eVar `eVar142`對應至`amo.s_kwcid(Context Data)`，則`eVar142`和`AMO ID`的資料應該相同。

如需有關如何套用處理規則的詳細資訊，請參閱[處理規則的運作方式](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
