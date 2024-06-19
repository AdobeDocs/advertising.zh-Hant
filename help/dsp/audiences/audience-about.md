---
title: 關於Advertising DSP中的對象管理
description: 瞭解對象管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 關於Advertising DSP中的對象管理

在DSP中，您可以建立和管理受眾區段和受眾集，並作為刊登版位的目標：

* 透過建立和實作DSP區段來收集您自己的第一方對象資料。 您稍後可以在區段中以廣告重新鎖定使用者，或避免區段中的使用者接收廣告。 您可以建立下列型別的區段：

   * [自訂區段](/help/dsp/audiences/custom-segment-create.md) 追蹤a)接觸到來自桌上型電腦和行動裝置廣告的使用者，以及b)造訪特定網頁的使用者。 追蹤標籤可以追蹤Cookie型使用者或與ID5通用ID相關聯的使用者。

   * [CCPA選擇退出銷售區段](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 若要根據加州消費者隱私法(CCPA)追蹤網站上消費者選擇退出銷售請求的使用者ID。 您每月可以從選擇退出銷售請求中擷取使用者ID的報表。

     如需有關CCPA選擇退出銷售請求的Adobe Advertising支援的詳細資訊，請參閱 [加州消費者隱私法的Adobe Advertising支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* （Beta功能） [取得通用ID並用於無cookie目標定位](/help/dsp/audiences/universal-ids.md)：

   * 手動傳送您的已驗證 [!DNL LiveRamp] [!DNL RampID] 區段直接傳送至DSP。

   * 允許DSP從您的客戶資料平台匯入第一方區段，並將其轉譯為支援的通用ID型別。

   * 將包含通用ID的第三方區段加入您的位置目標，無需執行任何額外步驟。

* 建立對象庫，對象為 [可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md). 已儲存的對象是由任何可用對象區段和任何其他已儲存的對象所組成。 您對已儲存對象所做的任何變更，都會自動套用至鎖定或排除對象的所有位置，以及包含已儲存對象的所有其他對象。

  儲存的對象可讓媒體規劃人員視需要將對象分組，方法是使用複雜的布林邏輯包含和排除多個區段。 當您建立對象時，會指出每個個別區段的大小以及對象總人數。 Campaign執行者隨後只需選取一或多個儲存的對象作為位置目標，而非手動設定每個位置的對象目標。

位置鎖定目標也可使用其他對象型別。

## 匯入第一方和第三方資料區段

您有許多選項可使用DSP使用者介面及/或透過自訂匯入服務，將第一方與第三方資料區段匯入DSP。

* DSP可提取您的Adobe Audience Manager和其他 [!DNL Adobe] 目標定位的對象。 如需必要條件和指示，請參閱&quot;[匯入Adobe Audience Manager區段以鎖定廣告](/help/integrations/audience-manager/import-audiences.md).

* DSP可使用將支援的客戶資料平台的第一方資料區段，轉換為具有通用ID的區段 [來源功能](/help/dsp/audiences/sources/source-about.md). 您也可以 [手動傳送您已驗證的郵件 [!DNL LiveRamp] [!DNL RampID] 直接將區段傳送至DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP可以直接從您的資料管理平台(DMP)匯入您的其他第一方資料區段，並視需要將其提供給任何一組廣告商。

* DSP可匯入自訂的第三方區段，包括第三方區段的複雜組合。 您可以視需要將這些區段提供給任何一組廣告商。

如需詳細資訊，請聯絡您的Adobe客戶團隊。

## 可作為放置目標的對象

您可以將位置鎖定在下列所有型別的對象中。

* 所有使用者建立且儲存在DSP中的對象集。

* 在DSP中建立的所有使用者建立受眾區段：

   * 造訪特定網頁的使用者與公開特定廣告曝光次數的使用者的自訂區段。

     對於傳遞到通用ID的曝光，不會產生任何費用。

   * CCPA根據加州消費者隱私法(CCPA)，對在您的網站上提交選擇退出銷售請求的使用者選擇退出銷售的對象區段。

* 所有匯入的第一方資料區段，包括轉換為通用ID的區段。

  若要取得為通用ID傳送的曝光數，則需支付額外費用。 請參閱&quot;[關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)」代表費率。

* 所有匯入的自訂第三方資料區段。

* （僅針對美國的位置） [30多家提供者的DSP客戶可使用的所有協力廠商資料區段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL eXelate]， ([!DNL Eyeota])，([!DNL LiveRamp])，[!DNL Lotame]， [!DNL Neustar]，以及更多功能。

  您可以鎖定特定區段，根據對象資料鎖定使用者（例如，具有特定人口統計資料、興趣或意圖和/或行為設定檔的使用者）。 您可以依資料提供者和類別瀏覽、依名稱或區段ID搜尋區段，或依資料提供者、區段大小總計、網頁瀏覽器計數或裝置計數篩選結果。

  協力廠商區段會產生額外費用，這些費用會顯示在每個區段名稱旁。

* (使用Adobe Experience Platform和的廣告商 [!DNL Real-Time CDP]、僅使用Adobe AdvertisingJavaScript轉換標籤的Adobe Audience Manager或Adobe Analytics)您在中建立的所有可用第一方、第二方或第三方受眾區段 [!DNL Real-Time CDP]，在Audience Manager中建立，或從Audience Manager發佈至Adobe Experience Cloud，或 [!DNL Analytics].

  使用區段的定價是預先議定的，在DSP中不可見。

  區段來源 [!DNL Analytics] 在建立或發佈為Experience Cloud對象後約一小時可使用。 直接來自Audience Manager或的區段 [!DNL Real-Time CDP] 共用後24小時內即可使用。

  >[!NOTE]
  >
  >請參閱以下檔案： [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)， [Analytics](https://experienceleague.adobe.com/docs/analytics.html)、和 [此 [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) 瞭解如何在這些解決方案中設定及收集區段的資料。

## 對象人數資料

在對象>所有對象和位置設定的對象鎖定目標區段中，您可以依大小範圍篩選每個區段清單，包括總範圍以及特定裝置型別或通用ID型別的個別範圍。

![依對象人數篩選](/help/dsp/assets/audience-size-filter.png)

您也可以檢視詳細的對象人數資料：

* 系統會顯示所有選定區段和已儲存對象的作用中重複資料刪除對象人數總計，且您可以依裝置型別（瀏覽器、行動或連線電視）檢視詳細資料。

  ![合併的對象人數](/help/dsp/assets/audience-size.png)

* 若為個別區段，總對象人數和CPM （若適用）會顯示在區段名稱旁。

  ![個別區段大小](/help/dsp/assets/audience-size-segment.png)

* 您可以檢視有關個別區段或儲存對象的詳細資訊，包括瀏覽器、行動裝置、連線電視和通用ID型別合作夥伴的大小。 對於儲存的對象，總大小是重複資料刪除總數。

  ![個別區段或儲存的對象詳細資料](/help/dsp/assets/audience-size-segment-details.png)

## 對象檢視

### 所有對象檢視

在 [!UICONTROL All Audiences] 檢視或對象庫，您可以儲存和管理可重複使用的對象，其中包括對象區段群組，甚至其他儲存的對象。 您可以使用受眾作為多個位置的目標。 版位名稱旁會顯示各對象所使用的版位數量。

您可以編輯、複製、刪除、匯出或共用任何對象。

### 區段檢視

在 [!UICONTROL Segments] 檢視，所有使用者都可以建立其他自訂區段。

此 [!UICONTROL Segments] 「檢視」也會列出下列區段型別：

* 所有使用者建立的自訂區段皆可供使用者使用。

  您可以檢視您建立的任何自訂區段的追蹤標籤，並和其他使用者共用這些區段。 您也可以編輯或刪除您建立的自訂區段。

  您無法編輯或共用其他使用者與您共用的自訂區段。

* 使用者可使用的所有第一方區段依原樣匯入。

  您無法編輯或共用與您共用的第一方區段。 如果您需要與其他使用者共用第一方區段，請聯絡您的Adobe客戶團隊。

* 所有可供使用者使用的自訂第三方區段。

  您無法編輯或共用與您共用的第三方區段。 如果您需要與其他使用者共用協力廠商區段，請聯絡您的Adobe客戶團隊。

### 來源檢視

在 [!UICONTROL Sources] 檢視，您可以在支援的客戶資料平台上設定第一方區段的來源，以將其轉換為包含指定通用ID型別的區段。 來源設定包括自動產生的來源金鑰，您會將其提供給客戶資料平台以建立連線。

如需關於支援的客戶資料平台、支援的通用ID型別以及設定每個客戶資料平台連線的工作流程的詳細資訊，請參閱&quot;[關於來源](/help/dsp/audiences/sources/source-about.md).」

翻譯後的區段可納入可重複使用的對象和無曲別目標定位的放置設定中。

>[!MORELIKETHIS]
>
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [建立及實作自訂區段](custom-segment-create.md)
>* [建立及實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](/help/dsp/audiences/sources/source-manage.md)
>* [手動匯入已驗證的區段，從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
