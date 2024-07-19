---
title: 從摘要產生的資料狀態
description: 瞭解從詳細目錄資料摘要產生的資料狀態。
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 從摘要產生的資料狀態

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

每個元件都可以有以下其中一種狀態：

* *[!UICONTROL New]：*&#x200B;元件不存在於廣告網路上，且未張貼至廣告網路，您仍可按一下元件名稱來編輯其設定（若有需要）。 當您準備好發佈資料時，請按一下&#x200B;**[!UICONTROL Post to SE]**&#x200B;並指定要提交的資料。

* *[!UICONTROL Posted]：* （僅限行銷活動和廣告群組）行銷活動或廣告群組已部分張貼至廣告網路，但由於發生錯誤，部分元件未張貼。 每個關鍵字和廣告的驗證狀態會顯示哪些資訊需要更正。 您可以按一下元件名稱來編輯元件設定（如有需要）。

* *[!UICONTROL Active]：*&#x200B;元件已在廣告網路上作用中，您無法在這裡編輯其設定。 作用中元件可能包含[!UICONTROL New]的子元件，如果資料有效，便可以張貼。

* *[!UICONTROL Paused]：*&#x200B;元件已在廣告網路上暫停，您無法在這裡編輯其設定。 暫停的元件可能包含[!UICONTROL New]的子元件，如果資料有效，便可以張貼。

* *[!UICONTROL Deleted]：*&#x200B;元件已在廣告網路上刪除，您無法在這裡編輯其設定。 已刪除的元件可能包含[!UICONTROL New]的子元件，如果資料有效，便可以張貼。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
