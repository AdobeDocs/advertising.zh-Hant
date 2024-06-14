---
title: 轉換使用者ID來源 [!DNL Tealium] 至通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Tealium] 第一方區段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 84ecc81745c6445d08cd743abfd412d62eddde86
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL Tealium] 至通用ID

*Beta功能*

將DSP整合用於 [!DNL Tealium] 客戶資料平台，將您組織的第一方雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。 程式使用 [!DNL Amazon Web Services] (AWS) firehose聯結器。 請依照下列步驟，與DSP共用Tealium的資料：

1. (若要將電子郵件地址轉換為 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [設定要啟用的追蹤 [!DNL Analytics] 測量](#analytics-tracking).

1. [在DSP中建立對象來源](#source-create).

1. [準備和共用區段對應資料](#map-data).

1. [在中建立聯結器 [!DNL Tealium] 共用區段資料](#tealium-connector).

1. [複製中的現有聯結器 [!DNL Tealium] 以繼續共用區段](#duplicate-connector).

1. [比較通用ID的數量與雜湊電子郵件地址的數量](#compare-id-count).

## 步驟1：設定追蹤 [!DNL Analytics] 測量 {#analytics-tracking}

*廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

若要將電子郵件地址轉換為 [!DNL RampIDs] 或 [!DNL ID5] IDs，您必須執行下列動作：

1. （如果您尚未這麼做）全部完成 [實作的先決條件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 並確保 [AMO ID和EF ID](/help/integrations/analytics/ids.md) 正在您的追蹤URL中填入。

1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

   * **的 [!DNL RampIDs]：** 您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到閱覽的轉換。 請聯絡您的Adobe客戶團隊，他們將會為您提供註冊的相關指示。 [!DNL LiveRamp] [!DNL LaunchPad] 標籤來源 [!DNL LiveRamp] 驗證流量解決方案。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md) 將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何 [可用的通用ID格式](source-about.md).

   來源設定將包含自動產生的來源金鑰，您將會使用它來準備區段對應資料。

1. 建立對象來源後，請將原始程式碼金鑰與 [!DNL Tealium] 使用者。

## 步驟3：準備和共用區段對應資料 {#map-data}

廣告商必須準備並共用區段對應資料。

1. 廣告商必須準備資料於 [!DNL Tealium]：

   1. 使用SHA-256演演算法雜湊廣告商對象的電子郵件ID。

   1. 將包含雜湊電子郵件ID的欄對應至訪客ID型別的屬性。

   1. 使用建立對象 `Tealium_visitor_id` 屬性。 套用正確的擴充功能以觸發對象。 請參閱 [[!DNL Tealium] 有關訪客ID屬性的檔案](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. 廣告商必須提供區段對應資料給Adobe帳戶團隊，才能在DSP中建立區段。 在逗號分隔值檔案中使用下列欄名和值：

   * **外部區段索引鍵：** 外部區段索引鍵，您稍後將在中的聯結器動作設定中指定該索引鍵 [!DNL Tealium]. 建議的命名慣例是&quot;`<DSP source key>_<Tealium segment name>`，例如「57bf424dc10_coffee-drinkers」。 對於DSP來源金鑰，請使用 [!UICONTROL Source Key] 從DSP對象來源設定。

   * **區段名稱：** 區段名稱。

   * **區段說明：** 區段的用途或規則，或兩者。

   * **父系ID：** 保留空白

   * **視訊CPM：** 0

   * **顯示CPM：** 0

   * **區段視窗：** 區段的存留時間。

## 步驟4：在中建立聯結器 [!DNL Tealium] 共用區段資料 {#tealium-connector}

針對您要共用的每個區段，針對觸發資料變更的每個動作建立個別的聯結器。 例如，若要共用各自有兩個觸發器的兩個區段，請建立四個聯結器。

1. Adobe帳戶團隊為廣告商提供AWS firehose聯結器憑證。

1. 在 [!DNL Tealium]， [新增聯結器](https://docs.tealium.com/server-side/connectors/add/)，使用下列選項：

   1. 選取 [!DNL AWS Firehose] 聯結器。

   1. 在來源設定中：

      1. 選取要共用的對象區段。

      1. 設定觸發器：

         * 對於區段的第一個聯結器，請選取觸發器 `Joined Audience`. 這可確保在使用者加入區段時與DSP共用資料。

         * 對於區段的第二個聯結器，請選取觸發器 `Left Audience`. 此聯結器用於處理所有退出及離開DSP區段的使用者。

   1. 在組態設定中，指定AWS firehose聯結器。 如果您尚未新增DSP的firehose聯結器，請使用下列資訊新增firehose聯結器：

      * **名稱：** 聯結器的名稱。

      * **存取金鑰：** Adobe帳戶團隊提供的存取金鑰。

      * **秘密金鑰：** Adobe帳戶團隊提供的秘密金鑰。

      * **地區：** 美國東北維吉尼亞(us-east-1)

   1. 在動作設定中，執行下列動作：

      1. 建立「將客戶資料傳送至傳遞串流（進階）」動作，使用下列資訊將資料新增至區段：

         * **動作名稱：** 動作的名稱。

         * **動作型別：** 傳送客戶資料至傳遞串流（進階）

         * **傳送資料流：** Tealium_CDP_Connector

         * **訊息資料：**  執行下列動作：

            1. 為區段選擇一個屬性：

               * 為Hashed_Email屬性命名自訂訊息 `hashed_email`.

               * 針對Cookie屬性，為自訂訊息命名 `cookies`.

            1. 在要建立自訂欄位的選項中，在 [!DNL Source Key] 欄位，輸入 [!UICONTROL External Segment Key] 這包含在 [區段對應資料](#map-data) 在前一個程式中。

               DSP將使用此索引鍵填入您的區段。

            1. （建議）建立更新動作以保持區段新鮮。

## 步驟5：複製中的現有聯結器 [!DNL Tealium] 以繼續共用區段 {#duplicate-connector}

每個區段只能有一個聯結器，每個聯結器只能有一個區段。

1. 在 [!DNL Tealium]，複製您要建立其他區段的區段，並重新命名新區段。

1. 在 [!DNL Tealium]，複製 [您建立的聯結器](#tealium-connector) ，並將新聯結器重新命名為「`<original name>-copy`」至新區段名稱。

## 步驟6：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

完成所有步驟後，24小時內即可在DSP中使用區段。 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段會在24小時內填入。 比較通用ID的數量與原始雜湊電子郵件地址的數量。

雜湊電子郵件地址轉譯為通用ID的速率應大於90%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，則應將其轉譯為90個以上的通用ID。 90%或更低的翻譯率是個問題。 如需區段計數可能變異的詳細資訊，請參閱&quot;[電子郵件ID與通用ID之間資料差異的原因](#universal-ids-data-variances).」

區段每24小時會重新整理一次。 不過，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 從重新推送區段以重新整理區段 [!DNL Tealium] 到期之前。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
