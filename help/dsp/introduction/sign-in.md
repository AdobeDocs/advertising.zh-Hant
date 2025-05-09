---
title: 登入DSP
description: 瞭解如何登入DSP。
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 登入Adobe Advertising DSP

Adobe Advertising DSP正轉換至Adobe Identity Management服務(IMS)以進行登入驗證。 IMS提供支援IMS的所有[!DNL Adobe]產品(包括Real-Time Customer Data Platform、Customer Journey Analytics、Target和Analytics)的單一登入(SSO)存取權。 隨著變更：

* 您可以使用一個[!DNL Adobe ID]從Experience Cloud登入頁面或舊版DSP登入頁面登入[!DNL Adobe]個產品。 您的[!DNL Adobe ID]提供使用者設定檔管理。 在未來版本中，您將可從頂端功能表變更DSP帳戶、IMS組織帳戶和[!DNL Adobe]產品。

* 支援企業驗證。

* 您可以維持24小時的登入狀態，而不需每小時登入。

您目前的DSP憑證將保持作用中狀態直至2025年6月26日，以便您能夠為變更做好準備。

## 使用舊版DSP登入進行驗證

* 前往[advertising.adobe.com](https://advertising.adobe.com)，並使用舊版DSP憑證登入。

## 使用[!DNL Adobe ID]進行驗證

1. 開啟下列任一登入畫面：

   * 移至[advertising.adobe.com](https://advertising.adobe.com)。 在&quot;[!UICONTROL Sign in with the Adobe Experience Cloud account]&quot;下，按一下&#x200B;**[!UICONTROL Continue]**。

   * 移至[experience.adobe.com](https://experience.adobe.com)。

1. 輸入您的認證：

   * 如果您已經使用[!DNL Adobe]帳戶，請使用現有的認證登入。

   * 如果您沒有[!DNL Adobe]帳戶，請尋找電子郵件邀請您建立[!DNL Adobe]帳戶。 您將收到每個DSP帳戶的一個邀請。 請依照電子郵件中的連結來設定您的認證。 如果您有多個DSP帳戶，請依照指示連結它們。

1. 選擇您的組織：

   * 如果出現提示，請選取&#x200B;**個人帳戶」或&#x200B;**&#x200B;公司或學校帳戶**。

   * 如果您擁有多個IMS組織的存取權，請選取正確的IMS組織。

如需Experience Cloud介面的詳細資訊，包括管理您的使用者設定檔，請參閱&quot;[Experience Cloud介面與管理](https://experienceleague.adobe.com/zh-hant/docs/core-services/interface/experience-cloud)&quot;。

### 疑難排解

如需瞭解一般登入問題，另請參閱[解決Adobe帳戶登入問題](https://helpx.adobe.com/tw/manage-account/kb/account-password-sign-help.linkfree.html)。

#### 啟用新的[!DNL Adobe] IMS登入是否有任何先決條件？

若要新增登入帳戶，請與您的Adobe帳戶團隊共用電子郵件地址。 團隊會將您的地址新增至已布建DSP的IMS組織的使用者清單。

同時，使用者可以繼續使用其舊的DSP憑證。

#### 使用Adobe IMS帳戶登入後，系統會將我重新導向回adobe.advertising.com登入頁面。

請洽詢您的IMS組織管理員，確認您使用的電子郵件已新增至IMS組織。 如果管理員確認您已新增至IMS組織，請要求您的Adobe帳戶團隊布建您的帳戶以使用DSP。

在此期間，您可以繼續使用舊版DSP憑證。

#### 我使用不正確的電子郵件地址登入，該地址讓我登入[!DNL Adobe]，但不提供DSP存取權。

1. 移至[experience.adobe.com](https://experience.adobe.com)並登出。

1. 移至[advertising.adobe.com](https://advertising.adobe.com)，並使用正確的電子郵件識別碼登入。

#### 我的[!DNL Adobe] IMS帳戶和DSP帳戶已註冊不同的電子郵件。 我該如何使用我的[!DNL Adobe] IMS帳戶登入？

請您的Adobe帳戶團隊布建現有的[!DNL Adobe] IMS帳戶，以使用DSP。
