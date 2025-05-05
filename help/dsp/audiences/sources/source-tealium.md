---
title: 將使用者ID從 [!DNL Tealium] 轉換為通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Tealium] 第一方區段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# 將使用者ID從[!DNL Tealium]轉換為通用ID

*Beta功能*

使用DSP與[!DNL Tealium]客戶資料平台的整合，將您組織的第一方雜湊電子郵件地址轉換為通用識別碼，以用於目標定位廣告。 處理程式使用[!DNL Amazon Web Services] (AWS) firehose聯結器。 請依照下列步驟，與DSP共用Tealium的資料：

1. （若要將電子郵件地址轉換為[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [設定追蹤以啟用 [!DNL Analytics] 測量](#analytics-tracking)。

1. [在DSP](#source-create)中建立對象來源。

1. [準備並共用區段對應資料](#map-data)。

1. [在 [!DNL Tealium] 中建立聯結器，以共用區段資料](#tealium-connector)。

1. [在 [!DNL Tealium] 中複製現有的聯結器，以繼續共用區段](#duplicate-connector)。

1. [比較通用ID數目與雜湊電子郵件地址數目](#compare-id-count)。

## 步驟1：設定[!DNL Analytics]測量的追蹤 {#analytics-tracking}

*廣告商與[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

若要將電子郵件地址轉換為[!DNL RampIDs]或[!DNL ID5] ID，您必須執行下列動作：

1. （如果您尚未這麼做）完成實作 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)的所有必要條件，並確認已在您的追蹤URL中填入[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

   * **對於[!DNL RampIDs]：**，您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到瀏覽次數的轉換。 請連絡您的Adobe客戶團隊，他們將會指示您從[!DNL LiveRamp]驗證流量解決方案註冊[!DNL LiveRamp] [!DNL LaunchPad]標籤。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md)以將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何[可用的通用ID格式](source-about.md)。

   來源設定將包含自動產生的來源金鑰，您將會使用它來準備區段對應資料。

1. 建立對象原始碼後，請將原始碼金鑰與[!DNL Tealium]使用者共用。

## 步驟3：準備和共用區段對應資料 {#map-data}

廣告商必須準備並共用區段對應資料。

1. 廣告商必須在[!DNL Tealium]內準備資料：

   1. 使用SHA-256演演算法雜湊廣告商對象的電子郵件ID。

   1. 將包含雜湊電子郵件ID的欄對應至訪客ID型別的屬性。

   1. 使用`Tealium_visitor_id`屬性建立對象。 套用正確的擴充功能以觸發對象。 請參閱有關訪客ID屬性[&#128279;](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/)的[!DNL Tealium] 檔案。

1. 廣告商必須提供區段對應資料給Adobe帳戶團隊，才能在DSP中建立區段。 在逗號分隔值檔案中使用下列欄名和值：

   * **外部區段金鑰：**&#x200B;外部區段金鑰，您稍後會在[!DNL Tealium]的聯結器動作設定中指定該金鑰。 建議的命名慣例是&quot;`<DSP source key>_<Tealium segment name>`&quot;，例如&quot;57bf424dc10_coffee-drinkers&quot;。 對於DSP來源金鑰，請使用DSP對象來源設定中的[!UICONTROL Source Key]。

   * **區段名稱：**&#x200B;區段名稱。

   * **區段說明：**&#x200B;區段的用途或規則，或兩者皆有。

   * **父系識別碼：**&#x200B;保留空白

   * **視訊CPM：** 0

   * **顯示CPM：** 0

   * **區段視窗：**&#x200B;區段存留時間。

## 步驟4：在[!DNL Tealium]中建立聯結器以共用區段資料 {#tealium-connector}

針對您要共用的每個區段，針對觸發資料變更的每個動作建立個別的聯結器。 例如，若要共用各自有兩個觸發器的兩個區段，請建立四個聯結器。

1. Adobe帳戶團隊為廣告商提供AWS firehose聯結器憑證。

1. 在[!DNL Tealium]中，[使用下列選項新增聯結器](https://docs.tealium.com/server-side/connectors/add/)：

   1. 選取[!DNL AWS Firehose]聯結器。

   1. 在來源設定中：

      1. 選取要共用的對象區段。

      1. 設定觸發器：

         * 針對區段的第一個聯結器，選取觸發器`Joined Audience`。 這可確保在使用者加入區段時與DSP共用資料。

         * 針對區段的第二個聯結器，選取觸發程式`Left Audience`。 此聯結器用於處理所有退出及離開DSP區段的使用者。

   1. 在組態設定中，指定AWS firehose聯結器。 如果您尚未新增DSP的firehose聯結器，請使用下列資訊新增firehose聯結器：

      * **名稱：**&#x200B;聯結器的名稱。

      * **存取金鑰：** Adobe帳戶團隊提供的存取金鑰。

      * **秘密金鑰：** Adobe帳戶團隊提供的秘密金鑰。

      * **地區：**&#x200B;美國東北Virginia (us-east-1)

   1. 在動作設定中，執行下列動作：

      1. 建立「將客戶資料傳送至傳遞串流（進階）」動作，使用下列資訊將資料新增至區段：

         * **動作名稱：**&#x200B;動作的名稱。

         * **動作型別：**&#x200B;將客戶資料傳送至傳遞資料流（進階）

         * **傳遞資料流：** Tealium_CDP_Connector

         * **訊息資料：**&#x200B;執行下列動作：

            1. 為區段選擇一個屬性：

               * 為Hashed_Email屬性命名自訂訊息`hashed_email`。

               * 針對Cookie屬性，將自訂訊息命名為`cookies`。

            1. 在建立自訂欄位的選項中，在[!DNL Source Key]欄位中，輸入包含在先前程式中的[區段對應資料](#map-data)中的[!UICONTROL External Segment Key]。

               DSP將使用此索引鍵填入您的區段。

            1. （建議）建立更新動作以保持區段新鮮。

## 步驟5：複製[!DNL Tealium]中的現有聯結器以繼續共用區段 {#duplicate-connector}

每個區段只能有一個聯結器，每個聯結器只能有一個區段。

1. 在[!DNL Tealium]中，複製您要建立其他區段的區段，並重新命名新區段。

1. 在[!DNL Tealium]中，複製[您在前一個程式中建立的聯結器](#tealium-connector)，並將新聯結器從&quot;`<original name>-copy`&quot;重新命名為新的區段名稱。

## 步驟6：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

驗證在您的對象資料庫中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或版位設定中建立或編輯對象時，可使用此資料庫）有區段正在填入，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。 如需有關可接受的ID轉譯率以及區段計數可能有所差異的資訊，請參閱[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)。

區段每24小時會重新整理一次。 不過，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 在到期之前從[!DNL Tealium]重新推播您的區段，以重新整理區段。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[啟用通用ID的支援](/help/dsp/audiences/universal-ids.md)&quot;。

若要疑難排解轉換程式的問題，請連絡您的Adobe客戶團隊或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
