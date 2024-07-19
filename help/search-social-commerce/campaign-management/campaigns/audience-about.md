---
title: 關於對象
description: 瞭解追蹤、建立和管理 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 對象的選項。
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 關於管理Search、Social和Commerce中的[!DNL Google Ads]和[!DNL Microsoft Advertising]對象

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]*

受眾資料庫會列出您所有[!DNL Google Ads]以客戶資料為根據、以市場內和類似的受眾，以及您的[!DNL Microsoft Advertising]再行銷和動態再行銷、自訂、客戶符合、市場內和類似的受眾。 您可以使用任何[!DNL Google Ads]個對象做為[!DNL Google Ads]個行銷活動層級和廣告群組層級的目標和排除專案，也可以使用任何[!DNL Microsoft Advertising]個對象做為[!DNL Microsoft Advertising]個行銷活動層級和廣告群組層級目標和（僅限動態再行銷對象）排除專案。 您可以新增或編輯任何對象目標的競標調整。

您也可以使用現有Adobe Experience Cloud對象中的區段或電子郵件清單，以及客戶關係管理(CRM)系統中的各種客戶資料，來建立和管理對象：

* **Adobe對象區段：**&#x200B;選擇加入Adobe Audience Manager或Adobe Analytics帳戶的廣告商可以從其[!DNL Adobe]區段中建立[!DNL Google Ads]個客戶相符對象：

   * (具有[!DNL Analytics]個帳戶的廣告商也不具備Audience Manager)您可以使用與Adobe Experience Cloud共用的[!DNL Analytics]區段中的使用者ID，建立[!DNL Google Ads]個客戶相符對象。

   * (具有Audience Manager帳戶的廣告商)您可以使用以搜尋、社交和Commerce作為目的地的Audience Manager區段中的使用者ID，建立[!DNL Google Ads]個客戶相符對象。 這可能包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud對象庫建立的區段。

  若要建立客戶相符對象，廣告商的[!DNL Google Ads]帳戶必須[符合自訂相符的條件](https://support.google.com/adspolicy/answer/6299717)並選擇加入[使用者ID區段](https://support.google.com/google-ads/answer/9199250)。 此外，搜尋、社交和Commerce中的廣告商帳戶必須設定為允許建立客戶相符對象。

  客戶資料型對象的[!DNL Adobe]區段資料和Cookie同步檔案每天都會同步至[!DNL Google Ads]。

* **Adobe Campaign電子郵件清單：**&#x200B;您的Adobe客戶團隊可以協助您設定工作流程，以從[!DNL Campaign]內的電子郵件清單建立和更新[!DNL Google Ads]客戶相符對象。

* **客戶資料清單：**&#x200B;擁有[!DNL Google Ads]或[!DNL Microsoft Advertising]帳戶且符合客戶比對資格的廣告商，可以建立和更新廣告網路特定客戶資料型對象&lt;！ — 或動態再行銷對象 — 至少針對[!DNL Google Ads]？—>包含在客戶資料型對象中，方式為上傳具有主要識別碼的CSV檔案。

* **動態再行銷清單：**&#x200B;擁有[!DNL Microsoft Advertising]帳戶的廣告商可以建立和管理動態再行銷對象，您可以使用這些對象，以多種方式之一重新鎖定最近與您產品互動的潛在客戶（例如產品檢視者或過去的買家）。 動態再行銷對象需要您在網頁上使用廣告網路的JavaScript轉換和對象追蹤標籤。 透過搜尋和受眾網路上的購物行銷活動，使用動態再行銷清單，透過產品廣告以及搜尋行銷活動，重新鎖定受眾，透過文字廣告和動態搜尋廣告重新鎖定受眾。<!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動態再行銷對象目標的競標修飾詞未在具有&quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;設定的組合中進行最佳化。

>[!NOTE]
>
>搜尋、Social和Commerce不會儲存您上傳或用來建立或編輯[!DNL Google Ads]或[!DNL Microsoft Advertising]對象之[!DNL Adobe]區段的任何客戶資料。

>[!MORELIKETHIS]
>
>* [建立 [!DNL Google Ads] 來自 [!DNL Adobe] 受眾的客戶比對受眾](google-audience-from-adobe-audience.md)
>* [從Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
>* [管理行銷活動和廣告群組的對象目標](audience-targets-manage.md)
>* [管理行銷活動和廣告群組的對象排除](audience-exclusions-manage.md)
