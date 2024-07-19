---
title: 以FTP存取報表
description: 瞭解如何在唯讀FTP位置接收報表。
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# 以FTP存取報表

您可以選擇在唯讀FTP位置接收報表，以便擷取其他自動化程式的檔案（例如，使用其他程式剖析資料）。 除了[!UICONTROL Search Engine Account Report]以外的所有基本報表和所有進階報表，都可以壓縮的TSV檔案（預設）或CSV檔案（副檔名為.ZIP）的形式傳送到FTP位置。 包含任何TSV或CSV檔案標頭，且無法隱藏。

若要以FTP存取報表，您必須存取指定的FTP帳戶，且必須使用特定命名慣例和排程來設定報表範本。

## 設定FTP帳戶以存取報表

* 請聯絡您的Adobe帳戶團隊，以設定FTP帳戶以進行報表存取。

  團隊會提供您使用者名稱和密碼。

## 設定FTP傳遞的報告範本

若要在指定的FTP目錄中產生報表，請使用下列命名慣例和排程來建立[報表範本](templates/template-create.md)。

>[!NOTE]
>
>除了[!UICONTROL Search Engine Account Report]之外，所有進階報表與基本報表都可以傳送至FTP位置。

1. 在報表範本中，將下列資訊加入範本名稱的任何位置：

   * `FTP` （大寫字母）。

   * （選用）三個系統日期中的任何一個，使用下列區分大小寫的語法，包括括弧：

      * `[TODAY]` — 包含執行報告的日期、小時和分鐘。 由於其中包含確切時間，因此相同的範本一天可以執行多次，而不會覆寫先前的報表。

      * `[SDATE]` — 包含報表日期範圍的開始日期。

      * `[EDATE]` — 包含報表日期範圍的結束日期。

   * （選擇性） `[CSV]` （大寫字母並括在方括弧中）可建立CSV格式的檔案，而非預設的TSV格式。

   範例： `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]`會建立202305051656-Portfolio-FTP-20230428-20110504.csv之類的檔案。

1. 排程報表在特定時間執行。

   報表完成的一小時內就會傳送至FTP帳戶。

>[!NOTE]
>
>* 若要透過電子郵件傳送已完成報表，只需在產生報表或範本時輸入所有電子郵件收件者的地址即可。
>* 報表會根據其指定的排程執行，並在完成的一小時內傳送到FTP帳戶。

## 存取FTP存放庫中的報表

若要存取報表，請使用您FTP帳戶的登入（`amo<userID>rpt`，例如amo1234rpt）及密碼或私密連線金鑰（如果已設定），連線至下列其中一個FTP主機：

* 國際客戶： `ftp3.adobe.net`
* 美國客戶： `ftp5.adobe.net`

>[!NOTE]
>
>報告存放庫是唯讀的，每15天會清除一次。


>[!MORELIKETHIS]
>
>* [建立報表範本](/help/search-social-commerce/reports/automation/templates/template-create.md)
