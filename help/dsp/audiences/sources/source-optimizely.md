---
title: 轉換使用者ID來源 [!DNL Optimizely] 至通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Optimizely] 第一方區段。
feature: DSP Audiences
source-git-commit: f51f07c1e057eb09c2cad292b2c8062f7d993166
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL Optimizely] 至通用ID

*Beta功能*

將DSP整合用於 [!DNL Optimizely] 客戶資料平台，將您組織的第一方雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

1. (若要將電子郵件地址轉換為 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [設定要啟用的追蹤 [!DNL Analytics] 測量](#analytics-tracking).

1. [在DSP中建立對象來源](#source-create).

1. [準備及推送區段資料](#push-data).

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

1. 建立對象來源後，請將原始程式碼金鑰與 [!DNL Optimizely] 使用者。

## 步驟3：準備並推送區段資料 {#push-data}

廣告商必須在他們的協助下準備及推送資料 [!DNL Optimizely] 代表性。

1. 範圍 [!DNL Optimizely Data Platform]，使用SHA-256演演算法將廣告商對象的電子郵件ID進行雜湊處理。

1. 聯絡廣告商的 [!DNL Optimizely] 代表將區段推送至DSP的說明。 推送區段時，請包含下列資訊：

   * **來源金鑰：** 這是在中建立的來源金鑰 [步驟2](#source-create).

   * **帳戶代碼：** 這是英數字元的DSP帳戶代碼，您可以在DSP中找到，網址為 [!UICONTROL Settings] > [!UICONTROL Account].

這些區段應該會在24小時內提供給DSP，並依照廣告商的設定重新整理。 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 從重新推送區段以重新整理區段 [!DNL Optimizely] 到期之前。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

<!--
Are they using the Data Platform web services, another type of API, or a UI? Add a link to instructions, including how to designate DSP as the destination. And where will they input the DSP-specific fields?]
-->

## 步驟4：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

完成所有步驟後，請在對象庫中驗證（您從建立或編輯對象時可使用此對象庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段可用，且會在24小時內填入。 比較通用ID的數量與原始雜湊電子郵件地址的數量。

雜湊電子郵件地址轉譯為通用ID的速率應大於90%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，則應將其轉譯為90個以上的通用ID。 90%或更低的翻譯率是個問題。 如需區段計數可能變異的詳細資訊，請參閱&quot;[電子郵件ID與通用ID之間資料差異的原因](#universal-ids-data-variances).」

如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
