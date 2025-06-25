---
title: 同步 [!DNL Adobe] 個對象
description: 瞭解如何同步處理 [!DNL Adobe] 對象的中繼資料、階層資料和不重複對象資料。
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 同步[!DNL Adobe]個對象

僅&#x200B;*[!DNL Direct Access]使用者端管理員和管理員*

*僅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics整合的廣告商*

您可以允許Search、Social和Commerce將廣告商或機構所有[!DNL Adobe]受眾的中繼資料、階層資料和不重複受眾資料提取到[!UICONTROL Campaigns] > [!UICONTROL Audiences]檢視中。 此資訊包括下列專案的資料：

* Adobe Audience Manager區段

* 發佈至Adobe Experience Cloud的Adobe Analytics區段

* 使用Adobe Experience Cloud [!DNL Audience Library]建立的區段

廣告商或機構必須實作[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)，並提供其組織識別碼（先前稱為[!DNL IMS Org ID]），才能符合資格。

初始同步處理大約需要24小時。 之後，資料會即時同步，延遲一到兩秒。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**。

1. 輸入廣告商Adobe Experience Cloud帳戶的唯一組織識別碼，然後按一下&#x200B;**[!UICONTROL Submit]**。

   如果您不知道廣告商的組織ID，請在[!UICONTROL Admin] > [!UICONTROL Manage Client]的廣告商設定中的&#x200B;**[!UICONTROL IMS Org ID]**&#x200B;欄位中查詢它。

>[!MORELIKETHIS]
>
>* [關於對象](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [與Adobe Experience Cloud解決方案和服務整合](/help/search-social-commerce/introduction/integrations.md)
