---
title: 將使用者ID從 [!DNL Optimizely] 轉換為通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Optimizely] 第一方區段。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# 將使用者ID從[!DNL Optimizely]轉換為通用ID

*Beta功能*

使用DSP與[!DNL Optimizely]客戶資料平台的整合，將您組織的第一方雜湊電子郵件地址轉換為通用識別碼，以用於目標定位廣告。

1. （若要將電子郵件地址轉換為[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [設定追蹤以啟用 [!DNL Analytics] 測量](#analytics-tracking)。

1. [在DSP](#source-create)中建立對象來源。

1. [準備並推送區段資料](#push-data)。

1. [比較通用ID數目與雜湊電子郵件地址數目](#compare-id-count)。

## 步驟1：設定[!DNL Analytics]測量的追蹤 {#analytics-tracking}

*廣告商與[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

若要將電子郵件地址轉換為[!DNL RampIDs]或[!DNL ID5] ID，您必須執行下列動作：

1. （如果您尚未這麼做）完成實作 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)的所有必要條件，並確認已在您的追蹤URL中填入[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作夥伴註冊，並在您的網頁上部署通用ID專用程式碼，以符合從桌上型電腦和行動瀏覽器（而非行動應用程式）上的ID到瀏覽次數的轉換：

   * **對於[!DNL RampIDs]：**，您必須在您的網頁上部署額外的JavaScript標籤，以符合從桌上型電腦和行動瀏覽器（但不包括行動應用程式）上的ID到瀏覽次數的轉換。 請連絡您的Adobe客戶團隊，他們將會指示您從[!DNL LiveRamp]驗證流量解決方案註冊[!DNL LiveRamp] [!DNL LaunchPad]標籤。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md)以將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何[可用的通用ID格式](source-about.md)。

   來源設定將包含自動產生的來源金鑰，您會使用它來推送區段資料。

1. 建立對象原始碼後，請將原始碼金鑰與[!DNL Optimizely]使用者共用。

## 步驟3：準備並推送區段資料 {#push-data}

廣告商必須使用[!DNL Optimizely Data Platform]準備並推送資料。 若對此程式有任何疑問，請聯絡您的[!DNL Optimizely]代表。

1. 在[!DNL Optimizely Data Platform]內，使用SHA-256演演算法雜湊對象的電子郵件ID。

1. 依照的[[!DNL Optimizely's] 指示將區段推送到DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 納入下列資訊以啟用整合：

   * **Source金鑰：**&#x200B;這是在[步驟2](#source-create)中建立的來源金鑰。

   * **帳戶代碼：**&#x200B;這是英數字元的DSP帳戶代碼，您可以在DSP的[!UICONTROL Settings] > [!UICONTROL Account]找到該代碼。

區段會重新整理為廣告商設定的內容。 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 在到期之前從[!DNL Optimizely]重新推播您的區段，以重新整理區段。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 步驟4：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

驗證您的對象庫（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在版位設定中建立或編輯對象時可存取）中是否有該區段可用且已填入，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。 如需有關可接受的ID轉譯率以及區段計數可能有所差異的資訊，請參閱[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[啟用通用ID的支援](/help/dsp/audiences/universal-ids.md)&quot;。

若要疑難排解轉換程式的問題，請連絡您的Adobe客戶團隊或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
