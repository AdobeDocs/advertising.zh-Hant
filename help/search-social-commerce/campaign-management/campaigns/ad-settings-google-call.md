---
title: '"[!DNL Google Ads] 僅限通話的廣告設定」'
description: 參考設定 [!DNL Google Ads] 僅限通話的廣告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] 僅限通話的廣告設定

您可以為使用搜尋網路的行銷活動建立僅限來電的文字廣告。

搜尋、Social和Commerce會使用帳戶層級的登陸頁面尾碼和追蹤範本來追蹤僅限來電的廣告，但您可以選擇在中覆寫廣告層級的帳戶層級追蹤 [!DNL Google Ads] 經理。

請參閱 [!DNL Google Ads] 說明 [每個帳戶的廣告限制](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]：** 企業的名稱。 長度上限為25個字元或12個雙位元組字元。

**[!UICONTROL Country]：** （選用）企業所在的國家/地區。

**[!UICONTROL Phone Number]：** 公司的電話號碼。 範例： (124) 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1]， [!UICONTROL Description 2]：** 廣告內文的第一行和第二行。 每行的長度上限為35個字元或17個雙位元組字元。

關鍵字替代語法不會計入最大長度。 例如，「`{Description1: Free Account Analysis!}`「 」會視為22個字元（只有「免費帳戶分析\！」部分）。

>[!NOTE]
>
>說明欄位不能包含電話號碼。

**[!UICONTROL Display URL]：** 廣告中顯示的URL。 顯示URL必須符合與您的企業相關聯的網域，但廣告不會將人們傳送至登陸頁面。

長度上限為35個單位元組或17個雙位元組字元。 關鍵字替代語法不會計入最大長度。 例如，「`{DisplayURL: example.com}`「」會視為11個字元（只有「example.com」部分）。

**[!UICONTROL Verification URL]：** （選用）將廣告電話號碼顯示為文字的網頁，以便 [!DNL Google Ads] 可以驗證電話號碼是否有效。 其網域必須與廣告的顯示URL相同。

**[!UICONTROL Is Tracked]：** 啟用呼叫追蹤和僅限呼叫的轉換。

**[!UICONTROL Count calls as phone call conversions]：** (當&quot;[!UICONTROL Is Tracked]&quot;已選取；選擇性)指定時，會將廣告產生的所有來電歸因於特定型別的電話轉換。 否則， [!DNL Google Ads] 建立名為「」的預設轉換動作[!UICONTROL Calls from ads]&quot;一旦它記錄來自您的轉寄號碼的至少一次轉換，然後將其呼叫歸因於它。

**[!UICONTROL Count Action]：** (當&quot;[!UICONTROL Count calls as phone call conversions]」已選取；選用)歸因呼叫的現有轉換動作。

您可以在中建立和管理轉換動作 [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [關於廣告](ad-about.md)
>* [管理廣告](ad-manage.md)
>* [[!DNL Google Ads] 擴展的動態搜尋廣告設定](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 回應式搜尋廣告設定](ad-settings-google-rsa.md)

