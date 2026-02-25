---
title: 上傳離線帳戶資料以用於報表和模擬
description: 瞭解如何手動上傳離線帳戶資料或上傳至 [!DNL Amazon] [!DNL S3]儲存貯體，以支援報告和模擬。 記錄檔會追蹤上載工作的進度。
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# 上傳離線帳戶資料以用於報表和模擬

*啟用帳戶資料上傳的廣告商*

針對不支援API報表和效能模擬的帳戶，上傳促銷活動內容和離線成本、點選次數和轉換資料。

您可以使用[!UICONTROL Upload Logs]功能來追蹤上載工作的進度：

* 檢視為帳戶上傳的每個檔案的清單。 每個檔案上傳工作的相關資訊包括檔案名稱、上傳頻道（*[!UICONTROL Cloud Storage]*&#x200B;或&#x200B;*[!UICONTROL Drag & Drop]*）、同步日期和狀態，以及上傳不完整的原因。

* 下載包含已針對任何工作上傳的帳戶實體和相關量度的檔案。 檔案為逗號分隔值(CSV)格式。

## 手動上傳帳戶資料

您可以在帳戶中手動上傳檔案中的資料，以填入促銷活動內容和成本、點選和轉換資料。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 執行下列任一項作業：

   * （從[!UICONTROL Accounts]檢視）：

      1. 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Upload]**。

      1. 將檔案拖曳到方塊中，或按一下&#x200B;**[!UICONTROL Browse Files]**&#x200B;並從您的裝置或網路選擇檔案。

      1. 按一下&#x200B;**[!UICONTROL Upload Files]**。

   * （從帳戶設定）：

      1. 以下列任一方式選取該帳戶：

         * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

         * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

      1. 按一下「**[!UICONTROL Upload File]**」標籤。

      1. 將檔案拖曳到方塊中，或按一下&#x200B;**[!UICONTROL Browse Files]**&#x200B;並從您的裝置或網路選擇檔案。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

# 將帳戶資料上傳至[!DNL Amazon] [!DNL S3]貯體 {#data-upload-s3}

您可以將資料上傳至[!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])貯體中的搜尋、社交和Commerce指派資料夾，藉此將促銷活動內容和成本、點選和轉換資料填入帳戶。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* 請聯絡您的Adobe帳戶團隊，為您的搜尋、社交和Commerce廣告商帳戶啟用帳戶資料上傳。 團隊將協助在[!DNL S3]儲存貯體中建立組織特定的資料夾，並在完成時通知您。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* 擷取您帳戶的[!DNL S3]雲端儲存路徑、存取金鑰ID和機密存取金鑰。 組織的所有資料上傳<!-- naming convention?-->帳戶都使用相同的存取金鑰識別碼和機密存取金鑰。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 執行下列任一項作業：

   * （從[!UICONTROL Accounts]檢視）：

      1. 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Upload]**。

      1. 在[!UICONTROL Cloud Storage Link]方塊中，按一下&#x200B;**[!UICONTROL Go to the Link]**。

      1. 按一下&#x200B;**[!UICONTROL Show Access Key and Secret]**。

      1. 在[!UICONTROL Storage Link]欄位旁邊，按一下&#x200B;**[!UICONTROL Copy]**&#x200B;以將連結複製到剪貼簿，並將連結儲存在安全的地方。

      1. 同樣地，複製並安全地儲存[!UICONTROL Access Key]和[!UICONTROL Secret Key]值。

      1. 按一下&#x200B;**[!UICONTROL Done]**。

   * （從帳戶設定）：

      1. 以下列任一方式選取該帳戶：

         * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

         * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

      1. 按一下「**[!UICONTROL Upload File]**」標籤。

      1. 在[!UICONTROL Cloud Storage Link]方塊中，按一下&#x200B;**[!UICONTROL Go to the Link]**。

      1. 按一下&#x200B;**[!UICONTROL Show Access Key and Secret]**。

      1. 在[!UICONTROL Storage Link]欄位旁邊，按一下&#x200B;**[!UICONTROL Copy]**&#x200B;以將連結複製到剪貼簿，並將連結儲存在安全的地方。

      1. 同樣地，複製並安全地儲存[!UICONTROL Access Key]和[!UICONTROL Secret Key]值。

      1. 按一下&#x200B;**[!UICONTROL Done]**。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

1. （每個組織一次）設定您的本機AWS環境：

   1. 從下列位置下載並安裝[!DNL AWS Command Line Interface] (AWS CLI)： [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)。

   1. 設定您的AWS認證：

      1. 建立純文字檔案，並將其命名為`~/.aws/credentials` （沒有副檔名）。

      1. 在任何文字編輯器中開啟檔案，並輸入組織的存取金鑰ID和機密存取金鑰，如下所示：

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. 從廣告網路下載您的帳戶資料報表並儲存。

1. 在AWS CLI中，執行下列命令以將您的帳戶資料上傳至您的[!DNL S3]雲端位置。

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   範例： `aws s3 cp filename.txt s3://cloud-location/`

## 檢視已上傳帳戶資料檔案的記錄

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Upload Logs]**。

1. （選擇性）若要下載已上傳檔案的資料，請按一下![欄中的](/help/search-social-commerce/assets/download.png "下載")下載[!UICONTROL Download]，然後依照瀏覽器的正常程式下載檔案。

## 必要資料

資料必須符合廣告網路的資料需求。 每個實體的資料欄位可能會因廣告網路而異。
