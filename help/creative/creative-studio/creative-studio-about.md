---
title: 關於Advertising Creative中的Creative Studio
description: 瞭解如何使用Creative Studio在Adobe Advertising Creative中建置AI輔助廣告內容。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 811
ht-degree: 0%

---

# 關於[!DNL Advertising Creative]中的[!UICONTROL Creative Studio]

*Beta功能*

[!UICONTROL Creative Studio]是AI輔助環境，您可以在單一工作階段中跨多種格式建置、調整大小和調整顯示廣告。 您透過自然語言聊天介面與AI互動，以產生和修改廣告內容 — 內容欄位不需要手動設計工作。

## Workspace概觀

[!UICONTROL Creative Studio]已組織為三個索引標籤：

**[!UICONTROL Creatives]** — 廣告建立的起點。 顯示從Creative Studio產生的現有創意內容，並將其整理到可收合的創意檔案庫中。 您可以在此處從範本產生標準顯示廣告、從目錄資料建立動態顯示創意，以及管理現有創意（編輯、產生廣告變化、預覽、複製、下載、刪除、QA和檢閱變更記錄）。 請參閱「在Creative Studio中管理標準廣告[&#128279;](creative-studio-manage-standard-ads.md)」和「在Creative Studio中管理動態廣告[&#128279;](creative-studio-manage-dynamic-ads.md)」。

**[!UICONTROL Templates]** — 顯示您的帳戶可用的所有顯示和視訊廣告範本，並依來源（全部、系統範本、使用者範本）、狀態和廣告格式進行篩選。 您可以預覽、收藏、加上標籤、下載和刪除範本，或直接從現有的顯示廣告範本啟動廣告產生工作階段。 請參閱[在Creative Studio中管理範本](creative-studio-manage-templates.md)。

**[!UICONTROL Assets]** — 儲存範本中使用的影像、視訊和音訊檔案，並可在廣告產生工作階段期間附加至AI聊天訊息。 您可以搜尋、篩選、上傳、下載和刪除資產。 請參閱[在Creative Studio中管理資產](creative-studio-manage-assets.md)。

## 主要功能

* **AI內容產生：**&#x200B;使用&#x200B;**[!UICONTROL Ad Variations Generator]**&#x200B;透過自然語言聊天介面產生廣告概念和變體。 AI助理可以產生標題、副標題、CTA、正文和背景影像變化，並可在相同工作階段中建立新的大小範本。 每個工作階段最多可啟用10個概念。

* **顯示廣告和視訊廣告支援：**&#x200B;建立和管理顯示廣告範本和視訊廣告範本。 建立範本時，請選擇&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**&#x200B;以符合您的行銷活動格式。

* **HTML5範本上傳：**&#x200B;將現有的HTML5廣告範本上傳為ZIP檔，以匯入範本。 **[!UICONTROL Import Templates]**&#x200B;對話方塊可讓您在匯入之前指派廣告商和範本名稱。

* **多重大小支援：**&#x200B;只要一步即可將廣告大小調整為IAB標準維度。 AI會自動調整每個格式的內容放置和大小，而畫布控制項（放大/縮小、適合熒幕、重播動畫）可協助您檢視每個大小。

* **品牌一致輸出：**&#x200B;套用您的[品牌設定檔](/help/creative/brands/brand-manage.md)時，AI會使用您品牌的圖志、調色盤、語音准則、影像標準和頻道准則，讓產生的內容保持在品牌上。

* **資產庫存取：**&#x200B;從資產庫中選取，在內容產生期間保持視覺內容可用，將影像和其他資產直接附加到AI聊天訊息。

* **摘要整合：**&#x200B;對於動態廣告行銷活動，請連線產品或內容目錄以大規模產生廣告，然後使用AI代理程式來篩選、預覽和品質檢查目錄產生的廣告組合。

* **範本組織：**&#x200B;將範本標示為我的最愛、套用標籤，以及依狀態、格式或來源篩選，讓您的範本資料庫保持井然有序。

## 廣告建立工作流程

| 工作流程 | 使用時機 |
| --- | --- |
| [從範本產生標準廣告](creative-studio-manage-standard-ads.md) | 選取顯示或視訊範本，並使用[!UICONTROL Ad Variations Generator]建立AI產生的內容變化。 當範本已存在且您想要AI輔助產生內容時為最佳狀態。 |
| [管理動態創意內容](creative-studio-manage-dynamic-ads.md) | 將產品或內容目錄連線到範本，將目錄欄位對應到範本元素，然後使用AI代理程式來預覽和QA所有產生的廣告組合。 最適合目錄導向的大型行銷活動。 |
| 建立新範本 | 從空白畫布開始，建立顯示區或視訊範本。 當沒有符合您需求的現有範本時為最佳選擇。 |
| 上傳HTML5範本 | 匯入一或多個ZIP檔案封裝的HTML5廣告範本。 當您有在[!DNL Advertising Creative]之外建置的生產就緒HTML5創意時，這是最佳選擇。 |

## 標準廣告與動態廣告

[!UICONTROL Creative Studio]支援兩種決定AI代理程式行為方式的廣告內容模型：

**標準廣告** — 您提供或產生所有廣告內容。 AI代理程式可以在範本配置的限制內產生、修改或取代任何內容欄位（標題、CTA、影像、顏色、複製色調）。 選取廣告商和資料庫，並選取附加至套裝的選項，將完成的標準廣告儲存至創意資料庫。 標準廣告最適合自訂訊息行銷活動。

**動態廣告** — 內容由產品或內容目錄驅動。 四步驟引導式工作流程會逐步引導您選取範本、將目錄欄位對應至範本元素，以及設定廣告集。 設定後，AI代理程式會轉移至QA和預覽角色：它可依目錄欄位篩選廣告、標幟品質問題（字元限制、內容溢位、損壞的影像、法規遵循）並分析跨目錄的組合，但無法直接修改目錄來源的內容。 若要變更動態廣告內容，請更新來源目錄。

>[!MORELIKETHIS]
>
>* [在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理動態創意內容](creative-studio-manage-dynamic-ads.md)
>* [在Creative Studio中管理範本](creative-studio-manage-templates.md)
>* [在Creative Studio中管理資產](creative-studio-manage-assets.md)
>* [在Advertising Creative中管理品牌設定檔](/help/creative/brands/brand-manage.md)
