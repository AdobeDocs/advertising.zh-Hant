---
title: 設定資料收集、資料傳輸及報告
description: 瞭解如何設定資料收集、資料傳輸和報告。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 222f04c9e3c6e8af2ad7dbabcba234008dd14606
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 0%

---

# 設定資料收集、資料傳輸及報告

*Beta功能*

在Customer Journey Analytics中檢視Advertising Cloud資料需要下列工作。

1. （您組織的網頁分析人員；選擇性） [收集AMO ID和EF ID的歷史資料](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}。

   此步驟僅適用於具有[!DNL Analytics for Advertising]的廣告商。

1. (您組織的Adobe Experience Platform網站管理員) [在Experience Platform中設定資料收集並實作轉換追蹤標籤](#data-collection)。

1. (您組織的Customer Journey Analytics網站管理員) [在Customer Journey Analytics中建立與Experience Platform資料集的連線](#dataset-connection)。

1. （您組織的網頁分析人員） [在Customer Journey Analytics中設定資料檢視](#cja-data-views)。

1. （您組織的網頁分析人員） [在Customer Journey Analytics Workspace中設定報告和視覺效果](#cja-reports)。

以下小節包含詳細的程式，其中包括整合所需的任務和設定，但並未說明工作流程中可用的所有功能。 如需完整資訊，請參閱連結的資源。

## 在Adobe Experience Platform中和您的網站上設定資料收集 {#data-collection}

若要在Experience Platform中設定資料收集並實作轉換追蹤標籤，必須執行下列工作。 您組織的Experience Platform網站管理員可以執行這些工作，但您組織的IT部門可能需要協助部署追蹤標籤。

### 收集資料並從Adobe Advertising傳送至Experience Platform Edge Network作為資料集

1. 在Experience Platform中，[為您要使用體驗資料模型(XDM)收集的資料定義手動結構描述](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/ui/resources/schemas)。

   * 在[!UICONTROL Schema Details]中，選取&#x200B;**[!UICONTROL Experience Event]**&#x200B;作為要擷取網站事件的結構描述的基底類別。 為結構描述命名，然後按一下&#x200B;**[!UICONTROL Finish]**。

   * 在左側面板中，新增欄位群組`Adobe Advertising Cloud ExperienceEvent Full Extension`以新增Adobe Advertising的特定欄位。<!-- Add link once published -->至少包含具有`trackingCode`和`trackingIdentities`屬性的conversionDetails物件，這些屬性包含[AMO ID和EF ID](ids.md)。 其他欄位為選用欄位。

   * （選用）視需要新增其他欄位群組，將其他資料欄位連線至Adobe Advertising資料。

   **注意：**&#x200B;您可以建立多個結構描述，但每個資料集和資料流只能使用一個結構描述，您將在以下步驟中建立該結構描述。

1. [根據結構描述建立資料集](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/create)以儲存和管理事件資料的集合。

   * 選擇&#x200B;**[!UICONTROL Create dataset from schema]**&#x200B;的選項並選取您的結構描述。

     Adobe Advertising會根據您的事件資料集，為相關的摘要量度資料（例如轉換值）和查詢資料(維度/分類中繼資料，例如Adobe Advertising促銷活動名稱)建立其他資料集。 資料集的資料會每天在Experience Platform中填入。

1. [為結構描述建立資料流](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/datastreams/configure)。

   * 針對[!UICONTROL Mapping schema]設定，選取您的結構描述。

   * 將服務`Adobe Advertising`和`Adobe Experience Platform`新增並啟用至資料流。

     這些服務可讓Edge Network儲存資料集，並將其路由至Adobe Advertising。

   * 針對[!UICONTROL Event dataset]設定，選取您的資料集。

     每個資料流只能將資料插入一個資料集。

### 將貴組織的網站資料傳送至您的Experience Platform資料流

1. 使用Experience Platform [標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/home) （先前稱為[!DNL Launch]）來產生JavaScript標籤，以將您組織的網站資料傳送至資料流。

   * 建立標籤屬性，這是標籤設定的容器。

   * 針對您的屬性，請從擴充功能目錄[安裝「Adobe Experience Platform Web SDK」擴充功能](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)。

     此擴充功能會透過Experience Platform Edge Network，將資料從您的Web屬性傳送至Experience Cloud。

     請勿使用Adobe Advertising擴充功能。

   * 建立[自訂Web SDK組建](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build)：

      * 在[!UICONTROL Custom build components]區段中，啟用&#x200B;**Advertising**&#x200B;元件。

        此元件在標籤中包含Adobe Advertising所需的所有JavaScript程式碼。 它也會在標籤規則中新增「Advertising」設定（選用），以定義如何將廣告資料用於歸因測量。

        您可以視需要選擇啟用其他元件。

      * 在[!UICONTROL SDK Instances]區段中：

         * 在[!UICONTROL Datastreams]設定中，選取要用於各個Web環境（生產、測試、開發）的資料流。

         * (僅具有Adobe Advertising DSP的組織)在[!UICONTROL Adobe Advertising]設定中：

            * 啟用&#x200B;**[!UICONTROL Adobe Advertising DSP]**&#x200B;設定以啟用瀏覽追蹤。

            * 指定要啟用閱覽追蹤的廣告商。

            * （選用）輸入您組織的ID5合作夥伴ID以收集ID。

            * （選用）輸入貴組織[!DNL LiveRamp RampID] JavaScript程式碼(ats.js)的路徑，以收集ID。

         * 儲存組建。

   * （選用） [視需要建立規則](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/ui/rules)，以決定Web SDK何時應將資料傳送至Edge Network。

      * 對於`[sendEvent](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/action-types#send-event)`動作，請使用[!UICONTROL Advertising]設定來定義如何將廣告資料用於歸因測量。 當規則包含一系列多個動作時，此設定很有幫助，而且僅當您為自訂組建元件選取&quot;[!UICONTROL Advertising]&quot;元件時可用。 選項包括：

        *自動：*&#x200B;允許使用廣告資料來根據快取中的資料測量目前`sendEvent`動作的廣告歸因。 在此情況下，廣告曝光事件會在機率時引發，而且可能無法用於目前事件。 例如，如果您引發購買結帳事件，但快取中沒有可用的廣告曝光資料，則結帳事件不會歸因於廣告曝光。

        *等待：*&#x200B;延遲呼叫的執行直到成功從伺服器擷取廣告資料並解析為止，以確保精確的歸因測量。 例如，您可能想要等待廣告曝光事件解決後再引發購買結帳事件。 **注意：**&#x200B;根據瀏覽器和ID型別，解析ID可能需要幾秒鐘的時間。 如果目前的`sendEvent`動作可以容納數秒的延遲，請使用此選項。

        *已停用：* （預設值）從您正在觸發的要求中排除廣告資料，使其無法用於歸因或相關追蹤。

        *提供資料元素：*&#x200B;使用資料元素在頁面載入期間包含或排除廣告資料。 資料元素的解析值可以包含`automatic`、`wait`和`disabled`。 請參閱下一步。

     如果您未使用規則來設定`sendEvent`動作，則廣告資料會以個別廣告擴充事件的形式傳送。

   * 視需要建立[資料元素](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/ui/data-elements)，以將網站上的變數對應到您先前建立的XDM結構描述結構。

1. [將標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/publish/publishing-flow)發佈到測試環境，您可以在其中反複開發標籤。

1. 驗證資料集的傳遞，然後[將標籤發佈到您的即時生產環境](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/publish/publishing-flow)。

   您組織的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

## 在Customer Journey Analytics中建立與Experience Platform資料集的連線 {#dataset-connection}

請依照下列步驟，將Adobe Advertising資料從您的Experience Platform資料集提取到Customer Journey Analytics中。 您組織的Customer Journey Analytics網站管理員可以執行這些工作。

1. 在Customer Journey Analytics中，[建立連線](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-connections/create-connection)，其中包含您的Experience Platform資料集和結構描述。

   **注意：**&#x200B;目前，您必須將所有DSP與Search、Social與Commerce帳戶的資料傳送至單一Experience Platform執行個體與沙箱。

   * 新增您的Experience Platform事件（量度）資料集、摘要（量度）資料集和維度（分類/中繼資料）資料集。

     您的團隊已建立事件資料集，而Adobe Advertising已根據您的事件資料集建立摘要和維度資料集。

     您可以視需要選擇加入其他資料集。

   * 將維度資料集對應至事件資料集：

      1. 開啟維度資料集的設定。

         設定頁面上的標題是&quot;[!UICONTROL Lookup Dataset]&quot;，這表示您可以將維度資料集與其中一個量度特定資料集聯結。

      1. 在[!UICONTROL Adobe Advertising Dimensions]區段中，將維度資料集對應至事件資料集：

         1. 針對[!UICONTROL Key]欄位，選取要做為維度資料集索引鍵的欄位： `Adobe Advertising ID` （與結構描述中的`trackingCode`欄位相同）。

         1. 針對[!UICONTROL Matching key]欄位，選取要做為事件資料集比對索引鍵的欄位。 可用欄位名稱包含以括弧括住的資料集名稱。 例如，如果您要將維度資料集對應至事件資料集，請選取`Tracking Code (Event datasets)`。

         稍後當您設定資料檢視時，也會將事件資料集對應至摘要資#cja-data-views集。

1. 數小時後，確認資料可在Customer Journey Analytics中使用。

   1. 在Customer Journey Analytics中，前往&#x200B;**[!UICONTROL Connections]**&#x200B;並選取您的連線。

   1. 在顯示的資料集清單中，確認&quot;[!UICONTROL Number of Records]&quot;報表顯示資料已新增。

## 在Customer Journey Analytics中設定資料檢視 {#cja-data-views}

在Customer Journey Analytics中，建立一或多個資料檢視以定義用於報告的量度和維度。 網頁分析人員可以執行這些工作。

1. 在Customer Journey Analytics中，[建立資料檢視](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 設定檢視以包含下列資訊。

   * 如果您有Adobe Analytics帳戶，請在[!UICONTROL Time Zone]索引標籤的[!DNL Analytics]區段中，使用您[!UICONTROL Calendar]帳戶的[!UICONTROL Configure]。

   * 在[!UICONTROL Components]索引標籤上：

      * 新增您的維度、事件和摘要資料集。

      * 從事件（量度）資料集和維度（分類/中繼資料）資料集選擇量度，以納入資料檢視。

        您已在您在[最後一個程式](#dataset-connection)中建立的連線中聯結這兩個資料集。

      * 將事件資料集加入摘要資料集，該資料集尚未加入任何專案：

         * 對於每一個包含您想要在Customer Journey Analytics中可用的摘要資料的維度，[建立一個衍生欄位](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-dataviews/derived-fields)。

           例如，若要檢視行銷活動的摘要資料，請建立維度`Adobe Advertising Campaign`的衍生欄位。

           您將使用相符的索引鍵`trackingCode` (這是Adobe Advertising ID的結構描述欄位)連結這兩個資料集。

            * 在衍生規則產生器的[!UICONTROL Lookup]區段中：

               * 針對&#x200B;**[!UICONTROL Value]**&#x200B;欄位，從量度摘要資料集中選取&quot;[!UICONTROL Tracking Code]&quot;。

               * 針對&#x200B;**[!UICONTROL Lookup dataset]**&#x200B;欄位，選取維度資料集(例如「Adobe Advertising分類」)。

               * 針對&#x200B;**[!UICONTROL Matching Key]**&#x200B;欄位，從分類資料集中選取&quot;[!UICONTROL Tracking Code]&quot;。

               * 針對&#x200B;**[!UICONTROL Values to return]**&#x200B;欄位，從分類資料集中選取維度（例如&quot;[!UICONTROL Adobe Advertising Campaign]&quot;）。

           衍生欄位名稱會附加「(DF)」，例如`Adobe Advertising Campaign(DF)`。

         * 對於每個衍生欄位：

            * 在[!UICONTROL Included components]區段中，新增衍生欄位。

              現在，相同維度會列出兩個名稱(例如，「Adobe Advertising Campaign(DF)」（衍生欄位）和「Adobe Advertising Campaign」（摘要資料集中的欄位）。

            * 在摘要資料集中選取維度(例如「Adobe Advertising Campaign」)，並編輯資料集的設定。

              設定會在右側開啟。

               * 在「摘要資料群組」區段中，選取&#x200B;**[!UICONTROL Create grouping]**&#x200B;的選項。

               * 在&#x200B;**[!UICONTROL Dimension]**&#x200B;欄位中，選取衍生欄位(已附加「(DF)」，例如「Adobe Advertising Campaign(DF)」)。

               * 選取&#x200B;**[!UICONTROL Hide in reporting]**&#x200B;的選項，這會隱藏Workspace中的衍生欄位名稱。

## 在Customer Journey Analytics Workspace中設定報表和視覺效果 {#cja-reports}

在Customer Journey Analytics Workspace中，請依照下列步驟設定報表和視覺效果。 網頁分析人員可以執行這些工作。

1. [在Workspace中建立專案](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)，以根據資料檢視內設定的維度和量度來建置報表和視覺效果。

1. （如果您有來自[!DNL Google Ads]或[!DNL Microsoft Advertising]的資料）使用廣告網路特定量度的欄位（已分組為`googleConversions`和`microsoftConversions`），建立發佈者追蹤的轉換報告。

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* [必要條件](prerequisites.md)
>* [個Adobe Advertising ID已由 [!DNL Customer Journey Analytics]](ids.md)使用
>* Customer Journey Analytics中的[Adobe Advertising量度和維度](advertising-data-in-cja.md)
>* [收集AMO ID與EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
>* [Customer Journey Analytics指南](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-landing)
>* Adobe Analytics使用者的Customer Journey Analytics [使用手冊](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
