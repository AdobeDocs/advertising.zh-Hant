---
title: 轉換使用者ID來源 [!DNL Optimizely] 至通用ID
description: 瞭解如何啟用DSP以擷取您的 [!DNL Optimizely] 第一方區段。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '593'
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

廣告商必須使用準備並推送資料 [!DNL Optimizely Data Platform]. 如對程式有任何疑問，請聯絡您的 [!DNL Optimizely] 代表性。

1. 範圍 [!DNL Optimizely Data Platform]，使用SHA-256演演算法雜湊對象的電子郵件ID。

1. 追隨 [[!DNL Optimizely's] 將區段推送至DSP的說明](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). 納入下列資訊以啟用整合：

   * **Source索引鍵：** 這是在中建立的來源金鑰 [步驟2](#source-create).

   * **帳戶代碼：** 這是英數字元的DSP帳戶代碼，您可以在DSP中找到，網址為 [!UICONTROL Settings] > [!UICONTROL Account].

區段會重新整理為廣告商設定的內容。 無論區段重新整理的頻率為何，根據預設，區段中的內容會在30天後過期，或是會在客戶指定的有效期後過期。 從重新推送區段以重新整理區段 [!DNL Optimizely] 到期之前。 若要請求自訂區段有效期，請聯絡您的Adobe客戶團隊。

## 步驟4：比較通用ID數量與雜湊電子郵件地址數量 {#compare-id-count}

這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段可用且正在填入)，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

如需有關可接受的ID轉譯率以及區段計數可能不同的原因的資訊，請參閱&quot;[電子郵件ID和通用ID之間的資料差異](#universal-ids-data-variances).」

如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
