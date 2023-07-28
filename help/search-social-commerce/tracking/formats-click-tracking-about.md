---
title: 關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式
description: 瞭解支援廣告網路的點選追蹤格式。
exl-id: 12148caf-fde6-4ac2-b8b4-222409895dd7
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# 關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式

使用Adobe Advertising轉換追蹤服務的廣告帳戶和促銷活動的追蹤範本、登入頁面尾碼（最終URL尾碼）和目的地URL格式如下：

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

其中：

* `http://pixel.everesttech.net` 將使用者重新導向至Adobe Advertising畫素伺服器。

* `<advertiser_ID>` 是指派給Adobe Advertising內廣告商的不重複使用者ID變數。

* `<token passing parameter>` 是下列其中一項的變數：

   * `cq?` 或 `rq` 表示已啟用權杖傳遞。

   * `c?` 或 `r` 表示已停用Token傳遞。

* `<ad network ID>` 是指定廣告網路數值ID的變數，例如 *3* 的 [!DNL Google Ads]， *10* 的 [!DNL Microsoft Advertising]， *45* 的 [!DNL Meta]， *86* 的 [!DNL Yahoo! Display Network]， *87* 的 [!DNL Naver]， *88* 的 [!DNL Baidu]， *90* 的 [!DNL Yandex]， *94* 的 [!DNL Yahoo! Japan Ads]， *105* 的 [!DNL Yahoo Native] （已棄用），或 *106* 的 [!DNL Pinterest] （已棄用）。

* `<tracking ID>` 是系統產生的追蹤ID字串的變數，可識別帳戶中唯一的關鍵字、廣告或位置。 字串會因廣告網路而異。

* `<the landing page>` 是變數，代表一般使用者要導向的網站URL。 對於具有目的地URL的帳戶，此值是一個URL。 對於具有追蹤範本的帳戶，此值為引數(例如 `{lpurl}`)代表最終URL。

請參閱個別頁面，指出 [[!DNL Baidu] 格式](formats-click-tracking-baidu.md)， [[!DNL Google Ads] 格式](formats-click-tracking-google.md)， [[!DNL Microsoft Advertising] 格式](formats-click-tracking-microsoft.md)， [[!DNL Naver] 格式](formats-click-tracking-naver.md)， [[!DNL Yahoo! Display Network] 格式](formats-click-tracking-yahoo-display-network.md)， [[!DNL Yahoo! Japan Ads] 格式](formats-click-tracking-yahoo-japan.md)、和 [[!DNL Yandex] 格式](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [上的贊助廣告的點選追蹤格式 [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [的點選追蹤格式 [!DNL Google Ads]](formats-click-tracking-google.md)
>* [的點選追蹤格式 [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [上的贊助廣告的點選追蹤格式 [!DNL Naver]](formats-click-tracking-naver.md)
>* [上的贊助廣告的點選追蹤格式 [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [上的贊助廣告的點選追蹤格式 [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [上的贊助廣告的點選追蹤格式 [!DNL Yandex]](formats-click-tracking-yandex.md)
