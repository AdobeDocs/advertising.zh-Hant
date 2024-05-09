---
title: 報表目的地設定
description: 按目的地型別檢視報表目的地所需的詳細資料。
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# 報表目的地設定

非電子郵件報告目的地所需的詳細資訊因目的地型別而異。

>[!NOTE]
>
> 您也可以將自訂報表傳送給不需要已儲存報表目的地的電子郵件收件者。 您可以在報表設定中指定電子郵件收件者，而非已儲存的目標。

## [!UICONTROL S3]

**[!UICONTROL Name]：** 可協助您識別目的地的名稱。

**[!UICONTROL S3 Bucket URL]：** 上資料夾的完整路徑 [!DNL Amazon Simple Storage Service] 報告上傳至的(S3)貯體。 範例： `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]：** ([!DNL Amazon S3])貯體(提供者： [!DNL Amazon])。

**[!UICONTROL Secret Access Key]：** ([!DNL Amazon S3])貯體(提供者： [!DNL Amazon])。

## [!UICONTROL FTP]

**[!UICONTROL Name]：** 可協助您識別目的地的名稱。

**[!UICONTROL Server]：** 伺服器的主機名稱。

**[!UICONTROL Port]：** 伺服器上要使用的連線埠號碼。 預設值為 *[!UICONTROL 21]*.

**[!UICONTROL Username]：** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]：** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：** 檔案上傳到的伺服器路徑。

## [!UICONTROL SFTP]

**[!UICONTROL Name]：** 可協助您識別目的地的名稱。

**[!UICONTROL Server]：** 伺服器的主機名稱。

**[!UICONTROL Port]：** 伺服器上要使用的連線埠號碼。 預設值為 *[!UICONTROL 21]*.

**[!UICONTROL Username]：** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]：** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：** 檔案上傳到的伺服器路徑。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]：** 可協助您識別目的地的名稱。

**[!UICONTROL Server]：** 伺服器的主機名稱。

**[!UICONTROL Port]：** 伺服器上要使用的連線埠號碼。 預設值為 *[!UICONTROL 21]*.

**[!UICONTROL Username]：** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]：** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：** 檔案上傳到的伺服器路徑。

>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [建立 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [編輯 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [刪除 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
