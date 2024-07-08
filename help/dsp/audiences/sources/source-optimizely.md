---
title: 將使用者ID轉換為 [!DNL Optimizely] 通用ID
description: 瞭解如何讓 DSP 攝取第一 [!DNL Optimizely] 方細分。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 31713da81bbb1eb840de0f8e0d40013b42cd3140
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 將使用者ID轉換為 [!DNL Optimizely] 通用ID

*Beta功能*

將DSP整合用於 [!DNL Optimizely] 客戶資料平台，將您組織的第一方雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

1. (若要將電子郵件地址轉換為 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [設定要啟用的追蹤 [!DNL Analytics] 測量](#analytics-tracking).

1. [在DSP中建立對象來源](#source-create).

1. [準備及推送區段資料](#push-data).

1. [比較通用ID的數量與雜湊電子郵件地址的數量](#compare-id-count).

## 步驟1：設定追蹤 [!DNL Analytics] 測量 {#analytics-tracking}

*廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

若要轉換電子郵件地址 [!DNL RampIDs] 或 [!DNL ID5] ID，您必須執行下列操作：

1. （ 如果您還沒有這樣做 ）完整應用程式實施的所有[先決條件，並確保[在跟蹤 URL 中填充 AMO ID 和 EF ID](/help/integrations/analytics/ids.md)。 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)

1. 註冊通用 ID 合作夥伴，並在網頁上部署通用 ID 專用代碼，以匹配從桌面和移動網站瀏覽器（但不包括移動應用）上的 ID 到視圖的轉化：

   * **對於 [!DNL RampIDs]：** 您必須在網頁上部署額外的JavaScript 標記，以匹配從桌面和移動網路瀏覽器（但不包括移動應用）上的ID到視圖的轉化。 請聯絡您的Adobe客戶團隊，他們將會為您提供註冊的相關指示。 [!DNL LiveRamp] [!DNL LaunchPad] 標籤來源 [!DNL LiveRamp] 驗證流量解決方案。 註冊是免費的，但您必須簽署合約。 註冊後，您的Adobe客戶團隊將產生，並提供唯一標籤給您的組織，以在您的網頁上實施。

## 步驟2：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md) 將對象匯入您的DSP帳戶或廣告商帳戶。 您可以選擇將您的使用者識別碼轉換為任何 [可用的通用ID格式](source-about.md).

   來源設定將包含自動產生的來源金鑰，您會使用它來推送區段資料。

1. 創建對象源后，與 [!DNL Optimizely] 用戶共用原始程式碼密鑰。

## 步驟 3：準備和推送 區段 數據 {#push-data}

廣告商必須準備並推送數據，使用 [!DNL Optimizely Data Platform]. 有關該過程的任何問題，請聯繫您的 [!DNL Optimizely] 代表。

1. 在 内 [!DNL Optimizely Data Platform]，雜湊使用 SHA-256 算法的對象電子郵件 ID。

1. 按照說明將 [[!DNL Optimizely's] 區段推送到DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 包括以下資訊以啟用整合：

   * **Source索引鍵：** 這是在中建立的來源金鑰 [步驟2](#source-create).

   * **帳戶代碼：** 這是英數字元的DSP帳戶代碼，您可以在DSP中找到，網址為 [!UICONTROL Settings] > [!UICONTROL Account].

這些區段應該會在24小時內提供給DSP，並依照廣告商的設定重新整理。 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 從重新推送區段以重新整理區段 [!DNL Optimizely] 到期之前。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 步驟4：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

完成所有步驟後，請在對象庫中驗證（您從建立或編輯對象時可使用此對象庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段可用，且會在24小時內填入。 比較通用 ID 的數量和原始哈希電子郵件地址的數量。

哈希電子郵件位址到通用ID的轉換率應大於90%。 例如，如果您從客戶 數據平台發送 100 個經過哈希處理的電子郵件地址，則應將其轉換為 90 個以上的通用 ID。 90% 或更低的翻譯率是一個問題。 有關區段計數如何變化的更多信息，請參閱“[电子郵件 ID 和通用 ID](#universal-ids-data-variances) 之間數據差異的原因”。

如需疑難解答支援，請連絡Adobe Systems客戶團隊或 `adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
