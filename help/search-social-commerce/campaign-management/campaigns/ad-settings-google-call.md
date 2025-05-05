---
title: '[!DNL Google Ads]僅呼叫廣告設定'
description: 參考 [!DNL Google Ads] 僅限通話廣告的設定。
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads]僅限通話的廣告設定

您可以為使用搜尋網路的行銷活動建立僅限來電的文字廣告。

搜尋、Social和Commerce使用帳戶層級的登陸頁面尾碼和追蹤範本來追蹤僅限來電的廣告，但您可以選擇在[!DNL Google Ads]管理員內覆寫廣告層級的帳戶層級追蹤。

請參閱[!DNL Google Ads]說明，瞭解每個帳戶[&#128279;](https://support.google.com/google-ads/answer/6372658?hl=en)的廣告限制。

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]：**&#x200B;企業的名稱。 長度上限為25個字元或12個雙位元組字元。

**[!UICONTROL Country]：** （選擇性）企業所在的國家/地區。

**[!UICONTROL Phone Number]：**&#x200B;公司的電話號碼。 範例：(124) 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1]，[!UICONTROL Description 2]：**&#x200B;廣告內文的第一行和第二行。 每行的長度上限為35個字元或17個雙位元組字元。

關鍵字替代語法不會計入最大長度。 例如，「`{Description1: Free Account Analysis!}`」會視為22個字元（只有「Free Account Analysis\！」部分）。

>[!NOTE]
>
>說明欄位不得包含電話號碼。

**[!UICONTROL Display URL]：**&#x200B;廣告中顯示的URL。 顯示URL必須符合與您的企業相關聯的網域，但廣告不會將人們傳送至登陸頁面。

長度上限為35個單位元組或17個雙位元組字元。 關鍵字替代語法不會計入最大長度。 例如，「`{DisplayURL: example.com}`」會視為11個字元（只有「example.com」部分）。

**[!UICONTROL Verification URL]：** （選用）廣告電話號碼顯示為文字的網頁，以便[!DNL Google Ads]可以驗證電話號碼是否有效。 其網域必須與廣告的顯示網址相同。

**[!UICONTROL Is Tracked]：**&#x200B;啟用呼叫追蹤和僅限呼叫的轉換。

**[!UICONTROL Count calls as phone call conversions]：** （選取「[!UICONTROL Is Tracked]」時；選擇性）將廣告產生的所有呼叫歸因於特定型別的電話轉換（若已指定）。 否則，[!DNL Google Ads]會在您轉寄號碼中記錄至少一個轉換之後，建立名為「[!UICONTROL Calls from ads]」的預設轉換動作，然後將其呼叫歸因於它。

**[!UICONTROL Count Action]：** （選取「[!UICONTROL Count calls as phone call conversions]」時；選擇性）呼叫歸因的現有轉換動作。

您可以在[!DNL Google Ads]內建立和管理轉換動作。

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [關於廣告](ad-about.md)
>* [管理廣告](ad-manage.md)
>* [[!DNL Google Ads] 延展的動態搜尋廣告設定](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 回應式搜尋廣告設定](ad-settings-google-rsa.md)
