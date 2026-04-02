---
title: Advertising DSP中的行銷活動管理概觀
description: 瞭解行銷活動管理階層和元件。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Advertising DSP中的行銷活動管理概觀

DSP行銷活動具有下列階層：

* Campaign
   * 封裝
      * 位置
         * 廣告
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[行銷活動](/help/dsp/campaign-management/campaigns/campaign-about.md)是航班設定的總體架構。 每個行銷活動都設定了廣告商、開始和結束日期、整體預算、跨裝置目標定位選項和預設頻率上限，以及可檢視度、詐騙、品牌安全和對象驗證的報告選項。 所有行銷活動層級設定會自動套用至行銷活動內的每個套件和位置。

## [!UICONTROL Packages]

每個行銷活動可以包含一個或多個[套件](/help/dsp/campaign-management/packages/package-about.md)，每個套件都包含一組版位。

使用套件將投放位置分組為設定預算、效能目標和自訂步調策略。 DSP將預算轉移到封裝中表現最好的位置，以最佳化封裝。 您可以依版位格式、詳細目錄型別、資料提供者、角色或其他可區別的特徵來組織套件。

套件是選用的，但建議使用。

## [!UICONTROL Placements]

[位置](/help/dsp/campaign-management/placements/placement-about.md)會儲存相同廣告型別的一或多個廣告的定位引數。 您可以建立單一行銷活動或套件的版位，然後為其指派廣告。

## [!UICONTROL Ads]

[廣告](/help/dsp/campaign-management/ads/ad-about.md)包含創意資產和追蹤URL。 您可以使用合作夥伴標籤頁或大量標籤範本，個別或大量上傳第三方廣告服務標籤。 您也可以手動建立原生顯示廣告供DSP提供。

設定廣告之後，您必須將每個廣告附加至位置，才能開始執行廣告。 您可以將單一廣告附加至一或多個位置。

在作用中行銷活動中，處於作用中行銷活動的所有作用中、已核准的廣告都符合根據版位鎖定目標引數執行的資格。

>[!MORELIKETHIS]
>
>* [關於Advertising DSP中的行銷活動管理](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [關於Advertising DSP中的封裝管理](/help/dsp/campaign-management/packages/package-about.md)
>* [關於Advertising DSP中的位置管理](/help/dsp/campaign-management/placements/placement-about.md)
>* [關於Advertising DSP中的廣告管理](/help/dsp/campaign-management/ads/ad-about.md)
>* [行銷活動啟動檢查清單](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [行銷活動管理檢視中的效能報告型別](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [管理您的行銷活動資料檢視](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [影片： DSP帳戶結構和使用者介面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
