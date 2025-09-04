---
title: 設定資料收集、資料傳輸及報告
description: 瞭解如何設定資料收集、資料傳輸和報告。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
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

1. 收集資料並從Adobe Advertising傳送至Experience Platform Edge Network作為資料集：

   1. 在Experience Platform中，[為您要使用體驗資料模型(XDM)收集的資料定義手動結構描述](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/ui/resources/schemas)。

      * 在[!UICONTROL Schema Details]中，選取&#x200B;**[!UICONTROL Experience Event]**&#x200B;作為要擷取網站事件的結構描述的基底類別。 為結構描述命名，然後按一下&#x200B;**[!UICONTROL Finish]**。

      * 在左側面板中，新增欄位群組`Adobe Advertising Cloud ExperienceEvent Full Extension`以新增Adobe Advertising的特定欄位。<!-- Add link once published -->至少包含具有`trackingCode`和`trackingIdentities`屬性的conversionDetails物件，這些屬性包含[AMO ID和EF ID](ids.html)。 其他欄位為選用欄位。

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

1. 將貴組織的網站資料傳送至您的Experience Platform資料流：

   1. 使用Experience Platform [標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/home) （先前稱為[!DNL Launch]）來產生JavaScript標籤，以將您組織的網站資料傳送至資料流。

      * 建立標籤屬性，這是標籤設定的容器。

      * 針對您的屬性，請從擴充功能目錄[安裝「Adobe Experience Platform Web SDK」擴充功能](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)。

        此擴充功能會透過Experience Platform Edge Network，將資料從您的Web屬性傳送至Experience Cloud。

        請勿使用Adobe Advertising擴充功能。

      * 建立自訂網頁SDK組建：

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

         * 針對[!UICONTROL Advertising]設定，定義如何將廣告資料用於歸因測量。 當規則包含一系列多個動作時，此設定很有幫助，而且僅當您為自訂組建元件選取&quot;[!UICONTROL Advertising]&quot;元件時可用。 選項包括：

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

*即將推出*

## 在Customer Journey Analytics中設定資料檢視 {#cja-data-views}

在Customer Journey Analytics中，建立一或多個資料檢視以定義用於報告的量度和維度。 網頁分析人員可以執行這些工作。

*即將推出*

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
