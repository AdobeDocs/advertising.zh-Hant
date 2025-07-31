---
title: （新UI）使用者管理
description: 瞭解如何管理使用者存取許可權。
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# （新UI）搜尋、社交和商務的使用者管理

某些使用者可以使用[Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)管理新搜尋、社交和Commerce使用者介面的存取權，這是管理所有Adobe權益和使用者管理的中心位置。 使用者分為一般使用者或管理員。 如果您是管理員，Adobe帳戶團隊會通知您。 如果您是管理員，請參閱下列章節，以識別管理使用者的許可權和工作流程。

## 管理員型別

Admin Console提供多種型別的管理員。 搜尋、社交和Commerce需要下列管理員型別和許可權。 如果您想要委派使用者管理任務，可以新增其他型別。

**系統管理員：**&#x200B;管理組織所有產品的超級使用者，包括組織的所有使用者端執行個體。 （使用者端例項與舊版廣告商帳戶相同，每個組織ID有一或多個例項）。 系統管理員可以執行組織的Admin Console中的所有管理任務，也可以將組織任何產品的管理功能委派給其他使用者。

**產品管理員：**&#x200B;管理特定[!DNL Adobe]產品(例如Search、Social和Commerce)的存取權以及該產品的使用者權益。 產品管理員可以建立產品的產品設定檔、建立（但不會移除）產品的使用者和使用者群組、從產品設定檔中新增或移除使用者和使用者群組，以及在產品中新增或移除其他產品管理員。

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## 預設產品設定檔

產品設定檔與角色類似，可讓使用者有權使用特定產品的特定服務。

搜尋、社交和商務的新使用者介面具有以下預設產品設定檔，這些設定檔提供不同的功能和服務子集。 您無法編輯預設產品設定檔的產品許可權，或刪除預設產品設定檔。 不過，產品管理員、產品設定檔管理員和系統管理員可視需求使用不同可用許可權子集來建立和管理其他產品設定檔。

* **[!UICONTROL Basic Optimization]：**&#x200B;此設定檔提供下列功能：

   * [!UICONTROL Objectives]：完整存取權

   * [!UICONTROL Simulations]：完整存取權

   * [!UICONTROL Portfolio Groups]：完整存取權

   * [!UICONTROL Portfolios]：建立/編輯[!UICONTROL Objectives]、[!UICONTROL Campaigns]和支出[!UICONTROL Management]投資組合設定的存取權；其餘投資組合設定的唯讀存取權。

   * [!UICONTROL Campaigns]：對行銷活動設定的唯讀存取權（無可用的建立、編輯或刪除功能）；對限制和投資組合指派的完整存取權

   * [!UICONTROL Ad Groups]：對廣告群組設定的唯讀存取權（無可用的建立、編輯或刪除功能）；對限制和投資組合指派的完整存取權

  對於仍在學習使用「搜尋」、「社交」和「Commerce」的使用者，建議使用此存取層級。

* **[!UICONTROL Expert Optimization]：**&#x200B;此設定檔提供下列功能：

   * [!UICONTROL Objectives]：完整存取權

   * [!UICONTROL Simulations]：完整存取權

   * [!UICONTROL Portfolio Groups]：完整存取權

   * [!UICONTROL Portfolios]：完整存取權

   * [!UICONTROL Campaigns]：對行銷活動清單的唯讀存取權（尚未提供行銷活動建立、編輯或刪除功能）；對限制和投資組合指派的完整存取權

   * [!UICONTROL Ad Groups]：對廣告群組清單的唯讀存取權（尚未提供行銷活動建立、編輯或刪除功能）；對限制和投資組合指派的完整存取權

  搜尋、社交和Commerce的專家使用者建議使用此存取層級。

* **[!UICONTROL Read-Only]：**&#x200B;此設定檔提供下列功能：

   * [!UICONTROL Objectives]：唯讀存取權

   * [!UICONTROL Simulations]：唯讀存取權

   * [!UICONTROL Portfolio Groups]：唯讀存取權

   * [!UICONTROL Portfolios]：唯讀存取權

   * [!UICONTROL Campaigns]：唯讀存取權

   * [!UICONTROL Ad Groups]：唯讀存取權

* **[!UICONTROL Admin]：**&#x200B;此設定檔授與所有可用功能的完整存取權，並允許使用者建立新的使用者端執行個體（與舊版廣告商帳戶相同，每個組織識別碼有一或多個執行個體）。 除非您具備適當的業務理由，否則請勿將此權利指派給任何人。

## 管理員的任務

### 登入Adobe Admin Console並開啟它以進行「搜尋」、「社交」和「Commerce」

>[!PREREQUISITES]
>
>您必須擁有Search、Social和Commerce的管理員存取權型別才能登入Admin Console。

1. 請前往https://adminconsole.adobe.com/enterprise/。

1. (如果您尚未登入Experience Cloud)登入Experience Cloud：

   1. 輸入您的[!DNL Adobe] ID，然後按一下&#x200B;**[!UICONTROL Continue]**。

   1. 選取&#x200B;**[!UICONTROL Personal Account]」或&#x200B;**&#x200B;[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. 選取適用的Experience Cloud組織。

      Admin Console會開啟至「[!UICONTROL Overview]」標籤。

   1. 在[!UICONTROL Product & services]底下，按一下「[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]」。

      產品頁面會開啟至「搜尋」、「社交」和「Commerce」的「[!UICONTROL Product profiles]」標籤。 其他索引標籤包括[!UICONTROL Users]和[!UICONTROL Product Admins]。

### 系統管理員的工作流程

請依照此工作流程操作Search、Social和Commerce的每個使用者端例項。

1. [登入Adobe Admin Console並開啟它以搜尋、社交和Commerce](#open-admin-console)。

1. （選擇性） [新增其他系統管理員](https://helpx.adobe.com/tw/enterprise/using/admin-roles.html#enterprise)作為備份。

1. 由[新增產品管理員](https://helpx.adobe.com/tw/enterprise/using/admin-roles.html#enterprise)委派產品和使用者管理。

### 產品管理員的工作流程

請依照此工作流程操作Search、Social和Commerce的每個使用者端例項。

1. [登入Adobe Admin Console並開啟它以搜尋、社交和Commerce](#open-admin-console)。

1. 視需要大量建立一般使用者[個別](https://helpx.adobe.com/tw/enterprise/using/manage-users-individually.html)或[&#128279;](https://helpx.adobe.com/tw/enterprise/using/bulk-upload-users.html)。

1. （選擇性）為執行個體建立[使用者群組](https://helpx.adobe.com/tw/enterprise/using/user-groups.html)，並將使用者指派給每個使用者群組。

   如果執行個體有許多使用者，請建立使用者群組，以確保根據使用者的專業知識層級為其指派正確的設定檔。 （請參閱步驟4，將使用者群組指派至產品設定檔。） 您可以根據業務範圍、使用者存取需求、使用者僱用日期或其他條件來建立使用者群組。

   >[!IMPORTANT]
   >
   >使用者群組名稱應清楚傳達使用者群組應獲指派的許可權。 例如，如果您想要建立具有「唯讀」許可權的使用者群組，請在使用者群組名稱中加入「唯讀」，例如「Acme_Uk_ReadOnly」或「Acme_ReadOnly」。

1. （選擇性） [使用定義的許可權集建立自訂產品設定檔](https://helpx.adobe.com/tw/enterprise/using/manage-product-profiles.html)。

   除了現有的四個預設產品設定檔之外，還新增了自訂設定檔。

   組織的每個產品設定檔都必須有唯一名稱。 如果您的組織使用多個Search、Social和Commerce執行個體（例如Acme_US和Acme_JP），則您無法在多個執行個體中複製產品設定檔名稱。 **最佳作法：**&#x200B;使用命名慣例`<Name>_<Instance>,`，例如「Implations_Only_JP」。

   **警告：**&#x200B;產品許可權非常精細。 設定自訂產品設定檔時請務必小心，否則可能會忽略要包含的功能。

1. [手動或大量指派每個使用者或使用者群組至相關的產品設定檔](https://helpx.adobe.com/tw/enterprise/using/manage-product-profiles.html)。

## 完整的使用者管理指南和其他連結

* 如需使用Adobe Admin Console進行使用者管理的詳細資訊，請參閱《[Adobe企業與團隊管理指南](https://helpx.adobe.com/tw/enterprise/admin-guide.html)》，包括[Admin Console概觀](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)。

* Admin Console： [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
