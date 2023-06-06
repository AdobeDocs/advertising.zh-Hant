---
title: 何時及如何依廣告網路和物件產生點選追蹤URL
description: 瞭解點選追蹤URL何時自動新增，以及何時以及如何為各種促銷活動元件手動新增。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 何時及如何依廣告網路和物件產生點選追蹤URL

下表說明如何產生各種促銷活動元件的點選追蹤URL。

| 廣告網路 | 元件 | 如何產生點選追蹤URL |
| ---- | ---- | ---- |
| [!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] | <ul><li>文字廣告</li><li>關鍵字</li><li>([!DNL Google Ads] content campaigns) placement</li><li>([!DNL Google Advertising] 和 [!DNL Advertising])網站連結</li></ul> | 當作用中行銷活動的追蹤設定包含選項時»[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]「 」（在促銷活動層級設定或繼承自帳戶設定），您不需要產生廣告群組元件的追蹤URL。 Search、Social和Commerce每次與廣告網路同步時，都會自動建立以下型別的追蹤URL並將其上傳到廣告網路： a) （具有最終URL的帳戶）追蹤範本的搜尋、Social和Commerce追蹤引數以及附加至最終URL的相同引數， b) （具有目的地URL的帳戶）內嵌搜尋、Social和Commerce追蹤程式碼的新目的地URL，以及c) (Google Ads和Microsoft Advertising帳戶)登陸頁面尾碼（最終URL尾碼）引數。<br><br>如果 [!UICONTROL Auto Upload] 選項停用，則您可透過下列任何方式為元件產生追蹤URL：<ul><li>([!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Ads]、和 [!DNL Yandex])當您從摘要檔案張貼廣告時，請選取 [!UICONTROL Generate Tracking URLs] 選項。 您可以選擇在張貼至廣告網路之前，驗證任何大量表單檔案中的追蹤範本欄位。</li><li>下載、上傳或張貼包含元件的大量表單檔案時，請選取 [!UICONTROL Generate Tracking URLs] 選項。 針對具有目的地URL的帳戶，您可以選擇在將檔案張貼至廣告網路之前，驗證基本URL/最終URL欄位欄位</li><li>使用 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md) 以產生追蹤URL並手動將其新增至適當的 [!UICONTROL Tracking Template] 或 [!UICONTROL Base URL] 欄位。 <b>注意：</b> 您產生的追蹤範本不包含帳戶或行銷活動設定中指定的任何其他追蹤引數。<ul><li>Google帳戶)前往 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，將熒幕上的值複製到適當的 [!UICONTROL Tracking Template] 欄位，並手動將整個追蹤字串新增至元件設定。 您必須新增 [!DNL Google Ads] [!DNL ValueTrack] 後面最終URL的引數 `&url=` 引數(例如 `{lpurl}`)。 如需清單： [!DNL ValueTrack] 引數可指出追蹤範本中的最終URL，請參閱[[!DNL Google Ads] documentation]9https://support.google.com/google-ads/answer/2375447。</li><li>（具有最終URL的其他帳戶）使用產生追蹤URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，並手動將整個追蹤字串新增至元件設定。 您必須在之後為最終URL新增引數 `&url=` 引數(例如 `{lpurl}`)。 對象 [!DNL Yahoo! Japan Ads] 帳戶，使用引數 `{lpurl}`. 如需清單： [!DNL Microsoft Advertising] 指示追蹤範本中最終URL的引數，請參閱 [Microsoft廣告檔案](https://help.bingads.microsoft.com/#apex/3/en/56799).</li><li>（具有目的地URL的帳戶）使用產生追蹤URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，並手動將追蹤URL新增至適當的 [!UICONTROL Base URL] 欄位。</li></ul></li></ul><b>附註：</b><br><br><ul><li>（具有最終URL的帳戶）使用最精細層級的追蹤範本（例如，關鍵字層級的追蹤範本會覆寫帳戶、行銷活動和廣告群組層級的範本，而關鍵字和版位的追蹤範本會覆寫關聯廣告的追蹤範本）。</li><li>Adobe廣告會將網站連結的點按次數和產生的收入，對應至包含Sitelink之廣告的相關關鍵字，而非個別貼現。 請參閱「[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md).」</li></ul><b>秘訣：</b> （具有最終URL的帳戶）如果您只在所需的最高層級建立追蹤範本（例如，帳戶或促銷活動層級追蹤範本），以將相同的追蹤套用至帳戶或促銷活動中的所有實體，則最容易管理追蹤。 |
| [!DNL Google Ads] | <ul><li>位置延伸</li><li>電話分機</li></ul> | 不適用 |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | 產品廣告 | <ul><li>[!DNL Microsoft Merchant Center] 帳戶：手動為您中的每個產品建立追蹤URL。 [!DNL Microsoft Merchant Center] 帳戶使用 [購物廣告的追蹤範本格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)，並手動將其新增至 [!UICONTROL Tracking Template] 「帳戶」、「促銷活動」或「產品群組」設定中的欄位。<br><br>或者，您也可以將追蹤URL新增至 [!DNL Microsoft Merchant Center account]. 若要這麼做，請包含追蹤URL，連同「」中的值[!DNL link]「或」[!DNL mobile_link]「 」欄位（如果適用） [自訂欄»[!DNL bingads_redirect]」在產品資訊源中](https://help.ads.microsoft.com/#apex/3/en/51084). 「」中的值[!DNL bingads_redirect]「欄位會取代」中的值[!DNL link]「和」[!DNL mobile_link]「欄位。 使用此方法產生的URL不包含帳戶設定中指定的任何追蹤引數。<br><br><b>注意：</b> 同步期間自動上傳追蹤的帳戶層級和促銷活動層級功能，不會為新專案產生追蹤 [!DNL Microsoft Advertising] 產品群組。 因應措施是在您上傳或張貼大量表單時產生追蹤。</li><li>[!DNL Google Merchant Center] 帳戶：使用產生追蹤URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，並手動將其新增至 [!UICONTROL Tracking Template] 帳戶、促銷活動或產品群組設定中的欄位。</li></ul> |
| [!DNL Naver] | 關鍵字 | 您可以透過以下方式設定所有廣告的點選追蹤 [大量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md). 或者，您也可以手動產生廣告的追蹤URL，並使用廣告網路的編輯器手動將其新增至廣告設定。 請參閱「[實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).」 |
| [!DNL Yahoo! Display Network] | 文字和顯示廣告 | 當作用中行銷活動的追蹤設定包含選項時»[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]「 （在促銷活動層級設定或繼承自帳戶設定），您不需要產生廣告的追蹤URL。 搜尋、Social和Commerce會在每次與廣告網路同步時，自動建立內嵌追蹤程式碼的新目的地URL並將其上傳到廣告網路。<br><br>如果 [!UICONTROL Auto Upload] 選項停用，然後您可以使用 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，並使用廣告網路的編輯器手動將其新增至廣告設定。 |

>[!MORELIKETHIS]
>
>* [使用「追蹤URL」工具產生搜尋、社交和商務點選追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [關於使用大量表單管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)
>* [設定Cookie型點選追蹤](/help/search-social-commerce/tracking/click-tracking-set-up.md)

