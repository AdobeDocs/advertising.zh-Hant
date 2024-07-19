---
title: 設定程式化保證交易
description: 瞭解如何設定您已與發佈商洽談的程式化預留(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 設定程式化保證交易

*[僅支援供應端平台](programmatic-guaranteed-about.md)*

在與支援的發行者交涉程式化保證(PG)交易後，您可以使用[!DNL Deal ID inbox]或手動輸入交易詳細資料在DSP中設定交易。

>[!NOTE]
>
> 對於PG交易，發佈商會處理所有預算步調、預算上限和定位。 所有允許透過DSP使用PG的SSP都確認發佈者可以設定預算上限。
>
> 在[!DNL FreeWheel]上設定與發行者的程式化預留交易需要額外的許可權和步驟。 如需詳細資訊，請參閱「[在 [!DNL FreeWheel]](freewheel-overview.md)中設定程式化預留交易的概觀」。

## 使用[!DNL Deal ID Inbox]設定程式化預留交易 {#pg-setup-deal-id-inbox}

下列方法是[!DNL FreeWheel]、[!DNL Google Authorized Buyers]和[!DNL Magnite DV+]的偏好程式。

1. [接受交易](deal-id-inbox-accept.md)。

1. 儲存交易後，選取要用於交易的廣告（或發佈商管理廣告的1x1追蹤畫素），並根據提示建立程式化預留(PG)預設位置。

   建立交易的預設PG投放位置，必須提供您100%的購買。 此型別的版位沒有鎖定目標，因此DSP可以傳回對發佈者之每個競標要求的競標。

   * 如果您接受單一交易，系統會自動將您重新導向至PG預設刊登版位建立工作流程。

     所有[!DNL FreeWheel]個交易都是以單一交易建議。

   * 如果您接受具有多個PG交易ID的提案，請確定您需要建立的每個PG預設位置。 建立所有必要的版位後，「繼續」按鈕就會啟用。

1. （選用）按一下![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**，以其他PG或非PG位置鎖定該PG交易。

   交易可以鎖定支援任何媒體型別組合（例如連線電視、桌上型電腦和音訊）的多個位置。

## 手動設定程式化預留交易

請將此方法用於所有其他SSP。

1. [手動設定交易識別碼詳細資料](deal-id-create.md)。

1. 儲存交易後，選取要用於交易的廣告（或發佈商管理廣告的1x1追蹤畫素），並根據提示建立PG預設位置。

   建立交易的PG預設刊登位置，必須提供您100%的購買內容。 此型別的版位沒有鎖定目標，因此DSP可以傳回對發佈者之每個競標要求的競標。

1. （選用）按一下![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**，以其他PG或非PG位置鎖定該PG交易。

   交易可以鎖定支援任何媒體型別組合（例如連線電視、桌上型電腦和音訊）的多個位置。

>[!MORELIKETHIS]
>
>* [關於程式化預留交易](programmatic-guaranteed-about.md)
>* [與程式化保證交易進行交涉的秘訣](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [提交廣告以進行程式化保證交易 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易識別碼收件匣中接受交易](deal-id-inbox-accept.md)
>* [手動建立交易識別碼詳細資料](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [詳細目錄功能概觀](inventory-overview.md)
