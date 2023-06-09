---
title: 關於對象
description: 瞭解追蹤、建立和管理選項 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 對象。
source-git-commit: 0b77c54ee9214021c841b4c1cca0b3439ea71f6f
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# 關於管理 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 搜尋、社交和商務中的對象

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 僅限*

受眾資料庫會列出您所有的 [!DNL Google Ads] 以客戶資料為基礎、市場內和類似的對象，以及 [!DNL Microsoft® Advertising] 再行銷和動態再行銷、自訂、客戶比對、市場內和類似對象。 您可以使用任何 [!DNL Google Ads] 對象為 [!DNL Google Ads] 行銷活動層級和廣告群組層級目標和排除專案，而且您可以使用任何 [!DNL Microsoft® Advertising] 對象為 [!DNL Microsoft® Advertising] 行銷活動層級和廣告群組層級目標及（僅限動態再行銷對象）排除專案。 您可以新增或編輯任何對象目標的競標調整。

您也可以使用現有Adobe Experience Cloud對象中的區段或電子郵件清單，以及來自客戶關係管理(CRM)系統的各種客戶資料，來建立和管理對象：

* **Adobe受眾區段：** 具有選擇加入Adobe Audience Manager或Adobe Analytics帳戶的廣告商可以建立 [!DNL Google Ads] 客戶比對來自下列專案的對象： [!DNL Adobe] 區段：

   * (廣告商使用 [!DNL Analytics] 沒有Audience Manager的帳戶)您可以建立 [!DNL Google Ads] 客戶使用下列來源的使用者ID來比對對象： [!DNL Analytics] 與Adobe Experience Cloud共用的區段。

   * (具有Audience Manager帳戶的廣告商)您可以建立 [!DNL Google Ads] 客戶使用來自以Search、Social和Commerce作為目的地之Audience Manager區段的使用者ID來比對對象。 這可能包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud對象庫建立的區段。

  若要建立符合客戶的對象，廣告商的 [!DNL Google Ads] 帳戶必須是 [符合自訂比對的資格](https://support.google.com/adspolicy/answer/6299717) 並選擇加入 [使用者ID區段](https://support.google.com/google-ads/answer/9199250). 此外，Search、Social和Commerce中的廣告商帳戶必須設定為允許建立客戶比對受眾。<!-- For Analytics audiences: Analytics Only Integration. For Audience Manager, Enable CM/CRM option) -->

  [!DNL Adobe] 客戶資料型對象的區段資料和Cookie同步檔案會同步至 [!DNL Google Ads] 每日。

* **Adobe Campaign電子郵件清單：** 您的Adobe帳戶團隊可以幫助您設定工作流程，以建立和更新 [!DNL Google Ads] 客戶比對來自電子郵件清單的對象，範圍： [!DNL Campaign].

* **客戶資料清單：** 廣告商使用 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 符合客戶比對資格的帳戶可以建立和更新廣告網路特定的客戶資料型對象 &lt;!> — 或動態再行銷對象 — 至少針對 [!DNL Google Ads]？—>透過上傳具有主要識別碼的CSV檔案。

* **動態再行銷清單：** 廣告商使用 [!DNL Microsoft® Advertising] 帳戶可以建立和管理動態再行銷對象，以便用於透過多種方式重新鎖定最近與您產品互動的潛在客戶（例如產品檢視者或過去的買家）。 動態再行銷對象會要求您在網頁上使用廣告網路的JavaScript轉換和對象追蹤標籤。 透過搜尋和受眾網路上的購物行銷活動，使用動態再行銷清單，透過產品廣告以及搜尋行銷活動，重新鎖定受眾，透過文字廣告和動態搜尋廣告重新鎖定受眾。 <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動態再行銷對象目標的競標修飾詞未在具有「」的產品組合中進行最佳化[!UICONTROL Auto-optimize Bid Adjustment Values]」設定。

>[!NOTE]
>
>Search、Social和Commerce不會儲存您上傳或來自的任何客戶資料 [!DNL Adobe] 用來建立或編輯的區段 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 對象。

>[!MORELIKETHIS]
>
>* [建立 [!DNL Google Ads] 客戶比對對象來自 [!DNL Adobe] 對象](google-audience-from-adobe-audience.md)
>* [建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
>* [管理行銷活動和廣告群組的對象目標](audience-targets-manage.md)
>* [管理行銷活動和廣告群組的對象排除](audience-exclusions-manage.md)
