---
title: 同步 [!DNL Adobe] 對象
description: 瞭解如何為同步處理您的中繼資料、階層資料和不重複受眾資料 [!DNL Adobe] 對象。
exl-id: 7d4a3c66-5013-412f-8937-d64c336751e3
feature: Search Admin
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 同步 [!DNL Adobe] 對象

*[!DNL Direct Access]僅限使用者端管理員與管理員*

*僅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics整合的廣告商*

您可以允許Search、Social和Commerce提取所有廣告商或代理的中繼資料、階層資料和唯一受眾資料 [!DNL Adobe] 將受眾帶入 [!UICONTROL Campaigns] > [!UICONTROL Audiences] 檢視。 此資訊包括下列專案的資料：

* Adobe Audience Manager區段

* 發佈至Adobe Experience Cloud的Adobe Analytics區段

* 使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]

廣告商或代理商必須實作 [Adobe Experience Platform Identity服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 並提供其組織ID (先前稱為 [!DNL IMS Org ID])。

初始同步處理大約需要24小時。 之後，資料會即時同步，延遲一到兩秒。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. 輸入廣告商之Adobe Experience Cloud帳戶的唯一組織ID，然後按一下 **[!UICONTROL Submit]**.

   如果您不知道廣告商的組織ID，請在 **[!UICONTROL IMS Org ID]** 在廣告商設定中的欄位 [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [關於對象](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [與Adobe Experience Cloud解決方案和服務整合](/help/search-social-commerce/introduction/integrations.md)
