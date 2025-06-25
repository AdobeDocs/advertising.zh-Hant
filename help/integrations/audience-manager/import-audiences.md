---
title: 匯入Adobe Audience Manager區段以鎖定廣告
description: 瞭解如何使用Adobe Audience Manager將您的 [!DNL Adobe] 受眾匯入Advertising DSP並搜尋
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# 匯入Adobe Audience Manager區段以鎖定廣告

Advertising DSP和[!DNL Advertising Search, Social, & Commerce]可以各自提取廣告商或機構所有[!DNL Adobe]受眾的中繼資料、階層資料和不重複受眾資料<!-- segments or audiences? Standardize terms per AAM's docs -->，包括：

* Adobe Audience Manager區段

* 發佈至Adobe Experience Cloud的Adobe Analytics區段

* 使用Adobe Experience Cloud [!DNL Audience Library]建立的區段

* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe Advertising的區段

若要存取DSP或[!DNL Creative]中的[!DNL Adobe]個對象，您必須將對象匯入DSP。 若要存取[!DNL Search, Social, & Commerce]中的[!DNL Adobe]個對象，您必須將對象匯入[!DNL Search, Social, & Commerce]。

## 先決條件

* 廣告商必須實作[該 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) 2.0版或更新版本。 [!DNL Identity Service]提供永續性的通用ID，可識別Experience Cloud所有解決方案的訪客。

  實作包括將[!DNL Identity service]程式碼新增至廣告商網站上的每個網頁。

* 組織必須已啟用Experience Cloud服務[&#128279;](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview)，且具有Experience Cloud [!DNL Organization ID] （先前稱為[!DNL IMS org ID]）。

  [!UICONTROL Organization ID]可讓擁有多個Adobe Experience Cloud產品的組織在某些產品之間共用資料。

* （具有[!DNL Analytics]的廣告商）廣告商必須[使用`appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) 1.6.4或更新版本實作 [!DNL Analytics] 。

* 廣告商的網站訪客不包含大量的[!DNL Apple Safari]位使用者。

* (當廣告商同時使用Audience Manager和[!DNL Analytics]時建議使用)若要減少每個網頁的呼叫，請移除資料收集的現有Audience Manager [!DNL Data Integration Library]程式碼，並改為為每個[!DNL Analytics]報表套裝啟用伺服器端轉送。 如需詳細資訊，請參閱[伺服器端轉送概觀](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf)。

* （建議）若符合率較高，僅將第一方網站資料傳送至Adobe Advertising。 如果廣告商繫結來自客戶關係管理系統的第三方資料或離線資料，資料洩漏可能會降低匹配率。

## 將Audience Manager對象匯入DSP

### 將受眾匯入DSP的步驟

[!DNL Adobe]帳戶和資料作業團隊會執行下列步驟。

1. Adobe帳戶團隊應該設定廣告商層級設定&quot;[!UICONTROL Adobe Analytics Cloud]&quot;。

1. Adobe客戶團隊應向資料營運團隊提交請求，以使用Advertising DSP原生API整合匯入組織的Audience Manager區段。

### Audience Manager會有哪些變更？

API會自動執行下列動作：

* 在Audience Manager中建立兩個DSP目的地：

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 將兩個目的地對應至所有Audience Manager區段，讓Audience Manager可以與DSP廣告商帳戶(與用於Audience Manager的相同Experience Cloud [!DNL Organization ID]相關聯)共用區段。

  組織可選擇性地從Audience Manager中的目的地移除不需要的區段。

* 將下列Exchange Cookie同步畫素新增至組織的Audience Manager容器，以擴大客戶促銷活動的觸及範圍：

   * Adobe AdCloud： 411 (此畫素為[!DNL Identity Service] 2.0版的標準及自動組成部分。[!DNL Identity Service]版本低於2.0的組織應將此畫素新增至其Audience Manager容器。

## 將Audience Manager對象匯入[!DNL Search, Social, & Commerce]

### 將對象匯入至[!DNL Search, Social, & Commerce]的步驟

[!DNL Adobe]人員可執行下列大部分或全部步驟。

1. Adobe客戶團隊應向資料作業團隊提交請求，以設定[!DNL Search, Social, & Commerce]與Audience Manager之間的整合。 包含您要匯出至[!DNL Search, Social, & Commerce]的Audience Manager區段名稱。

1. 在Audience Manager中，設定[!DNL Search, Social, & Commerce]的目的地：

   1. 建立兩個新目的地： `[!UICONTROL Adobe Media Optimizer (HTTP)]`和`[!UICONTROL Adobe Media Optimizer Batch Destination]`。

      [!DNL Media Optimizer]是[!DNL Search, Social, & Commerce]的舊名稱。

   1. 指定每個目的地的區段。

      透過[!UICONTROL Automatically map all current and future segments]選項，所有區段都會每日對應及同步。

      [!UICONTROL Manually map segments]選項可讓您手動對應區段以與批次目的地(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)同步。 不需要手動將任何區段對應至HTTP目的地。

1. 在[!DNL Search, Social, & Commerce]內，[!DNL Search, Social, & Commerce]實作團隊或具有直接存取使用者端管理員角色的使用者應該從[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup]起始匯入。

   需要組織的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 此ID必須與用於組織Audience Manager帳戶的ID相同。

### Audience Manager會有哪些變更？

在Audience Manager中，組織可以使用兩個[!DNL Search, Social, & Commerce]目的地：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## 資料同步

初始匯入需要約24小時。 初次匯入後，資料會即時同步，延遲一到兩秒。

區段會籍資料只會在下列其中一個事件發生後傳送：

* (使用DSP的廣告商)：

   * Adobe Advertising顯示廣告會定位此區段。

   * 區段已新增到Audience Manager使用者介面中的[!DNL Adobe AdCloud Cross-Channel]批次和即時目的地。

* （具有[!DNL Search, Social, & Commerce]的廣告商）：

   * 在Adobe Advertising搜尋廣告中鎖定該區段。

   * 區段會新增至Audience Manager使用者介面中的[!DNL Adobe Media Optimizer]批次和HTTP目的地。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP如何同步資料

DSP會使用[!DNL Adobe Experience Cloud Identity (ECID) Service]自動同步資料。 同步期間，[!DNL ECID Service]會在[!DNL cm.everesttech.net]呼叫Adobe Advertising。 由於Adobe Advertising是值得信賴的網域，ID同步會從上層頁面進行，而非像大多數第三方啟用合作夥伴所做的那樣，在目的地發佈iframe內進行。 Audience Manager會使用[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam) （也稱為[!DNL Device ID]），依裝置ID識別不重複使用者。

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### 搜尋、社交和Commerce如何同步資料

搜尋、社交和Commerce會使用[!DNL Adobe Experience Cloud Identity (ECID) Service]自動同步資料。 同步期間，[!DNL ECID Service]會在[!DNL cm.everesttech.net]呼叫Adobe Advertising，這是屬於Adobe Advertising的受信任網域。 Audience Manager會使用[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam) （也稱為[!DNL Device ID]），依裝置ID識別不重複使用者。

## 在何處尋找您的同步區段

### 在DSP中

DSP會依Audience Manager分類法組織區段名稱，並在以下專案中包含對應的區段會籍數：

* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：在[!UICONTROL Audience Targeting]區段的[!UICONTROL Adobe Segments]索引標籤上。

* 在[對象設定](/help/dsp/audiences/audience-settings.md)中：在[!UICONTROL Adobe Segments]索引標籤上。

### 在Advertising Creative中

在[!DNL Creative]中，可在目標節點的體驗設定中使用區段。

### 在[!DNL Advertising Search, Social, & Commerce]

在[!DNL Search, Social, & Commerce]中，當您從[!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library]使用[!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot;建立[!DNL Google]對象時，可以使用區段。

對於您建立的每個[!DNL Google]個對象，[!DNL Google]會提供對象人數。

>[!MORELIKETHIS]
>
>* [Adobe Advertising與Adobe Audience Manager的整合](/help/integrations/audience-manager/overview.md)
