---
title: 報表目的地設定
description: 按目的地型別檢視報表目的地所需的詳細資料。
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# 報表目的地設定

非電子郵件報告目的地所需的詳細資訊因目的地型別而異。

>[!NOTE]
>
> 您也可以將自訂報表傳送給不需要已儲存報表目的地的電子郵件收件者。 您可以在報表設定中指定電子郵件收件者，而非已儲存的目標。

## [!UICONTROL S3]

**[!UICONTROL Name]：**&#x200B;可協助您識別目的地的名稱。

**[!UICONTROL S3 Bucket URL]：**&#x200B;報告上傳至的[!DNL Amazon Simple Storage Service] (S3)貯體上的資料夾完整路徑。 範例： `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]：** ([!DNL Amazon S3])貯體的存取金鑰識別碼（由[!DNL Amazon]提供）。

**[!UICONTROL Secret Access Key]：** ([!DNL Amazon S3])貯體的秘密存取金鑰（由[!DNL Amazon]提供）。

## [!UICONTROL FTP]

**[!UICONTROL Name]：**&#x200B;可協助您識別目的地的名稱。

**[!UICONTROL Server]：**&#x200B;伺服器的主機名稱。

**[!UICONTROL Port]：**&#x200B;伺服器上要使用的連線埠號碼。 預設值為&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登入伺服器的使用者名稱。

**[!UICONTROL Password]：**&#x200B;登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：**&#x200B;檔案上傳到的伺服器路徑。

## [!UICONTROL SFTP]

**[!UICONTROL Name]：**&#x200B;可協助您識別目的地的名稱。

**[!UICONTROL Server]：**&#x200B;伺服器的主機名稱。

**[!UICONTROL Port]：**&#x200B;伺服器上要使用的連線埠號碼。 預設值為&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登入伺服器的使用者名稱。

**[!UICONTROL Password]：**&#x200B;登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：**&#x200B;檔案上傳到的伺服器路徑。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]：**&#x200B;可協助您識別目的地的名稱。

**[!UICONTROL Server]：**&#x200B;伺服器的主機名稱。

**[!UICONTROL Port]：**&#x200B;伺服器上要使用的連線埠號碼。 預設值為&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登入伺服器的使用者名稱。

**[!UICONTROL Password]：**&#x200B;登入伺服器的密碼。

**[!UICONTROL Path (Optional)]：**&#x200B;檔案上傳到的伺服器路徑。

>[!MORELIKETHIS]
>
>* [關於報告目的地](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [建立報告目的地](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [編輯[!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [刪除報告目的地](/help/dsp/reports/report-destinations/report-destination-delete.md)
