---
title: 轉換使用者ID來源 [!DNL Amperity] 至通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Amperity] 第一方區段。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL Amperity] 至通用ID

*Beta功能*

將DSP整合用於 [!DNL Amperity] 客戶資料平台，將您組織的第一方雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

1. (若要將電子郵件地址轉換為 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [設定要啟用的追蹤 [!DNL Analytics] 測量](#analytics-tracking).

1. [在DSP中建立對象來源](#source-create).

1. [準備和共用區段對應資料](#map-data).

1. [請求資料推送來源 [!DNL Amperity] 至DSP](#push-data).

1. [比較通用ID的數量與雜湊電子郵件地址的數量](#compare-id-count).

## 步驟1：設定追蹤 [!DNL Analytics] 測量 {#analytics-tracking}

*廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

若要將電子郵件地址轉換為 [!DNL RampIDs] 或 [!DNL ID5] IDs，您必須執行下列動作：

1. （如果您尚未這麼做）全部完成 [實作的先決條件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 並確保 [AMO ID和EF ID](/help/integrations/analytics/ids.md) 正在您的追蹤URL中填入。

1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

   * **的 [!DNL RampIDs]：** 您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到閱覽的轉換。 請聯絡您的Adobe客戶團隊，他們將會為您提供註冊的相關指示。 [!DNL LiveRamp] [!DNL LaunchPad] 標籤來源 [!DNL LiveRamp] 驗證流量解決方案。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md) 將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何 [可用的通用ID格式](source-about.md).

   來源設定將包含自動產生的來源金鑰，您會使用它來推送區段資料。

1. 建立對象來源後，請將原始程式碼金鑰與 [!DNL Amperity] 使用者。

## 步驟3：準備和共用區段對應資料 {#map-data}

廣告商必須準備並共用區段對應資料。

1. 範圍 [!DNL Amperity]，使用SHA-256演演算法雜湊對象的電子郵件ID。

1. 廣告商必須提供區段對應資料給Adobe帳戶團隊，才能在DSP中建立區段。 在逗號分隔值檔案中使用下列欄名和值：

   * **外部區段索引鍵：** 此 [!DNL Amperity] 和區段相關聯的區段索引鍵。

   * **區段名稱：** 區段名稱。

   * **區段說明：** 區段的用途或規則，或兩者。

   * **父系ID：** 保留空白

   * **視訊CPM：** 0

   * **顯示CPM：** 0

   * **區段視窗：** 區段的存留時間。

## 步驟4：要求從推送資料 [!DNL Amperity] 至DSP {#push-data}

1. 在DSP內對應區段後，廣告商必須搭配其 [!DNL Amperity] 代表將區段資料發佈至DSP。

1. 接著，廣告商必須向Adobe客戶團隊確認已收到區段資料。

這些區段應該會在24小時內提供給DSP。 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段可用且正在填入的區段。

區段會重新整理，就像為中的廣告商設定的一樣 [!DNL Amperity]. 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 從重新推送區段以重新整理區段 [!DNL Amperity] 到期之前。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 步驟5：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

在對象庫中（當您從以下位置建立或編輯對象時可使用該庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在位置設定內)比較通用ID數量與原始雜湊電子郵件地址數量。 如需有關可接受的ID轉譯率以及區段計數可能不同的原因的資訊，請參閱&quot;[電子郵件ID和通用ID之間的資料差異](#universal-ids-data-variances).」

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[支援啟用通用ID](/help/dsp/audiences/universal-ids.md).」

若要疑難排解轉換程式的問題，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
