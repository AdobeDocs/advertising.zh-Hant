---
title: 關於[!UICONTROL Deal ID Inbox]
description: 瞭解[!UICONTROL Deal ID inbox]功能，此功能可讓您接受已在 [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (先前稱為 [!DNL AdX]), and [!DNL Magnite DV+]  （先前稱為 [!DNL Rubicon]）上與發佈者協商的私人交易。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 關於[!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox]可讓您快速設定DSP透過供應端平台(SSP)從發佈者匯入的交易，因此您不必手動設定每個交易。 您可以接受已經與[!UICONTROL Deal ID inbox]的[!DNL FreeWheel]、[!DNL Google Authorized Buyers] （先前稱為[!DNL AdX]）和[!DNL Magnite DV+] （先前稱為[!DNL Rubicon]）發行者交涉的已保證和未保證私人詳細目錄交易。

>[!NOTE]
>
>Advertising DSP是第一個與[!DNL FreeWheel] API整合的DSP。

在[!UICONTROL Deal ID inbox]中，您可以看到發行者看到的交易詳細資料、加速交易設定，以及避免手動輸入錯誤。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天凌晨4:30 （東部標準時間）自動重新整理所有交易詳細資料。 它也會每小時重新整理所有[!DNL FreeWheel]交易，並更新[!DNL Google]和[!DNL Magnite DV+]的現有交易。 您也可以隨時手動重新整理交易詳細資料，以填入新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>對於透過[!DNL Google Authorized Buyers]的程式化預留交易，您必須提供至少90%的預算，否則您的帳戶將無法存取[!UICONTROL Deal ID inbox]中的[!DNL Google]交易。

## 實作[!UICONTROL Deal ID Inbox]

若要在[!UICONTROL Deal ID inbox]中接收交易，您的SSP帳戶必須將您組織的DSP帳戶對應至您的SSP帳戶。 DSP可與相關SSP共用組織的帳戶名稱。 如需指示，請聯絡您的Adobe客戶團隊。

在交易洽談期間，請告訴發佈者將交易傳送給您的購買者，而不是傳送給上層DSP帳戶。 交易識別碼可以是名稱或ID，具體取決於SSP。

## 您可以對交易執行的動作

* **檢閱交易**，以確認SSP已傳送正確的發行者、發行日期、CPM和其他交易詳細資料。 如果發佈者發生錯誤，請在DSP外部聯絡他們，以便他們更正並重新傳送交易。

* 在檢閱後&#x200B;**接受交易**，這些交易不再出現在[!UICONTROL Deal ID inbox]中。 接受的交易列在[!UICONTROL Inventory] > [!UICONTROL Deals]中，並準備在廣告商的位置中鎖定目標。

* **忽略不需要或未經請求的交易**。 已忽略的交易會移至[!UICONTROL Deal ID inbox]內的[!UICONTROL Ignored Deals]索引標籤（作為封存）。 當您忽略交易時，DSP不會提醒SSP和發佈者。

* 從[!UICONTROL Inventory] > [!UICONTROL Deals] （不在[!UICONTROL Deal ID inbox]中）修改已接受交易的詳細資料&#x200B;**。**&#x200B;同樣地，當發佈者傳送變更至交易時，廣告商有責任在[!UICONTROL Inventory] > [!UICONTROL Deals]中實作這些變更，因為[!UICONTROL Deal ID inbox]在交易設定後不會同步處理來自SSP的變更。

## 無法接受哪些型別的交易？

當交易清單不包含![接受](/help/dsp/assets/accept.png)圖示或[!UICONTROL Accept]按鈕時，您無法從[!UICONTROL Deal ID inbox]接受它。 您可以[手動](/help/dsp/inventory/deal-id-create.md)建立交易ID詳細資料。

您無法接受下列交易型別：

* [!DNL Google]個非美元交易。

* [!DNL Magnite DV+]個非美元交易

* [!DNL FreeWheel]個非您帳戶貨幣的交易。

* 結束日期早於今天的交易。

* 標示為「多種媒體型別」的舊[!DNL Magnite DV+]交易。

交易詳細資訊包括無法接受交易的原因。

>[!MORELIKETHIS]
>
>* [在交易識別碼收件匣中接受交易](deal-id-inbox-accept.md)
>* [詳細目錄功能概觀](inventory-overview.md)
