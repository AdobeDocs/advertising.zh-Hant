---
title: 管理重新目標畫素
description: 瞭解如何建立並實作重新定位畫素，以作為廣告體驗的目標。
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# 管理重新目標畫素

*已關閉的Beta*

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

您可以建立重新定位畫素，以識別使用使用者Cookie或通用ID進入廣告商登陸頁面或轉換頁面的訪客，並擷取頁面正在追蹤這些訪客的特定屬性。 此畫素會追蹤訪客在頁面上執行的最新事件。 建立畫素之後，即可產生畫素標籤，插入相關網頁，開始追蹤訪客。<!-- Note to self: surfer id=cookie or universal ID -->

然後您可以使用畫素做為廣告體驗中任何創意的目標，以只向具有指定屬性的使用者顯示廣告，這些使用者先前造訪過與畫素關聯的網頁。 例如，如果網頁追蹤這些屬性值，您可以鎖定看過10號紅色鞋子的訪客。<!-- better example? Make sure they match attribute examples below -->

重新目標定位設定檔會儲存180天。

範例畫素：

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative]目前僅支援Advertising DSP的通用ID。 未來版本將支援協力廠商DSP的通用ID。<!-- Clarify this and reword as needed -->
>* 您也可以使用來自Adobe Audience Manager和Adobe Analytics的第一方對象作為您體驗的[創意目標](/help/creative/experiences/experience-settings-targeting.md)。
>* 當您在Advertising DSP版位內使用體驗作為廣告時，可以將版位鎖定為您在DSP中可以使用的所有對象。 您也可以[建立自訂對象區段標籤](/help/dsp/audiences/custom-segment-create.md)以追蹤特定登陸頁面的所有訪客，然後將這些區段作為刊登的創意目標。
>* 已選擇退出追蹤以進行廣告定位的網站訪客，不會根據對象區段或重新定位設定檔收到內含個人化創意內容的廣告。

## 建立重新定位畫素

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Creative]**，然後選取> **[!UICONTROL Retargeting Pixel]**。

1. 指定[重新定位畫素設定](#retargeting-pixel-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. [產生畫素標籤](#retargeting-pixel-generate)以提供給廣告商或網站連絡人。

   重新定位畫素標籤必須是頁面上的最後一個動作。<!-- verify here and below -->

   廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

## 編輯重新定位畫素

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 將游標停留在畫素名稱上，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[重新定位畫素設定](#retargeting-pixel-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. [產生畫素標籤](#retargeting-pixel-generate)以提供給廣告商或網站連絡人，讓他們可以取代原始標籤。

   重新定位畫素標籤必須是登陸頁面上的最後一個動作。

   廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

## 產生重新定位畫素的標籤 {#retargeting-pixel-generate}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 將游標停留在畫素名稱上，然後按一下&#x200B;**[!UICONTROL Generate Tag]**。

1. 按一下&#x200B;**[!UICONTROL Copy to Clipboard]**&#x200B;將標籤複製到電腦的剪貼簿，您可以將文字貼到檔案中儲存。

1. 在畫素標籤中，將「`Insert <attribute>`」替換為值，以指定`<img src>`和`<script src>`區段中每個屬性的值。 如果標籤擷取通用ID，請指定ID5合作夥伴ID。

   如果您手動新增其他屬性，則必須包含URL編碼。

   例如，如果您包含屬性「category」、「color」和「size」並擷取ID5通用ID，則畫素標籤會包含以下引數： `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--`和`&id5pid=--Insert ID5_PARTNER_ID--`。 若要鎖定選取大小為10的紅色涼鞋的使用者，例如，將影像標籤和指令碼標籤中的引數變更為`&ut1=sandals&ut2=red&ut3=10`，並在指令碼標籤中輸入您的ID5合作夥伴ID，例如`&id5pid=0123456789`。

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. 提供廣告商或網站連絡人的已完成畫素標籤，以及要插入標籤的相關登入頁面清單。

   重新定位畫素標籤必須是登陸頁面上的最後一個動作。

   廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

## 刪除重新定位畫素

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 將游標停留在畫素名稱上，然後按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

## 重新定位畫素設定 {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]：**&#x200B;畫素的名稱。 **注意：**&#x200B;畫素標籤包含畫素ID (`pxId=<ID>`)，而非畫素名稱。

**[!UICONTROL Advertiser]：** （現有畫素為唯讀）追蹤畫素的廣告商。

**[!UICONTROL Attribute 1]：**&#x200B;要包含在畫素標籤中的屬性，例如「SKU」、「category」、「size」或頁面的其他屬性，或頁面上顯示的產品。 在插入相關網頁之前，請在畫素標籤中指定屬性值。

將廣告體驗目標定位給曝光於畫素的使用者時，目標定位設定會指定必須呈現的屬性值，才能顯示創意。

**[!UICONTROL Attribute 2]**、**[!UICONTROL Attribute 3]**、**[!UICONTROL Attribute 4]**、**[!UICONTROL Attribute 5]：** （選用）要包含在畫素標籤中的其他屬性。 在您將畫素標籤插入相關網頁之前，請為畫素標籤中的每個其他屬性指定值。

將廣告體驗目標定位給曝光於畫素的使用者時，目標定位設定會指定必須呈現的屬性值，才能顯示創意。

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]：** (Beta功能；僅限新畫素；選用)要追蹤的畫素標籤通用ID型別：

* *[!UICONTROL ID5]：*&#x200B;畫素標籤追蹤[!DNL ID5]個ID。 對於傳遞到通用ID的曝光，不會產生任何費用。

* *[!UICONTROL Ramp ID]：*&#x200B;畫素標籤追蹤[!DNL Ramp IDs]。 對於傳遞到通用ID的曝光，不會產生任何費用。

若要使用此功能，您或DSP帳戶中的其他使用者必須先接受使用通用ID的服務合約條款，才能將通用ID用於新ID型別。 若客戶擁有受管理的服務合約，您的Adobe客戶團隊將代表貴組織取得您的同意並接受條款。 若要閱讀條款，請按一下&#x200B;**[!UICONTROL Terms of Service]**。 若要接受條款，請捲動至條款底部，然後按一下&#x200B;**[!UICONTROL Accept]**。

>[!MORELIKETHIS]
>
>* [目標廣告體驗設定](/help/creative/experiences/experience-settings-targeting.md)
>* [關於廣告體驗](/help/creative/experiences/experience-about.md)
