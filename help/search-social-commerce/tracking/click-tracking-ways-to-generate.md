---
title: 何時及如何依廣告網路和物件產生點選追蹤URL
description: 瞭解點選追蹤URL何時自動新增，以及何時以及如何為各種促銷活動元件手動新增。
exl-id: 896de0c1-75ed-450c-b995-893f1a63e5ce
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 何時及如何依廣告網路和物件產生點選追蹤URL

下表說明如何為各種促銷活動元件產生點選追蹤URL。

| 廣告網路 | 元件 | 如何產生點選追蹤URL |
| ---- | ---- | ---- |
| [!DNL Baidu]、[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]和[!DNL Yandex] | <ul><li>文字廣告</li><li>關鍵字</li><li>（[!DNL Google Ads]個內容行銷活動）版位</li><li>（[!DNL Google Advertising]和[!DNL Advertising]）網站連結</li></ul> | 當作用中行銷活動的追蹤設定包含選項&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot; （在行銷活動層級設定或繼承自帳戶設定）時，您不需要產生廣告群組元件的追蹤URL。 搜尋、Social和Commerce每次與廣告網路同步時，都會自動建立下列型別的追蹤URL並上傳至廣告網路： a) （具有最終URL的帳戶）用於追蹤範本的搜尋、Social和Commerce追蹤引數以及附加至最終URL的相同引數， b) （具有目的地URL的帳戶）內嵌搜尋、Social和Commerce追蹤程式碼的新目的地URL，以及c) （[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶）登陸頁面尾碼（最終URL尾碼）引數。<br><br>如果[!UICONTROL Auto Upload]選項已停用，則您可以透過下列任何方式產生元件的追蹤URL：<ul><li>（[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Ads]和[!DNL Yandex]）當您從摘要檔案張貼廣告時，請選取[!UICONTROL Generate Tracking URLs]選項。 您可以選擇在張貼至廣告網路之前，驗證任何大量表單檔案中的追蹤範本欄位。</li><li>下載、上傳或張貼包含元件的大量表單檔案時，請選取[!UICONTROL Generate Tracking URLs]選項。 針對具有目的地URL的帳戶，您可以選擇在將檔案張貼至廣告網路之前，驗證基本URL/最終URL欄位欄位</li><li>使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，並手動將其新增至適當的[!UICONTROL Tracking Template]或[!UICONTROL Base URL]欄位。 <b>注意：</b>您產生的追蹤範本不包含帳戶或行銷活動設定中指定的任何其他追蹤引數。<ul><li>Google帳戶)移至[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，複製適當[!UICONTROL Tracking Template]欄位中的熒幕上值，並手動將整個追蹤字串新增至元件設定。 您必須在`&url=`引數（例如`{lpurl}`）之後為最終URL新增[!DNL Google Ads] [!DNL ValueTrack]引數。 如需表示追蹤範本中最終URL的[!DNL ValueTrack]引數清單，請參閱[[!DNL Google Ads]檔案]9https://support.google.com/google-ads/answer/2375447中「可用的[!DNL ValueTrack]引數」一節中的「僅限追蹤範本」引數。</li><li>（具有最終URL的其他帳戶）使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，並手動將整個追蹤字串新增至元件設定。 您必須在`&url=`引數（例如`{lpurl}`）之後新增最終URL的引數。 對於[!DNL Yahoo! Japan Ads]帳戶，請使用引數`{lpurl}`。 如需表示追蹤範本中最終URL的[!DNL Microsoft Advertising]引數清單，請參閱[[!DNL Microsoft Advertising] 檔案](https://help.bingads.microsoft.com/#apex/3/en/56799)。</li><li>（具有目的地URL的帳戶）使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，並在適當的[!UICONTROL Base URL]欄位中手動新增追蹤URL。</li></ul></li></ul><b>附註：</b><br><br><ul><li>（具有最終URL的帳戶）會使用最精細層級的追蹤範本（例如，關鍵字層級的追蹤範本會覆寫帳戶、行銷活動和廣告群組層級的範本，而關鍵字和刊登版位的追蹤範本會覆寫關聯廣告的追蹤範本）。</li><li>Adobe Advertising會將網站連結的點按次數和產生的收入，對應至包含Sitelink之廣告的相關關鍵字，而非個別對應至該廣告。 請參閱&quot;[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)&quot;。</li></ul><b>秘訣：</b> （具有最終URL的帳戶）如果您只在所需的最高層級建立追蹤範本，例如帳戶或促銷活動層級的追蹤範本，以將相同的追蹤套用至帳戶或促銷活動中的所有實體，則最容易管理追蹤。 |
| [!DNL Google Ads] | 電話分機 | 不適用 |
| [!DNL Google Ads]，[!DNL Microsoft Advertising] | 產品廣告 | <ul><li>[!DNL Microsoft Merchant Center]帳戶：使用[購物廣告的追蹤範本格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)，手動建立[!DNL Microsoft Merchant Center]帳戶中每個產品的追蹤URL，並手動將其新增至帳戶、行銷活動或產品群組設定中的[!UICONTROL Tracking Template]欄位。<br><br>或者，您也可以將追蹤URL新增至[!DNL Microsoft Merchant Center account]內的產品資料。 若要這麼做，請在產品摘要[&#128279;](https://help.ads.microsoft.com/#apex/3/en/51084)內的自訂欄「[!DNL bingads_redirect]」中，加入追蹤URL以及適當的「[!DNL link]」或「[!DNL mobile_link]」欄位中的值。 「[!DNL bingads_redirect]」欄位中的值會取代「[!DNL link]」和「[!DNL mobile_link]」欄位中的值。 使用此方法產生的URL不包含帳戶設定中指定的任何追蹤引數。<br><br><b>注意：</b>帳戶層級和促銷活動層級在同步期間自動上傳追蹤的功能，不會產生新[!DNL Microsoft Advertising]產品群組的追蹤。 因應措施是在您上傳或張貼大量表單時產生追蹤。</li><li>[!DNL Google Merchant Center]帳戶：使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，並手動將其新增至帳戶、行銷活動或產品群組設定中的[!UICONTROL Tracking Template]欄位。</li></ul> |
| [!DNL Naver] | 關鍵字 | 您可以透過[大量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)為所有廣告設定點選追蹤。 或者，您也可以手動產生廣告的追蹤URL，並使用廣告網路的編輯器手動將其新增至廣告設定。 請參閱&quot;[實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;。 |
| [!DNL Yahoo! Display Network] | 文字和顯示廣告 | 當作用中行銷活動的追蹤設定包含選項&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot; （在行銷活動層級設定或繼承自帳戶設定）時，您不需要產生廣告的追蹤URL。 搜尋、Social和Commerce會在每次與廣告網路同步時，自動建立並上傳內嵌追蹤程式碼的新目的地URL至廣告網路。<br><br>如果[!UICONTROL Auto Upload]選項已停用，則您可以使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，並使用廣告網路的編輯器手動將其新增至廣告設定。 |

>[!MORELIKETHIS]
>
>* [使用「追蹤URL」工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生搜尋、社交和Commerce點選追蹤URL
>* [關於使用大量表單管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)
>* [設定Cookie型點選追蹤](/help/search-social-commerce/tracking/click-tracking-set-up.md)
