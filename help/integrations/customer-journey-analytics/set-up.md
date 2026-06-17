---
title: 設定資料收集、資料傳輸及報告
description: 瞭解如何設定資料收集、資料傳輸和報告。
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a93c33ee47bd1a8df137a69598b367e985def4ee
workflow-type: tm+mt
source-wordcount: 1802
ht-degree: 0%

---

# 設定資料收集、資料傳輸及報告

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

*僅不含[!DNL Analytics for Advertising]的廣告商*

使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)在Adobe Advertising和Customer Journey Analytics之間以原生方式交換資料時，需要執行下列工作。 資料傳輸和歸因在啟動後開始，不包含歷史資料。

具有[!DNL Analytics for Advertising]的廣告商不需要這些工作。

1. （您組織的Adobe Experience Platform網站管理員） [在Experience Platform中設定資料收集並實作轉換追蹤標籤](#data-collection)。

1. （您組織的Customer Journey Analytics網站管理員） [在Customer Journey Analytics中建立與Experience Platform資料集的連線](#dataset-connection)。

1. （您組織的網頁分析人員） [在Customer Journey Analytics中設定資料檢視](#cja-data-views)。

1. （您組織的網頁分析人員） [在Customer Journey Analytics Workspace中設定報告和視覺效果](#cja-reports)。

以下小節包含詳細的程式，其中包括整合所需的任務和設定，但並未說明工作流程中可用的所有功能。 如需完整資訊，請參閱連結的資源。

## 在Adobe Experience Platform中和您的網站上設定資料收集 {#data-collection}

若要在Experience Platform中設定資料收集並實作轉換追蹤標籤，必須執行下列工作。 您組織的Experience Platform網站管理員可以執行這些工作，但您組織的IT部門可能需要協助部署追蹤標籤。

### 收集資料並從Adobe Advertising傳送至Experience Platform Edge Network作為資料集

此程式包括建立綱要。 您可以選擇編輯現有結構描述；在這種情況下，您不需要建立資料集或資料流。

1. 在Experience Platform中，[為您要使用體驗資料模型(XDM)收集的資料定義手動結構描述](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/ui/resources/schemas)。

   * 在[!UICONTROL Schema Details]中，選取&#x200B;**[!UICONTROL Experience Event]**&#x200B;作為要擷取網站事件的結構描述的基底類別。 為結構描述命名，然後按一下&#x200B;**[!UICONTROL Finish]**。

   * 在左側面板中，新增欄位群組[Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)，以新增Adobe Advertising的特定欄位。 至少要包含conversionDetails物件，該物件具有`trackingCode`和`trackingIdentities`屬性，其中包括[AMO ID和EF ID](ids.md)。 其他欄位為選用欄位。 不需要其他設定。

   * （選用）視需要新增其他欄位群組，將其他資料欄位連線至Adobe Advertising資料。

   **注意：**&#x200B;您可以建立多個結構描述，但每個資料集和資料流只能使用一個結構描述，您將在以下步驟中建立該結構描述。

1. [根據結構描述建立資料集](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/create)以儲存和管理事件資料的集合。 這將是您的&#x200B;*事件資料集*。 如果您使用資料集編輯現有結構描述，則可以跳過此步驟。

   * 選擇&#x200B;**[!UICONTROL Create dataset from schema]**&#x200B;的選項並選取您的結構描述。

     Adobe Advertising會根據您的事件資料集建立兩個額外的資料集： 1\)包含相關摘要資料（例如彙總點按次數和彙總曝光數）的&#x200B;*摘要資料集*&#x200B;以及2\) *查詢資料集* （包含維度/分類中繼資料，例如Adobe Advertising促銷活動名稱）。 資料集的資料會每天在Experience Platform中填入。

   >[!TIP]
   >
   >先建立虛擬事件資料集，在使用生產資料集之前驗證資料流程。

1. [建立資料串流](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/datastreams/configure)，以指定從網站或應用程式傳送資料的位置，以及如何處理傳入的資料。

   * 針對[!UICONTROL Mapping schema]設定，選取您的結構描述。

   * 將服務`Adobe Advertising`和`Adobe Experience Platform`新增並啟用至資料流。

     [!UICONTROL Adobe Advertising]服務可讓廣告曝光與裝載相關聯，且[!UICONTROL Adobe Experience Platform]可讓Edge Network儲存資料集並將其路由至Adobe Advertising。

   * 針對[!UICONTROL Event dataset]設定，選取您的事件資料集。

     每個資料流只能將資料插入一個資料集。

### 將貴組織的網站資料傳送至您的Experience Platform資料流

在Adobe Experience Platform Tags中使用Adobe Web SDK擴充功能，將您組織的網站資料傳送至您的Experience Platform資料流。

>[!NOTE]
>
>僅支援Adobe標籤。 不支援獨立Experience Platform Web SDK (`alloy.js`)或協力廠商標籤管理員。

1. 使用Experience Platform [標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/home) （先前稱為[!DNL Launch]）來產生JavaScript標籤，以將您組織的網站資料傳送至資料流。

   * 建立標籤屬性，這是標籤設定的容器。

   * 針對您的屬性，請從擴充功能目錄[安裝「Adobe Experience Platform Web SDK」擴充功能](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)。

     此擴充功能會透過Experience Platform Edge Network，將資料從您的Web屬性傳送至Adobe CX Enterprise。

     請勿使用Adobe Advertising擴充功能。

   * 建立[自訂Web SDK組建](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build)：

      * 在[!UICONTROL Custom build components]區段中，啟用&#x200B;**Advertising**&#x200B;元件。

        此元件包含標籤中Adobe Advertising所需的所有JavaScript程式碼，Advertising DSP和Advertising Search、Social及Commerce客戶都需要此元件。 元件也會在標籤規則（選填）中新增「Advertising」設定，以定義如何將廣告資料用於歸因測量。

        您可以視需要選擇啟用其他元件。

      * 在[!UICONTROL SDK Instances]區段中：

         * 在[!UICONTROL Datastreams]設定中，選取要用於各個Web環境（生產、測試、開發）的資料流。

         * （僅限具有Adobe Advertising DSP的組織）在[[!UICONTROL Adobe Advertising]設定](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)中，啟用&#x200B;**[!UICONTROL Adobe Advertising DSP]**&#x200B;以允許檢視追蹤，並指定要啟用檢視追蹤的廣告商。 您可以新增組織的ID5合作夥伴ID及/或組織[!DNL LiveRamp RampID] JavaScript程式碼(ats.js)的路徑，選擇從通用ID收集ID。

           如果您的廣告商未列出，請輸入每個廣告商的廣告商ID。 如有需要，請向您的Adobe帳戶團隊索取ID。

           [!DNL RampID] JavaScript路徑的範例： `https://launchpad-wrapper.privacymanager.io/<customer-specific-id>/launchpad-liveramp.js`

         * 儲存組建。

   * （選用） [視需要建立規則](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/ui/rules)，以決定Web SDK何時應將資料傳送至Edge Network。

      * 對於`[sendEvent](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`動作，請使用[[!UICONTROL Advertising]設定](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising)來定義如何將廣告資料用於歸因測量。 當規則包含一系列多個動作時，此設定很有幫助，而且僅當您為自訂組建元件選取&quot;[!UICONTROL Advertising]&quot;元件時可用。

   * 視需要建立[資料元素](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/ui/data-elements)，以將網站上的變數對應到您先前建立的XDM結構描述結構。

1. [將標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/publish/publishing-flow)發佈到測試環境，您可以在其中反複開發標籤。

1. [檢查您三個資料集的活動](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/user-guide#view-datasets)以驗證傳遞。

1. [將標籤發佈至您的即時生產環境](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/publish/publishing-flow)。

   您組織的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

## 在Customer Journey Analytics中建立與Experience Platform資料集的連線 {#dataset-connection}

請依照下列步驟，將Adobe Advertising資料從您的Experience Platform資料集提取到Customer Journey Analytics中。 您組織的Customer Journey Analytics網站管理員可以執行這些工作。

您也可以選擇編輯具有相同資訊的現有連線。

1. 在Customer Journey Analytics中，[建立或編輯連線](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-connections/create-connection)，其中包含您的Experience Platform資料集和結構描述。

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * 確認已選取正確的沙箱。

   * 計算每日事件平均數量（大多陣列織不足100萬）。

   * 新增您的Experience Platform事件量度資料集（型別： `Event`）、您的<!-- Adobe Advertising -->事件摘要量度資料集（型別： `Event`）以及<!-- Adobe Advertising -->維度（分類/中繼資料）資料集（型別： `Lookup`）。

     您的團隊已建立事件資料集，而Adobe Advertising已根據您的事件資料集建立摘要和維度資料集。

     您可以視需要選擇加入其他資料集。

   * 設定資料集設定：

      * 針對[!UICONTROL Event Dataset]設定：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]：**&#x200B;啟用設定

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]：**&#x200B;啟用設定

      * 針對[!UICONTROL Lookup Dataset]設定，將維度資料集對應至事件資料集：

         * **[!UICONTROL Key]** （要當作維度資料集索引鍵使用的欄位）： `Tracking Code` （與結構描述中的`trackingCode`欄位相同）。

         * **[!UICONTROL Matching key]** （做為事件資料集比對索引鍵的欄位）： `Tracking Code (Event datasets)`。

         * **[!UICONTROL Import all new data]：**&#x200B;啟用設定

      * 針對[!UICONTROL Metrics Dataset]設定：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]：**&#x200B;確認值

         * **[!UICONTROL Import all new data]：**&#x200B;啟用設定

2. 在三小時內，確認資料可在Customer Journey Analytics中使用。

   1. 在Customer Journey Analytics中，前往&#x200B;**[!UICONTROL Connections]**&#x200B;並選取您的連線。

   2. 在顯示的資料集清單中，確認&quot;[!UICONTROL Number of Records]&quot;報表顯示資料已新增。

## 在Customer Journey Analytics中設定資料檢視 {#cja-data-views}

在Customer Journey Analytics中，建立一或多個資料檢視以定義用於報告的量度和維度。 網頁分析人員可以執行這些工作。

1. 在Customer Journey Analytics中，[建立資料檢視](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 設定檢視以包含下列資訊。

   * 如果您有Adobe Analytics帳戶，請在[!UICONTROL Configure]索引標籤的[!UICONTROL Calendar]區段中，使用您[!DNL Analytics]帳戶的[!UICONTROL Time Zone]。

   * 在[!UICONTROL Components]索引標籤上：

      * 新增查詢資料集（包含維度/分類資料）、事件資料集（包含事件層級資料）和摘要資料集（包含其他量度，例如點按次數）。

      * 從事件資料集和查詢資料集中選取要納入資料檢視的量度。

      * 搜尋「[!UICONTROL Tracking Code]」（屬於結構描述路徑為`_experience.adcloud.conversionDetails.trackingCode`的事件資料集的一部分）。<!-- and do what with it? Add it? Or is that what you --> 將&#x200B;**[!UICONTROL Persistence]**&#x200B;設為&#x200B;*[!UICONTROL Most Recent]*。

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## 在Customer Journey Analytics Workspace中設定報表和視覺效果 {#cja-reports}

在Customer Journey Analytics Workspace中，請依照下列步驟設定報表和視覺效果。 網頁分析人員可以執行這些工作。

1. [在Workspace中建立專案](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)，以根據資料檢視內設定的維度和量度來建置報表和視覺效果。

您可以在一個自由表格中使用相同維度，將摘要量度和事件資料分類。

1. （如果您有來自[!DNL Google Ads]或[!DNL Microsoft Advertising]的資料）使用廣告網路特定量度的欄位（已分組為`googleConversions`和`microsoftConversions`），建立發佈者追蹤的轉換報告。

>[!TIP]
>
>摘要事件通常會為報表新增少量的額外資料，例如一些額外事件、每天一個額外的工作階段或每個報表一個額外的人員。相較於標準網路事件，這些新增專案微不足道。不過，您可以排除虛擬人員ID `00000000-0000-0000-0000-000000000000`的資料，以篩選出此額外的摘要事件資料。
>![使用人員ID排除資料的範例](/help/integrations/assets/cja-report-with-person-id.png "使用人員ID排除資料的範例")

![您的資料集在Customer Journey Analytics中會如何顯示](/help/integrations/assets/cja-report-example.png "您的資料集在Customer Journey Analytics中會如何顯示")

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* [必要條件](prerequisites.md)
>* [由 [!DNL Customer Journey Analytics]](ids.md)使用的Adobe Advertising ID
>* Customer Journey Analytics中的[Adobe Advertising量度和維度](advertising-data-in-cja.md)
>* [收集AMO ID與EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
>* [疑難排解](troubleshooting.md)
>* [Customer Journey Analytics指南](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-landing)
>* Adobe Analytics使用者的Customer Journey Analytics [使用手冊](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
