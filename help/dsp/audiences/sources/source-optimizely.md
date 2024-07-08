---
title: 將使用者ID轉換為 [!DNL Optimizely] 通用ID
description: 瞭解如何讓 DSP 攝取第一 [!DNL Optimizely] 方細分。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# 將使用者ID轉換為 [!DNL Optimizely] 通用ID

*Beta功能*

使用与 客戶 数据平台的 [!DNL Optimizely] DSP 集成，將組織的第一方哈希電子郵件地址轉換為通用 ID，以便目標定位廣告。

1. （將電子郵件地址轉換至 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->;廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [設定追蹤以啟用 [!DNL Analytics] 測量](#analytics-tracking)。

1. [建立 DSP](#source-create) 中的對象來源。

1. [準備及推送區段數據](#push-data)。

1. [比較通用 ID 的數量和哈希電子郵件地址](#compare-id-count)的數量。

## 第 1 步：設置測量追蹤[!DNL Analytics] {#analytics-tracking}

*廣告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

若要轉換電子郵件地址 [!DNL RampIDs] 或 [!DNL ID5] ID，您必須執行下列操作：

1. （ 如果您還沒有這樣做 ）完整應用程式實施的所有[先決條件，並確保[在跟蹤 URL 中填充 AMO ID 和 EF ID](/help/integrations/analytics/ids.md)。 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)

1. 註冊通用 ID 合作夥伴，並在網頁上部署通用 ID 專用代碼，以匹配從桌面和移動網站瀏覽器（但不包括移動應用）上的 ID 到視圖的轉化：

   * **對於 [!DNL RampIDs]：** 您必須在網頁上部署額外的JavaScript 標記，以匹配從桌面和移動網路瀏覽器（但不包括移動應用）上的ID到視圖的轉化。 請聯繫您的Adobe Systems客戶團隊，他們將為您提供[!DNL LiveRamp][!DNL LaunchPad]註冊Authentication流量解決方案標記[!DNL LiveRamp]的說明。註冊免費，但您必須簽署協定。 註冊后，Adobe Systems客戶團隊將生成並提供唯一的標記，供組織在您的網頁上實施。

## 步驟 2：在 DSP 中建立對象源 {#source-create}

1. [建立對象來源](source-manage.md) 將對象匯入您的DSP 帳戶或廣告商 帳戶。 您可以選擇將 用戶 標識符轉換為任何 [可用的通用 ID 格式](source-about.md)。

   源設置將包括自動生成的源密鑰，你將使用該金鑰推送區段數據。

1. 創建對象源后，與 [!DNL Optimizely] 用戶共用原始程式碼密鑰。

## 步驟 3：準備和推送 區段 數據 {#push-data}

廣告商必須在其 [!DNL Optimizely] 代表的幫助下準備和推送數據。

1. 在 内 [!DNL Optimizely Data Platform]，雜湊使用 SHA-256 算法廣告商對象的電子郵件 ID。

1. 按照說明將 [[!DNL Optimizely's] 區段推送到DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 包括以下資訊以啟用整合：

   * **來源金鑰：**&#x200B;這是在步驟 2](#source-create) 中創建[的源密鑰。

   * **帳戶 Code：**&#x200B;這是字母數位DSP帳戶Code，您可以在 > 的 DSP [!UICONTROL Account]中找到[!UICONTROL Settings]。

區段應在 24 小時內可供DSP使用，並會根據廣告商的配置進行重新整理。 無論刷新區段的頻率如何，默認情況下，包含在區段中的內容會在 30 天后過期，或者在客戶指定的過期期限之後過期。 透過重新推送到期前的 [!DNL Optimizely] 區段來重新整理區段。 若要請求自定義區段到期日，請連絡您的Adobe Systems客户團隊。

## 步驟 4：比較通用 ID 的數量與哈希電子郵件地址的數量 {#compare-id-count}

完成所有步驟后，請在對象庫（從>[!UICONTROL All Audiences]或在刊登設置中創建或編輯對象[!UICONTROL Audiences]時可用）中驗證區段是否可用並在 24 小時內填充。比較通用 ID 的數量和原始哈希電子郵件地址的數量。

哈希電子郵件位址到通用ID的轉換率應大於90%。 例如，如果您從客戶 數據平台發送 100 個經過哈希處理的電子郵件地址，則應將其轉換為 90 個以上的通用 ID。 90% 或更低的翻譯率是一個問題。 有關區段計數如何變化的更多信息，請參閱“[电子郵件 ID 和通用 ID](#universal-ids-data-variances) 之間數據差異的原因”。

如需疑難解答支援，請連絡Adobe Systems客戶團隊或 `adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方受眾來源](/help/dsp/audiences/sources/source-about.md)
>* [管理物件來源以啟動通用ID Audiences](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於觀眾管理](/help/dsp/audiences/audience-about.md)
