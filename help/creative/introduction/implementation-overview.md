---
title: 實作Adobe Advertising Creative概觀
description: 瞭解實作 [!DNL Creative]的基本工作流程。
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# 實作Adobe Advertising Creative概觀

*已關閉的Beta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative]營運團隊會與每個廣告商合作，設定其創意和創意體驗，在DSP中將廣告體驗實作為廣告，或向您的團隊提供第三方廣告標籤以實作自身，並驗證初始成本、點選和轉換資料。

Adobe客戶團隊、機構團隊或廣告商(視service level agreement的條款而定)需要持續監視每個體驗，並視需要加以編輯以滿足廣告商的目標。

## [!DNL Creative]體驗的初始設定工作

實作團隊及/或您的機構將與您合作，進行下列工作：

1. 定義您的個人化目標（例如您是否要個人化廣告以進行潛在客戶開發或重新目標定位）；所有可用的第一方、第二方和第三方資料，包括創意資產和受眾區段；以及達成目標的策略。<!-- and CRM data? used how/where? -->

1. （新廣告商帳戶）設定管理帳戶：

   1. 為[!DNL Creative]設定廣告商帳戶，並在Advertising Search、Social和Commerce中建立帳戶。

      [!DNL Creative]帳戶設定是在Advertising DSP內，即使廣告商未使用DSP的其餘部分。

      同樣地，即使廣告商不是[!DNL Search, Social, & Commerce]客戶，[!DNL Search, Social, & Commerce]帳戶仍可用來建立轉換追蹤標籤，以及在[!DNL Creative]中設定轉換欄。

   1. （如有必要）建立廣告商的使用者帳戶以檢視及管理其創意和廣告體驗，並產生報表。

1. （可選）如果要建立第一方對象區段以包含作為創意的目標，請以下列其中一種方式建立標籤：

   * [建立重新定位畫素](/help/creative/pixels/retargeting-pixel-manage.md)，將廣告重新定位給具有特定登入頁面或轉換頁面特定屬性的訪客，然後產生標籤以插入相關網頁。

   * (使用DSP的廣告商)在DSP中，[建立自訂對象區段](/help/dsp/audiences/custom-segment-create.md)以追蹤特定登陸頁面或轉換頁面的所有訪客，然後產生標籤以插入相關網頁。

   這兩種型別的標籤都是影像標籤，會在新增標籤的網頁上顯示1畫素x 1畫素的透明影像（畫素），一般使用者無法看到該影像。 稍後，您可以在廣告體驗中設定創意內容，以鎖定特定的重新定位畫素或區段，讓相關的廣告元素僅會向先前造訪過與該畫素或區段相關聯的網站頁面的使用者顯示。

   廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

   **注意：**&#x200B;您也可以使用來自Adobe Audience Manager和Adobe Analytics的第一方對象作為創意目標。 訪客符合從[!DNL Analytics]共用的對象資格後，該資訊便可在24到48小時內於[!DNL Creative]中操作。<!--Are times still true? -->

1. 在DSP中設定行銷活動階層，您將在其中實作廣告體驗。 使用與廣告體驗中目標定位相容的目標定位，您將在行銷活動中實施。

   階層式鎖定目標行為可能因DSP而異。 Advertising DSP會將廣告層級鎖定目標套用在（而非取代）位置層級鎖定目標之上。 例如，如果位置鎖定澳洲的使用者，而廣告鎖定日本的使用者，則廣告會將體驗鎖定為「其他所有人」分支。 請務必思考整個行銷活動結構。

1. 根據您的廣告目標設定廣告體驗：

   * **自動化工作流程：** [!DNL Creative]營運團隊可以使用廣告範本和資料摘要，為您的組織建立動態廣告。

     如需詳細資訊，請洽詢您的Adobe客戶團隊。

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **手動工作流程：**&#x200B;手動設定廣告體驗：

      1. [設定要在您的體驗中使用的標準創意](/help/creative/creative-libraries/creative-add-standard.md)：

         * 針對[!DNL Creative]將託管的創意內容，請上傳它們。 這可以在Adobe Experience Manager帳戶中包含影像資產。

         * 對於在支援的協力廠商廣告伺服器上託管的創意內容，請指向創意檔案。

      1. （選擇性） [將創意分組為組合](/help/creative/creative-libraries/bundle-manage.md)，您可以透過一個步驟將這些組合附加到目標體驗。

      1. 設定[廣告體驗](/help/creative/experiences/experience-about.md)：

         * 針對[目標廣告體驗](/help/creative/experiences/experience-create-targeting.md)，序列創意和選用的廣告目標。

           廣告目標可包含重新定位您在[!DNL Creative]中建立的畫素；您在Adobe Experience Cloud中的對象區段(包括在DSP、Audience Manager或[!DNL Analytics]中)；地理目標；或網頁上的特定資料觸發器(例如SKU=01234567890123或Cart=empty)。

         * 針對[非目標廣告體驗](/help/creative/experiences/experience-create-no-targeting.md)，建立一般體驗設定。

           廣告目標可包含重新定位您在[!DNL Creative]中建立的畫素；您在Adobe Experience Cloud中的對象區段(包括在DSP、Audience Manager或[!DNL Analytics]中)；地理目標；或網頁上的特定資料觸發器(例如SKU=01234567890123或Cart=empty)。













1. 為您的廣告體驗設定轉換追蹤：


設定轉換追蹤。 根據實作，這可能涉及新增
廣告商網頁的轉換追蹤標籤和/或設定每日
廣告商已個別收集的轉換資料的摘要拖放區。


您可以在Advertising Search、Social和Commerce內或Adobe動態標籤管理員（先前稱為動態標籤管理員）內產生Adobe Advertising轉換追蹤標籤。
注意：您必須使用JavaScript轉換標籤，而非影像標籤。


廣告商的IT部門或其他群組可能需要進行排程或通知
關於，標籤部署。


（選用）在「搜尋」、「社交」和「Commerce」中進行每次轉換（交易屬性）
在資料檢視和報告中，以個別欄集形式提供。


轉換（交易屬性）會列在下列位置的搜尋、社交和Commerce中
已追蹤至少一個轉換事件。


如果您未提供特定量度，則會合併所有轉換
在一個「轉換」欄集中。


驗證所追蹤的資料。


（選用）設定傳送排程報表至指定的電子郵件地址。


如需指示，請參閱「報表」的說明章節。


在Advertising DSP或其他DSP上設定廣告行銷活動，並提供JavaScript
或適用於廣告商廣告體驗的iframe標籤，這些廣告商可將其實作為
DSP中的第三方廣告。


監視已完成的廣告體驗的效能（檢視預先定義的）
個別體驗或建立自訂效能報表的效能詳細資料。


（視需要）根據效能和更新的訊息更新廣告體驗。






>[!MORELIKETHIS]
>
>* [關於Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [使用者介面的組織方式](/help/creative/introduction/ui.md)
