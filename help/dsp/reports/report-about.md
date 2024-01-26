---
title: 關於自訂報表
description: 瞭解手動建立自訂報表或使用預先設定之報表範本的選項。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# 關於自訂報表

自訂報表可讓您使用行銷活動維度（例如廣告商、位置、網站或地標）和對您最重要的量度，自訂報表資料的內容和傳送。 您可以：

* 在精細層次完整設定行銷活動績效報表。
* 從預先設定的報表範本中選擇，並選擇性進一步自訂。

您可以產生報表一次，或排程在指定時區的03:00每日、每週或每月產生報表。 報告產生後，會傳送給每個指定的電子郵件收件者或連結 [報表目的地](/help/dsp/reports/report-destinations/report-destination-about.md) 下列型別：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL （測試版）

>[!NOTE]
>
>您也可以檢視促銷活動所有層級（行銷活動、套件、位置或廣告）的隨選資料 [在相關的行銷活動管理檢視中](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## 可用的報表型別

* **[!UICONTROL Custom]：** 此報表為空白範本，您可以使用大部分的維度和量度建立自己的自訂報表。 [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]、和 [!UICONTROL Site] 報告是此範本的各種變體，針對其各自的使用案例預先選取了欄和維度。

* 預先設定的報表範本

   * **[!UICONTROL Billing]：** 使用此報告來瞭解關鍵計費量度，例如依促銷活動劃分的媒體計費支出量度。

     >[!NOTE]
     >
     >此報表包括關於計費區段的資料。 如果向使用者或裝置提供的曝光屬於多個區段，則只會針對該曝光對一個可計費區段進行評分。

   * **[!UICONTROL Conversion]：** 此報表可讓您根據透過Adobe Advertising轉換追蹤擷取的轉換量度，瞭解行銷活動的執行狀況。 此報表包含多重接觸歸因。

   * **[!UICONTROL Device]：** 使用此預先填入的範本，依裝置相關維度檢視關鍵量度。

   * **[!UICONTROL Frequency (by Impression)]：** 使用此報表來瞭解向不重複檢視者顯示的曝光數分佈（例如，有多少不重複檢視者看到一個曝光數、兩個曝光數、三個曝光數等）。 資料可依位置或行銷活動取得。

     >[!NOTE]
     >
     >* 資料在2019年3月1日之後提供。
     >* 頻率是根據資料取樣來估計。
     >* 對於某些詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。 此報表僅包含可使用裝置識別碼的曝光數。

   * **[!UICONTROL Frequency (by App/Site)]：** 使用此報表可瞭解透過應用程式或網站觸及的不重複使用者人數。 您也可以檢視僅透過特定應用程式或網站觸及的不重複使用者人數（「不重複使用者」）。

     >[!NOTE]
     >
     >* 資料會在2018年11月15日之後提供。
     >* 對於某些私人詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。

   * **[!UICONTROL Geo]**：此預先填入的範本可供您依地理維度檢視關鍵量度。

   * **[!UICONTROL Margin]：** 使用此報表可依行銷活動或位置檢視關鍵量度，例如利潤、利潤和其他支出量度。

   * **[!UICONTROL Segment]：** 使用此預先填入的範本，按區段檢視關鍵量度。

     >[!NOTE]
     >
     >* 此報表旨在顯示不同目標區段的表現。 它使用區段會籍資料。 當向屬於兩個或多個目標區段的人或裝置提供曝光時，此報表會為每個區段包含一個列。 因此，此報表中的總計可能與實際傳送不符。
     >* 區段的轉換量度和自訂目標資料在2019年8月2日之後提供。 自2018年6月1日開始，可使用區段的所有其他資料。

   * **[!UICONTROL Site]：** 依預設，包括標準量度、媒體淨支出總計，以及依網站區分的可計費淨支出總計。

   * **[!UICONTROL Household Reach & Frequency]：** 此報表可讓您根據IP位址（而非裝置/Cookie層級），在家庭層級檢視跨廣告格式的單一維度的曝光數、觸及範圍和頻率。 運用見解來最佳化您的媒體組合、改善效能，並找出遞增觸及的機會。 請參閱&quot;[家庭報表常見問題集](/help/dsp/reports/faq-household-report.md)」以取得詳細資訊。

   * **[!UICONTROL Household Conversions]：** 此報表可讓您根據IP位址檢視家庭層級的檢視轉換，而非裝置/Cookie層級。 使用見解來測量及最佳化行銷活動績效。 請參閱&quot;[家庭報表常見問題集](/help/dsp/reports/faq-household-report.md)」以取得詳細資訊。

## 跨帳戶報告 {#cross-account-reporting}

擁有多個DSP帳戶的任何組織都可以根據組織的需求，選擇在自訂報表中啟用跨帳戶資料。 例如，您可以授予帳戶A存取帳戶B資料的許可權，並授予帳戶B存取帳戶C （但不存取帳戶A）資料的許可權。 若要啟用及設定此功能，請聯絡您的Adobe客戶團隊。

為您的組織啟用此功能後，您可以 [篩選](report-settings.md) 下列任一報表型別（依帳戶）：  [!UICONTROL Custom]， [!UICONTROL Site]， [!UICONTROL Segment]， [!UICONTROL Geo]， [!UICONTROL Device]， [!UICONTROL Frequency (by Impression)]、和 [!UICONTROL Conversion].

您的帳戶設定位於 [!UICONTROL Settings] > [!UICONTROL Account] 指定a)您的帳戶可以使用其資料的其他帳戶，以及b)可以存取您帳戶資料的其他帳戶。

>[!MORELIKETHIS]
>
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [家庭報表常見問題集](/help/dsp/reports/faq-household-report.md)
>* [關於Campaign Management檢視中的效能報表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用報表欄](/help/dsp/reports/report-columns.md)
>* [關於 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
