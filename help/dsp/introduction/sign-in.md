---
title: 登入DSP
description: 瞭解如何登入DSP。
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
TQID: https://experienceleague.adobe.com/KjBIag8qcpMONcX6pS2IJot3IA4Q-KOq0Av-1VzAot4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 0%

---

# 登入Adobe Advertising DSP

Adobe Advertising DSP正轉換至Adobe Identity Management服務(IMS)以進行登入驗證。 IMS使用Federated ID為所有支援IMS的[!DNL Adobe]產品提供單一登入(SSO)存取，包括Real-Time Customer Data Platform、Customer Journey Analytics、[!DNL Target]和[!DNL Analytics]。 隨著變更：

* 您可以使用一個[!DNL Adobe ID]從Adobe CX Enterprise （先前的Adobe Experience Cloud）登入頁面或舊版DSP登入頁面登入[!DNL Adobe]產品。 您的[!DNL Adobe ID]提供使用者設定檔管理。 在未來版本中，您將可從頂端功能表變更DSP帳戶、IMS組織帳戶和[!DNL Adobe]產品。

* 支援企業驗證。

* 您可以維持24小時的登入狀態，而不需每小時登入。

您目前的DSP憑證將會維持作用中一小段時間，以便您能夠為變更做好準備。

## 使用舊版DSP登入進行驗證

* 前往[advertising.adobe.com](https://advertising.adobe.com)，並使用舊版DSP憑證登入。

## 使用[!DNL Adobe ID]進行驗證

1. 開啟下列任一登入畫面：

   * 移至[advertising.adobe.com](https://advertising.adobe.com)。 在&quot;[!UICONTROL Sign in with the Adobe Experience Cloud account]&quot;下，按一下&#x200B;**[!UICONTROL Continue]**。

   * Go to [experience.adobe.com](https://experience.adobe.com).

1. Enter your credentials:

   * If you already use an [!DNL Adobe] account, then sign in with your existing credentials.

   * If you don&#39;t have an [!DNL Adobe] account, then look for an email inviting you to create an [!DNL Adobe] account. You&#39;ll receive one invitation for each of your DSP accounts. Follow the link in the email to set up your credentials. If you have multiple DSP accounts, follow the instructions to link them.

1. Choose your organization:

   * If prompted, select either **[!UICONTROL Personal Account]&quot; or **[!UICONTROL Company or School Account]**.

   * If you have access to multiple IMS organizations, select the correct one.

如需CX Enterprise介面的詳細資訊，包括管理您的使用者設定檔，請參閱&quot;[CX Enterprise介面與管理](https://experienceleague.adobe.com/en/docs/core-services/interface/experience-cloud)&quot;。

### 疑難排解

For general sign-in issues, see also &quot;[Solve Adobe account sign-in issues](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.linkfree.html).&quot;

#### Are there any prerequisites to enable a new [!DNL Adobe] IMS login?

To add a new login account, share the email address with your Adobe Account Team. The team will add your address to the user list for the IMS organization to which DSP has been provisioned.

In the meanwhile, the user can continue to use their legacy DSP credentials.

#### After signing in using an Adobe IMS account, I&#39;m redirected back to the adobe.advertising.com login page.

Check with your IMS organization administrator that the email you are using was added to the IMS organization. If the administrator confirms that you are added to the IMS organization, then ask your Adobe Account Team to provision your account to use DSP.

In the meanwhile, you can continue to use your legacy DSP credentials.

#### I signed in using an incorrect email address, which signed me into [!DNL Adobe] but doesn&#39;t provide DSP access.

1. Go to [experience.adobe.com](https://experience.adobe.com) and sign out.

1. Go to [advertising.adobe.com](https://advertising.adobe.com) and sign in with the correct email ID.

#### My [!DNL Adobe] IMS account and DSP account are registered with different emails. How do I sign in using my [!DNL Adobe] IMS account?

請您的Adobe帳戶團隊布建現有的[!DNL Adobe] IMS帳戶，以使用DSP。
