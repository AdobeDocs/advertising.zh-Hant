---
title: 關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式
description: 瞭解支援廣告網路的點選追蹤格式。
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式

使用Adobe Advertising轉換追蹤服務的廣告帳戶和促銷活動的追蹤範本、登入頁面尾碼（最終URL尾碼）和目的地URL格式如下：

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

其中：

* `http://pixel.everesttech.net`將使用者重新導向至Adobe Advertising畫素伺服器。

* `<advertiser_ID>`是Adobe Advertising內指派給廣告商的不重複使用者ID變數。

* `<token passing parameter>`是下列其中一個專案的變數：

   * `cq?`或`rq`表示已啟用權杖傳遞。

   * `c?`或`r`表示已停用Token傳遞。

* `<ad network ID>`是指定廣告網路數值ID的變數，例如[!DNL Google Ads]的&#x200B;*3*、[!DNL Microsoft Advertising]的&#x200B;*10*、[!DNL Meta]的&#x200B;*45*、[!DNL Yahoo! Display Network]的&#x200B;*86*、[!DNL Naver]的&#x200B;*87*、[!DNL Baidu]的&#x200B;*88*、[!DNL Yandex]的&#x200B;*90*、*94*&#x200B;的[!DNL Yahoo! Japan Ads] [!DNL Yahoo Native]的&#x200B;*105*（已棄用）或[!DNL Pinterest]的&#x200B;*106*（已棄用）。

* `<tracking ID>`是系統產生的追蹤ID字串的變數，可識別帳戶中唯一的關鍵字、廣告或位置。 字串會因廣告網路而異。

* `<the landing page>`是變數，代表一般使用者在網站上導向的URL。 對於具有目的地URL的帳戶，此值是一個URL。 對於具有追蹤範本的帳戶，此值是代表最終URL的引數（例如`{lpurl}`）。

請參閱個別頁面，指出[[!DNL Baidu] 格式](formats-click-tracking-baidu.md)、[[!DNL Google Ads] 格式](formats-click-tracking-google.md)、[[!DNL Microsoft Advertising] 格式](formats-click-tracking-microsoft.md)、[[!DNL Naver] 格式](formats-click-tracking-naver.md)、[[!DNL Yahoo! Display Network] 格式](formats-click-tracking-yahoo-display-network.md)、[[!DNL Yahoo! Japan Ads] 格式](formats-click-tracking-yahoo-japan.md)和[[!DNL Yandex] 格式](formats-click-tracking-yandex.md)。

>[!MORELIKETHIS]
>
>* [於 [!DNL Baidu]](formats-click-tracking-baidu.md)贊助廣告的點選追蹤格式
>*  [!DNL Google Ads]](formats-click-tracking-google.md)的[點選追蹤格式
>*  [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)的[點選追蹤格式
>* [於 [!DNL Naver]](formats-click-tracking-naver.md)贊助廣告的點選追蹤格式
>* [於 [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)贊助廣告的點選追蹤格式
>* [於 [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)贊助廣告的點選追蹤格式
>* [於 [!DNL Yandex]](formats-click-tracking-yandex.md)贊助廣告的點選追蹤格式
