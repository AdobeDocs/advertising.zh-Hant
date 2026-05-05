---
title: 在DSP中管理廣告商的轉換量度。
description: 瞭解如何將Adobe Advertising追蹤的轉換量度用於DSP廣告商。
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 管理廣告商的轉換量度

廣告商的轉換量度會在整個Adobe Advertising中使用：

* 在Advertising DSP中，您可以在行銷活動管理檢視、自訂目標和自訂報表中包含轉換量度。 您也可以使用廣告商的轉換量度來建立[自訂目標](/help/dsp/admin/custom-objectives-manage.md)，這些目標可用來最佳化封裝。

* （具有Advertising搜尋、Social和Commerce的廣告商）在「搜尋」、「社交」和「Commerce」中，轉換量度的資料可顯示在行銷活動、產品組合和目標管理檢視及報表中的欄中。 具有足夠存取許可權的使用者也可以使用轉換量度來建立目標，這些目標是用來最佳化產品組合。

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

為DSP使用者追蹤的量度型別包括：

* Adobe Advertising追蹤廣告商的轉換量度。

* [從Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md)同步的轉換和網站參與量度。

* [網站事件已從Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md)同步。

* 來自自訂摘要的轉換。

從可用的轉換量度清單中，有權存取廣告商資料的每位使用者都可以自訂他們看到的可用於管理檢視和報表的量度，包括或省略他們選擇的特定量度。 您可以使用與擷取資料中拼字完全相同的量度名稱，或是變更欄標題中所顯示的名稱，以提高可讀性。

>[!IMPORTANT]
>
>依預設，廣告商的轉換量度無法納入行銷活動管理檢視、自訂目標和自訂報告中。 若要讓轉換量度可供使用，您必須明確提供該量度。

>[!TIP]
>
>當廣告商（或廣告網路）停止收集轉換量度後，[在管理檢視和報告中隱藏它](#conversion-metrics-change-available)，除非您想要用它來檢視歷史資料。

## 檢視為廣告商追蹤的轉換量度

* 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**。

會列出為廣告商收集的所有轉換量度，以及指派給他們的任何不同顯示名稱。 每個量度列都包含量度的來源。

## 變更轉換量度的顯示名稱

例如，如果您使用名為&#x200B;*reg*&#x200B;的轉換量度來收集註冊資料，那麼您可以選擇變更顯示名稱，使其顯示為「註冊」。

您無法刪除現有的顯示名稱。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**。

1. 將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL Edit Display Name]**。

1. 輸入應顯示的名稱，然後按一下&#x200B;**[!UICONTROL Save]**。

   顯示名稱必須是唯一的，而且不能包括下列特殊字元： `\"<'>&`

## 變更行銷活動管理檢視、自訂目標和自訂報表中可用的轉換量度 {#change-the-conversion-metrics-available-in-ui}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions]**。

   已針對廣告商收集的所有轉換量度，以及已針對顯示指定的任何不同名稱都會列示。

1. （選用）篩選清單：

   1. 在清單上方，按一下![篩選器](/help/dsp/assets/filter.png "篩選器")。

   1. 指定篩選器，然後按一下&#x200B;**[!DNL Apply]**。

      您可以依AMO使用者端ID、量度在UI中是否可見或隱藏，以及資料來源來篩選量度。

1. 變更管理檢視和報告可用的轉換量度：

   * 若要顯示量度，請將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL Show in UI and Reports]**。

   * 若要隱藏量度，請將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL Hide in UI and Reports]**。

>[!MORELIKETHIS]
>
>* [管理您的行銷活動資料檢視](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [管理自訂目標](/help/dsp/admin/custom-objectives-manage.md)
