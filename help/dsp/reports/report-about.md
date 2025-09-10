---
title: 關於自訂報表
description: 瞭解手動建立自訂報表或使用預先設定之報表範本的選項。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: a3e6324edcf5a52f6338ce969034cd9c4b6fb487
workflow-type: tm+mt
source-wordcount: '1560'
ht-degree: 0%

---

# 關於自訂報表

自訂報表可讓您使用行銷活動維度（例如廣告商、位置、網站或地標）和對您最重要的量度，自訂報表資料的內容和傳送。 您可以：

* 在精細層次完整設定行銷活動績效報表。

* 從預先設定的報表範本中選擇，並選擇性進一步自訂。

您可以根據指定條件（例如每15天或每個月1日），在指定時區的03:00產生一次報表，或安排每日、每週或每月產生報表。 報告產生後，您可以從[!UICONTROL Reports] > [!UICONTROL Custom Reports]或以下列型別的已連結[報告目的地](/help/dsp/reports/report-destinations/report-destination-about.md)下載報告：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>您也可以在相關的行銷活動管理檢視[中，檢視行銷活動](/help/dsp/campaign-management/reports/campaign-reports-about.md)所有層級的隨選資料（行銷活動、套件、位置或廣告）。

## 可用的報表型別

* **[!UICONTROL Custom]：**&#x200B;此報表為空白範本，您可以使用大部分的維度和量度來建立自己的自訂報表。 [!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]和[!UICONTROL Site]報告是此範本的變體，並針對其各自的使用案例預先選取欄和維度。

* 預先設定的報表範本

   * **[!UICONTROL Billing]：**&#x200B;使用此報告來瞭解關鍵計費量度，例如依行銷活動的媒體計費的支出量度。 無法針對通用ID的位置使用資料。

     >[!NOTE]
     >
     >此報表包括關於計費區段的資料。 如果向使用者或裝置提供的曝光屬於多個區段，則只會針對該曝光對一個可計費區段進行評分。

   * **[!UICONTROL Conversion]：**&#x200B;請使用此報表，根據使用Adobe Advertising轉換追蹤擷取的轉換量度，瞭解行銷活動的執行狀況。 此報表包含多重接觸歸因。

  <!--
    * **[!UICONTROL Custom Creative Report Beta]:** (Beta feature) Use this report to monitor performance across your Advertising Creative ad experiences.
    -->

   * **[!UICONTROL Device]：**&#x200B;使用此預先填入的範本，依裝置相關維度檢視關鍵量度。

   * **[!UICONTROL Frequency (by Impression)]：**&#x200B;使用此報表來瞭解向不重複檢視者顯示的曝光數分佈（例如，有多少不重複檢視者看到一個曝光數、兩個曝光數、三個曝光數等）。 資料可依位置或行銷活動取得。

     >[!NOTE]
     >
     >* 資料在2019年3月1日之後提供。
     >* 頻率是根據資料取樣來估計。
     >* 對於某些詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。 此報表僅包含可使用裝置識別碼的曝光數。

   * **[!UICONTROL Frequency (by App/Site)]：**&#x200B;使用此報告來瞭解透過應用程式或網站到達您的廣告的不重複使用者數目。 您也可以檢視您的廣告僅透過特定應用程式或網站觸及的不重複使用者人數（「不重複使用者」）。

     >[!NOTE]
     >
     >* 2018年11月15日之後提供資料。
     >* 對於某些私人詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。

   * **[!UICONTROL Geo]**：使用此預先填入的範本，依地理維度檢視關鍵量度。

   * **[!UICONTROL Margin]：**&#x200B;使用此報表可依行銷活動或刊登位置檢視關鍵量度，例如利潤、利潤和其他支出量度。 無法針對通用ID的位置使用資料。

   * **[!UICONTROL Segment]：**&#x200B;使用此預先填入的範本，依區段檢視關鍵量度。

     >[!NOTE]
     >
     >* 此報表旨在顯示不同目標區段的表現。 它使用區段會籍資料。 當向屬於兩個或多個目標區段的人或裝置提供曝光時，此報表會為每個區段包含一個列。 因此，此報表中的總計可能與實際傳送不符。
     >* 區段的轉換量度和自訂目標資料在2019年8月2日後可供使用。 自2018年6月1日開始，可使用區段的所有其他資料。

   * **[!UICONTROL Site]：**&#x200B;依預設，包含標準量度、媒體淨支出總計，以及依網站區分的可計費淨支出總計。

   * **[!UICONTROL Household Reach & Frequency]：**&#x200B;此報表可根據IP位址（而非裝置/Cookie層級），在家庭層級檢視跨廣告格式的單一維度的曝光數、觸及範圍和頻率。 運用見解來最佳化您的媒體組合、改善效能，並找出遞增觸及的機會。 如需詳細資訊，請參閱[家庭報表常見問題集](/help/dsp/reports/faq-reports.md)。 無法針對通用ID的位置使用資料。

   * **[!UICONTROL Household Conversions]：**&#x200B;使用此報表來檢視根據IP位址的家庭層級檢視轉換，而非裝置/Cookie層級的檢視轉換。 使用見解來測量及最佳化行銷活動績效。 如需詳細資訊，請參閱[家庭報表常見問題集](/help/dsp/reports/faq-reports.md)。 無法針對通用ID的位置使用資料。

   * **[!UICONTROL Path to Conversion]：**&#x200B;使用此報告來識別如何最佳化預算，以及根據表現最佳的廣告互動序列來個人化廣告。 報表會顯示同一家庭中導致指定資料範圍內每個所選轉換量度的互動點順序。 報表會在首次互動與轉換之間使用指定的回顧期間，且可包含一個維度：

      * [!UICONTROL Channel Assist Type]：顯示下列行銷管道協助轉換程式的方式： [!UICONTROL Audio Impression]、[!UICONTROL CTV Impression]、[!UICONTROL Display Click]、[!UICONTROL Display Impression]、[!UICONTROL Native Click]、[!UICONTROL Native Impression]、[!UICONTROL Search Click]、[!UICONTROL Video Click]或[!UICONTROL Video Impression]。

      * [!UICONTROL Campaign ID]或[!UICONTROL Campaign Name]：顯示哪些行銷活動協助了轉換程式。

      * [!UICONTROL Ad ID]或[!UICONTROL Ad Name]會顯示哪些DSP廣告已產生轉換。

      * [!UICONTROL Ad ID & Paid Keyword (SSC)]或[!UICONTROL Ad Name & Paid Keyword (SSC)]會顯示哪些Search、Social和Commerce關鍵字導致了轉換。

     報表中的欄包括&quot;[!UICONTROL Event #1]&quot;到&quot;[!UICONTROL Event #10]&quot;[!UICONTROL Path Length]&quot;、&quot;% \&lt;轉換量度名稱1\>、&quot;% \&lt;轉換量度名稱2\>&quot;等。

     包括最多10個最近的互動點。 路徑列會依轉換次數排序。

     若要將此報告與[!DNL Advanced Measurement Services]和Adobe Analytics建立的報告進行比較，請參閱[關於自訂報告的常見問題集](/help/dsp/reports/faq-reports.md)。

   * **[!UICONTROL Path Length]：**&#x200B;使用此報表來追蹤一段時間轉換所需的使用者互動點數，以便您選擇最佳廣告頻率。 報表會依路徑長度（互動點）顯示轉換次數，例如使用者只有一個廣告互動、兩個廣告互動等後發生的轉換次數。 報表可包含多個轉換量度的資料，且會在首次互動和轉換之間使用指定的回顧期間。 報表中的欄包括「[!UICONTROL Path Length]」、「[!UICONTROL Number of] \&lt;轉換量度名稱1\>」、「% \&lt;轉換量度名稱1\>」、「\&lt;轉換量度名稱2\>」、「% \&lt;轉換量度名稱2\>」等。

     會顯示每個路徑長度（最多10個）的資料；路徑長度超過10個的資料會分組在一起。

   * **[!UICONTROL Time to Conversion]：**&#x200B;使用此報表來決定最佳歸因回顧期間，並識別轉換時間較長的行銷活動（可能受益於重新目標定位）。 報表會依上次互動（廣告曝光度或點按）到轉換的時間長度（以天為單位）顯示轉換次數。 報表可包含多個轉換量度的資料，且會在首次互動和轉換之間使用指定的回顧期間。 報表中的欄包括「[!UICONTROL Time Taken (in days)]」、「[!UICONTROL Number of] \&lt;轉換量度名稱1\>」、「% \&lt;轉換量度名稱1\>」、「\&lt;轉換量度名稱2\>」、「% \&lt;轉換量度名稱2\>」等。 需要超過回顧期間的轉換會分組在一列中（例如，如果報表使用30天的回顧期間，則所有需要超過30天的轉換會分組在具有&quot;[!UICONTROL Time Taken (in days)]&quot;值&quot;30+&quot;的列中）。

   * **[!UICONTROL Content BETA]：**&#x200B;使用此報告來依照指定的內容維度（例如型別、生產品質和內容評等）瞭解曝光傳遞和其他量度，以便您最佳化目標定位並確保品牌安全。 除了內容維度之外，該報表還包含大部分的標準維度、量度和篩選器。 依內容維度的資料可用於[!DNL Freewheel]、[!DNL Index]、[!DNL Magnite]、[!DNL Microsoft]、[!DNL Nexxen]、[!DNL Pubmatic]、[!DNL Sharethrough]和[!DNL Triplelift]。 內容訊號會由發佈者在資料流期間傳遞，並受到可用性限制。

## 跨帳戶報告 {#cross-account-reporting}

擁有多個DSP帳戶的任何組織都可以根據組織的需求，選擇在自訂報表中啟用跨帳戶資料。 例如，您可以授予帳戶A存取帳戶B資料的許可權，並授予帳戶B存取帳戶C （但不存取帳戶A）資料的許可權。 若要啟用及設定此功能，請聯絡您的Adobe客戶團隊。

為您的組織啟用此功能後，您就可以依帳戶[篩選](report-settings.md)下列任何報表型別： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。

您在[!UICONTROL Settings] > [!UICONTROL Account]的帳戶設定表示a)其他帳戶其資料可供您的帳戶使用，以及b)其他可存取您帳戶資料的帳戶。

## [!UICONTROL Custom Reports]檢視

[!UICONTROL Reports] > [!UICONTROL Custom Reports]列出您現有的報表，包括已產生的報表、已排程供未來產生的報表，以及失敗的報表。 「[!UICONTROL Report Run]」欄顯示從2024年8月22日開始觸發報告的日期。 依預設，會列出使用者建立的所有未封存報表，最新的位於頂端。 您可以進一步依狀態篩選清單，不論報表是週期性還是單次、報表型別、目的地型別和報表建立者。

您可以建立新的自訂報告、編輯現有報告或複製它們以建立新報告、立即執行報告、下載過去四個月的任何報告例項和刪除報告。

## 報表狀態 {#custom-report-status}

* **[!UICONTROL Yet to start]：**&#x200B;報表從未執行。

* **[!UICONTROL Report generating]：**&#x200B;目前正在建立報告。

* **[!UICONTROL Ready to download]：** （僅限週期性報表）報表的一或多個執行個體可供下載，且已排程多個報表執行個體。

* **[!UICONTROL Failed]：**&#x200B;報告作業失敗。 若要瞭解為何個別報表執行個體對報表拖曳執行失敗，請按一下![旁的](/help/dsp/assets/chevron-down.png "向下箭頭")向下箭頭[!UICONTROL Download]。 失敗的報表工作會以錯誤圖示(![錯誤指標](/help/dsp/assets/indicator-critical.png "錯誤指標"))表示。 將游標放在錯誤圖示上，即可取得錯誤說明。

* **[!UICONTROL Completed]：**&#x200B;對於非週期性報表，報表已完成。 對於週期性報表，所有報表例項都會完成。 您可以下載過去四個月內完成的所有報表。

* **[!UICONTROL Archived]：**&#x200B;報告已封存且無法執行。 當報表產生多次失敗時，就會設定此狀態。 目前，您無法從使用者介面設定此狀態。

>[!MORELIKETHIS]
>
>* [建立自訂報告](/help/dsp/reports/report-create.md)
>* [下載自訂報告](/help/dsp/reports/report-download.md)
>* [自訂報告設定](/help/dsp/reports/report-settings.md)
>* [關於家庭報告的常見問題集](/help/dsp/reports/faq-reports.md)
>* 行銷活動管理檢視中的[效能報表型別](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)
>* [關於[!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
