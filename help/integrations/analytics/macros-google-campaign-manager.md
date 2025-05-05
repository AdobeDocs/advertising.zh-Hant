---
title: 將 [!DNL Analytics for Advertising] 巨集附加至 [!DNL Google Campaign Manager 360] 廣告標籤
description: 瞭解為何以及如何將 [!DNL Analytics for Advertising] 巨集新增至您的 [!DNL Google Campaign Manager 360] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 將[!DNL Analytics for Advertising]巨集附加至[!DNL Google Campaign Manager 360]廣告標籤

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*僅適用於Advertising DSP*

如果您針對Advertising DSP廣告使用[!DNL Google Campaign Manager 360]中的廣告標籤，請使用[`%p`巨集](https://support.google.com/campaignmanager/table/6096962)將[!DNL Analytics for Advertising]引數附加至您的登陸頁面URL。 引數會在登陸頁面URL中記錄AMO ID (`s_kwcid`)和`ef_id`查詢字串引數，允許Adobe Advertising將廣告的點選資料傳送至Adobe Analytics。

針對下列型別的[!DNL Analytics for Advertising]實作，[!DNL Campaign Manager 360]顯示廣告和視訊廣告使用巨集：

* **在其網站上實作[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript程式碼的廣告商**： JavaScript程式碼已記錄AMO ID (`s_kwcid`)和`ef_id`查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤功能，加入點按式轉換。 最佳實務是將下列區段中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是僅在Cookie仍可用時用於點選追蹤的解決方案。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用[!DNL Analytics for Advertising] JavaScript程式碼，而是僅仰賴[!DNL Analytics]伺服器端轉送來取得點進資料的廣告商** （不含任何檢視資料）：若要報告您透過Adobe Advertising購買的廣告所驅動的站上點進活動，必須有下列巨集。

## 將巨集附加至您的[!DNL Google Campaign Manager 360]廣告

在[!DNL Google Campaign Manager 360]內，將下列引數附加至每個顯示廣告和視訊廣告的登陸頁面URL： `%pamo=!;`

您可以透過數種方式指定登入頁面URL。 以下小節包含每個選項的指示。

以下範例為尾碼格式化的登入頁面URL。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* 如果登陸頁面URL包含雜湊符號(#)，這是不常見的情況，請將`amo`引數放在雜湊符號之前。
>* 如果未在`amo`引數後面包含其他引數，則在其後面新增引數（例如&amp;a=b）。 範例： `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 設定廣告商層級登陸頁面URL尾碼

1. 請參閱[指示以開啟廣告商屬性](https://support.google.com/campaignmanager/answer/2829344)。
1. 在[!UICONTROL Landing page URL suffix]設定中，在[!UICONTROL URL suffix]欄位中包含`%pamo!;`。

### 設定行銷活動層級登陸頁面URL尾碼

1. 請參閱[指示以開啟行銷活動屬性](https://support.google.com/campaignmanager/answer/2838056#set)。
1. 在[!UICONTROL Landing page URL suffix]設定中，在[!UICONTROL URL suffix]欄位中包含`%pamo!;`。

### 設定創意層級登陸頁面URL尾碼

1. 開啟創意屬性。
1. 在[!UICONTROL Click tags]設定中，在點選標籤的[!UICONTROL Landing page]欄中加入`%pamo!;`。

## 如何在DSP中展開[!DNL Analytics for Advertising]巨集

在DSP中，當您建立包含[!DNL Analytics for Advertising]引數(`amo`)的廣告時，`ef_id`和`s_kwcid`巨集會自動附加至點選URL。 最佳實務是檢查DSP中的標籤，以確保`ef_id`和`s_kwcid`巨集存在。

以下是[!DNL Google Campaign Manager 360] [ins標籤](https://support.google.com/campaignmanager/answer/6080468)在DSP中顯示的範例。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

當使用者按一下廣告時，[!DNL Google Campaign Manager 360]會在URL尾碼中看到`%pamo`，並動態地將`amo`引數的值插入URL。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe AdvertisingID已由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](macros-flashtalking.md)
