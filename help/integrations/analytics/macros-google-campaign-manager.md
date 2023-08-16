---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤
description: 瞭解新增原因和方法 [!DNL Analytics for Advertising] 將巨集新增至 [!DNL Google Campaign Manager 360] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

*僅適用於Advertising DSP*

如果您使用的廣告標籤來自 [!DNL Google Campaign Manager 360] 若為您的Advertising DSP廣告，請附加 [!DNL Analytics for Advertising] 引數至您的登陸頁面URL，使用 [`%p` 巨集](https://support.google.com/campaignmanager/table/6096962). 引數會記錄AMO ID (`s_kwcid`)和 `ef_id` 登陸頁面URL中的查詢字串引數，可讓Adobe Advertising將廣告的點選資料傳送至Adobe Analytics。

將巨集用於 [!DNL Campaign Manager 360] 下列型別的顯示廣告和視訊廣告 [!DNL Analytics for Advertising] 實作：

* **使用「 」的廣告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**：JavaScript程式碼已記錄AMO ID (`s_kwcid`)和 `ef_id` 查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤功能，加入點按式轉換。 最佳作法是將下列章節中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是一種解決方案，僅適用於Cookie仍可用時的點選追蹤。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用的廣告商 [!DNL Analytics for Advertising] JavaScript程式碼，並仰賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （不含任何瀏覽資料）：報告您透過Adobe Advertising購買的廣告所驅動的站上點選活動時，需要下列巨集。

## 將巨集附加至 [!DNL Google Campaign Manager 360] 廣告

範圍 [!DNL Google Campaign Manager 360]，將下列引數附加至每個顯示廣告和視訊廣告的登陸頁面URL： `%pamo=!;`

您可以透過數種方式指定登入頁面URL。 以下小節包含每個選項的指示。

以下範例為尾碼格式化的登入頁面URL。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* 如果登陸頁面URL包含雜湊符號(#)（這種情況不常見），請放置 `amo` 雜湊符號前的引數。
>* 如果之後未包含其他引數 `amo` 引數，然後在其後面新增引數（例如&amp;a=b）。 範例： `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 設定廣告商層級登陸頁面URL尾碼

1. 請參閱 [開啟廣告商屬性的指示](https://support.google.com/campaignmanager/answer/2829344).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定行銷活動層級登陸頁面URL尾碼

1. 請參閱 [開啟行銷活動屬性的指示](https://support.google.com/campaignmanager/answer/2838056#set).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定創意層級登陸頁面URL尾碼

1. 開啟創意屬性。
1. 在 [!UICONTROL Click tags] 設定，包含 `%pamo!;` 在 [!UICONTROL Landing page] 點按標籤的欄。

## 如何 [!DNL Analytics for Advertising] 在DSP中展開巨集

在DSP中，當您建立包含 [!DNL Analytics for Advertising] 引數(`amo`)， `ef_id` 和 `s_kwcid` 巨集會自動附加至按一下URL。 最佳實務是檢查DSP中的標籤，以確保 `ef_id` 和 `s_kwcid` 有巨集存在。

以下範例為 [!DNL Google Campaign Manager 360] [ins標籤](https://support.google.com/campaignmanager/answer/6080468) 它在DSP中顯示的樣子。

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

當使用者點選廣告， [!DNL Google Campaign Manager 360] 看到 `%pamo` （在URL尾碼中）並動態插入 `amo` 引數放入URL中。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](macros-flashtalking.md)
