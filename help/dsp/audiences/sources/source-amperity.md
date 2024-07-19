---
title: 將使用者ID從 [!DNL Amperity] 轉換為通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Amperity] 第一方區段。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# 將使用者ID從[!DNL Amperity]轉換為通用ID

*Beta功能*

使用DSP與[!DNL Amperity]客戶資料平台的整合，將您組織的第一方雜湊電子郵件地址轉換為通用識別碼，以用於目標定位廣告。

1. （若要將電子郵件地址轉換為[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [設定追蹤以啟用 [!DNL Analytics] 測量](#analytics-tracking)。

1. [在DSP](#source-create)中建立對象來源。

1. [準備並共用區段對應資料](#map-data)。

1. [要求從 [!DNL Amperity] 到DSP](#push-data)的資料推送。

1. [比較通用ID數目與雜湊電子郵件地址數目](#compare-id-count)。

## 步驟1：設定[!DNL Analytics]測量的追蹤 {#analytics-tracking}

*廣告商與[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

若要將電子郵件地址轉換為[!DNL RampIDs]或[!DNL ID5] ID，您必須執行下列動作：

1. （如果您尚未這麼做）完成實作 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有[必要條件，並確認已在您的追蹤URL中填入[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

   * **對於[!DNL RampIDs]：**，您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到瀏覽次數的轉換。 請連絡您的Adobe客戶團隊，他們將會指示您從[!DNL LiveRamp]驗證流量解決方案註冊[!DNL LiveRamp] [!DNL LaunchPad]標籤。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md)以將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何[可用的通用ID格式](source-about.md)。

   來源設定將包含自動產生的來源金鑰，您會使用它來推送區段資料。

1. 建立對象原始碼後，請將原始碼金鑰與[!DNL Amperity]使用者共用。

## 步驟3：準備和共用區段對應資料 {#map-data}

廣告商必須準備並共用區段對應資料。

1. 在[!DNL Amperity]內，使用SHA-256演演算法雜湊對象的電子郵件ID。

1. 廣告商必須提供區段對應資料給Adobe帳戶團隊，才能在DSP中建立區段。 在逗號分隔值檔案中使用下列欄名和值：

   * **外部區段索引鍵：**&#x200B;與區段相關聯的[!DNL Amperity]區段索引鍵。

   * **區段名稱：**&#x200B;區段名稱。

   * **區段說明：**&#x200B;區段的用途或規則，或兩者皆有。

   * **父系識別碼：**&#x200B;保留空白

   * **視訊CPM：** 0

   * **顯示CPM：** 0

   * **區段視窗：**&#x200B;區段存留時間。

## 步驟4：要求從[!DNL Amperity]推送資料到DSP {#push-data}

1. 在DSP內對應區段後，廣告商必須與其[!DNL Amperity]代表合作，將區段資料發佈至DSP。

1. 接著，廣告商必須向Adobe客戶團隊確認已收到區段資料。

這些區段應該會在24小時內提供給DSP。 驗證您的對象庫（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在版位設定中建立或編輯對象時可用）中是否有該區段可用且正在填入。

區段將會依照[!DNL Amperity]內廣告商的設定進行重新整理。 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 在到期之前從[!DNL Amperity]重新推播您的區段，以重新整理區段。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 步驟5：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

在對象庫中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在版位設定中建立或編輯對象時可用），比較通用ID的數量與原始雜湊電子郵件地址的數量。 如需有關可接受的ID轉譯率以及區段計數可能有所差異的資訊，請參閱[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[啟用通用ID的支援](/help/dsp/audiences/universal-ids.md)&quot;。

若要疑難排解轉換程式的問題，請連絡您的Adobe客戶團隊或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
