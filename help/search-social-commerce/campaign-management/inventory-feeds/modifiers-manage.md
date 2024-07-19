---
title: 管理修飾元
description: 瞭解如何設定和管理詳細目錄資料摘要之廣告範本的修飾元。
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 管理修飾元

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

修飾詞是形容詞或副詞，可在句子中新增或移除而不變更基本句子結構。 您可以建立修飾元群組，以便在摘要資料範本的各種資料欄位中作為變數使用。 您可以在帳戶結構（行銷活動和廣告群組）欄位、關鍵字、基本URL和廣告中包含修飾元，為每個關聯的修飾元值建立一個值。 例如，如果您在廣告標題中使用修飾元群組變數，且修飾元群組包含三個修飾元（「便宜」、「折扣」及「經濟適用」），則系統會為資料摘要中的每個資料列建立三個個別的廣告，每個修飾元各一個。 同樣地，如果您在廣告群組的基礎URL中加入含有多個值的修飾元群組，則會為每個產生的基礎URL建立一組關鍵字。

每個修正因子群組可包含您想要的修正因子。 每個範本只能使用一個修飾元群組。

## 建立修正因子群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Modifiers]**。

1. 按一下修飾元群組清單上方的&#x200B;**[!UICONTROL Create]**。

1. 指定修飾元群組設定：

   **[!UICONTROL Name]：**&#x200B;修飾元群組的名稱。

   **[!UICONTROL Modifiers]：**&#x200B;群組的修飾元值（每行一個）。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 編輯修飾元群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Modifiers]**。

1. 在修正因子群組清單中，按一下修正因子群組名稱。

1. 編輯修飾元群組設定：

   **[!UICONTROL Name]：**&#x200B;修飾元群組的名稱。

   **[!UICONTROL Modifiers]：**&#x200B;群組的修飾元值（每行一個）。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 刪除修飾元群組

>[!IMPORTANT]
>
>當您刪除修飾元群組時，請從現有範本的欄位中移除該修飾元群組（表示為`<modifier_group_name>`）的所有變數。 如果您嘗試使用不存在的修飾元變數，透過範本傳播資料，作業會失敗1。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Modifiers]**。

1. 選取要刪除的每個修正因子群組旁的核取方塊。

1. 按一下修飾元群組清單上方的&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Yes]**。

1. （如有必要） [從所有適用的範本中移除修飾元](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)的參考。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [管理廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
