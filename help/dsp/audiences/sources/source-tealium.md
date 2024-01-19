---
title: 搭配使用DSP整合的工作流程 [!DNL Tealium]
description: 瞭解如何啟用DSP以擷取您的 [!DNL Tealium] 第一方區段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 搭配使用DSP整合的工作流程 [!DNL Tealium]

您可以從以下位置分享您組織的第一方資料： [!DNL Tealium] 客戶資料平台使用 [!DNL Amazon Web Services] (AWS) firehose聯結器。 要與DSP共用Tealium中的資料有四個步驟：

1. [在DSP中建立對象來源](#source-create).

1. [準備和共用區段對應資料](#map-data).

1. [在中建立聯結器 [!DNL Tealium] 共用區段資料](#tealium-connector).

1. [複製中的現有聯結器 [!DNL Tealium] 以繼續共用區段](#duplicate-connector).

## 步驟1：在DSP中建立對象來源 {#source-create}

* [建立對象來源](source-create.md) 將對象匯入您的DSP帳戶或廣告商帳戶，並與共用原始程式碼金鑰。 [!DNL Tealium] 使用者。

## 步驟2：準備和共用區段對應資料 {#map-data}

1. 廣告商必須準備並共用區段對應資料：

   1. 廣告商必須準備資料於 [!DNL Tealium]：

      1. 廣告商對象的電子郵件ID必須使用SHA-256演演算法執行雜湊處理。

      1. 包含雜湊電子郵件ID的欄必須對應至訪客ID型別的屬性。

      1. 必須使用建立對象 `Tealium_visitor_id` 屬性。 必須套用正確的擴充功能才能觸發對象。 請參閱 [[!DNL Tealium] 有關訪客ID屬性的檔案](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. 廣告商必須提供區段對應資料給Adobe帳戶團隊，才能在DSP中建立區段。 在逗號分隔值檔案中使用下列欄名和值：

      * **外部區段索引鍵：** 外部區段索引鍵，您稍後將在中的聯結器動作設定中指定該索引鍵 [!DNL Tealium]. 建議的命名慣例是&quot;`<DSP source key>_<Tealium segment name>`，例如「57bf424dc10_coffee-drinkers」。

      * **區段名稱：** 區段名稱。

      * **區段說明：** 區段的用途或規則，或兩者。

      * **父系ID：** 保留空白

      * **視訊CPM：** 0

      * **顯示CPM：** 0

      * **區段視窗：** 區段的存留時間。

## 步驟3：在中建立聯結器 [!DNL Tealium] 共用區段資料 {#tealium-connector}

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

            1. 在要建立自訂欄位的選項中，在 [!DNL Source Key] 欄位，輸入 [!UICONTROL External Segment Key] 區段對應資料中所包含的其他欄位， [步驟2](#map-data).

               DSP將使用此索引鍵填入您的區段。

            1. （建議）建立更新動作以保持區段新鮮。

## 步驟4：複製中的現有聯結器 [!DNL Tealium] 以繼續共用區段 {#duplicate-connector}

每個區段只能有一個聯結器，每個聯結器只能有一個區段。

1. 在 [!DNL Tealium]，複製您要建立其他區段的區段，並重新命名新區段。

1. 在 [!DNL Tealium]，複製您在中建立的聯結器 [步驟3](#tealium-connector)，並從「 」重新命名新聯結器`<original name>-copy`」至新區段名稱。

>[!MORELIKETHIS]
>
>* [關於從受眾來源啟用已驗證的區段](/help/dsp/audiences/sources/source-about.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [搭配使用DSP整合的工作流程 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
