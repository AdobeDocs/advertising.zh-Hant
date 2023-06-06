---
title: 關於使用庫存摘要自動化廣告管理
description: 瞭解進階行銷活動管理，其可讓您根據產品或服務詳細目錄的相關資料，自動管理帳戶結構並提供動態廣告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 關於使用庫存摘要自動化廣告管理

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

此 [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] 進階行銷活動管理的檢視可讓您自動建立和更新廣告網路帳戶結構，並根據有關產品或服務詳細目錄的資料提供動態廣告。 您可以每天或視需要經常上傳含有產品資料的新檔案，或直接連結至 [!DNL Google] 或 [!DNL Microsoft®] 商家中心帳戶。 使用此功能可以：

* 從有序的資料來源建立新的行銷活動。

* 動態更新文字和回應式搜尋廣告， [!DNL Google Ads] 購物廣告，或 [!DNL Microsoft® Advertising] 每當處理新資料時，購物廣告都會針對可變更的資料元素（例如價格或數量）使用動態變數。 每次您變更資料時，現有的廣告都會被刪除，而新的廣告則會建立。

* 當庫存跌至特定層級以下時、根據指定的結束日期時，或當摘要資料中省略了現有元件時，自動暫停或移除廣告群組、關鍵字和廣告。

若要設定廣告，請建立包含變數（預留位置）的詳細目錄摘要範本，然後以上傳檔案或中的實際資料欄取代變數。 [已同步的Google或Microsoft®商家中心帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 變數亦可包含您在檔案中設定的修飾元群組，或檔案中的個別列，以為資料檔案中的每個適用列建立多個廣告、關鍵字、促銷活動或廣告群組。 例如，如果您在廣告標題中使用修飾詞群組變數，且修飾詞群組包含兩個修飾詞（「廉價」和「折扣」），則會為每個產品建立兩個個別的廣告 — 每個修飾詞各一個。 對象 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 動態搜尋廣告，您也可以包含廣告自訂的值。

| [!UICONTROL Ad Variation] 範本的區域 | 搜尋、社交和商務中的修飾元 | 摘要內容 | 產生的廣告 |
|----|----|----|----|
| 標題：購買高端\{<i>產品類別</i>\} &lt;<i>廉價清單</i>>.<br><br>說明1：大量\{<i>產品名稱</i>\}。<br><br>說明2：位於\{<i>折扣百分比</i>\}%折扣。 | 修飾元群組「CheapList」的值：<br><br>「物美價廉」<br><br>&quot;折扣價&quot; | 產品類別、產品名稱、折扣百分比<br>電子產品，iPods，10<br><br>服裝，襯衫，15<br><br><b>注意：</b> 您可以使用逗號或定位點來分隔值。 | <u>低價購買高端電子產品。</u><br>平板電腦庫存龐大。 可享受10%的折扣。<br><br><u>以折扣購買高階電子產品。</u><br>平板電腦庫存龐大。 可享受10%的折扣。<br><br><u>以低廉的價格購買高檔服裝。</u><br>大量庫存的襯衫。 可享受15%的折扣。<br><br><u>以折扣購買高檔服裝。</u><br>大量庫存的襯衫。 可享受15%的折扣。 |

廣告產生後，您可以選擇檢閱廣告，然後張貼至廣告網路。

>[!NOTE]
>若要使用試算表檔案大量建立或編輯行銷活動資料，請參閱&quot;[關於使用大量表單管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).」

>[!MORELIKETHIS]
>
>* [使用詳細目錄摘要管理行銷活動資料的工作流程](inventory-feeds-workflow.md)
>* [清查摘要何時建立或刪除帳戶元件？](when-are-components-created-deleted.md)

