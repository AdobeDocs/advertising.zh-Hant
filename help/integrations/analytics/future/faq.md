---
title: 常見問答
description: xxx
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 常見問題集xxx

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/14214
依預設，Adobe Analytics會報告每個報表中所有擷取的事件。 「[!UICONTROL Unspecified]」事件代表未連線至Adobe Advertising的表單完成事件。 例如，在Ad Platform報表中，電子郵件促銷活動驅動的有機轉換或轉換將屬於「未指定」。

您可以使用篩選器，透過移除「包含未指定（無）」選項的核取記號來從報表中移除未指定的事件。<!-- Not sure if this is in DSP or in Analytics Workspace -->

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323
將Analytics事件標籤放在與Ad Cloud畫素相同的位置，以確保XXX相符。

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323

問：在內部安全性稽核期間，當我們將Ad Cloud整合至現有的Adobe Analytics安裝時，某些功能會被標籤為已啟用的安全性問題。

有問題的整合是AdCloud與Adobe Audience Manager之間的整合。 此功能可提高AdCloud與Adobe Audience Manager之間訪客ID的符合率。 其做法是傳送網路要求至pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com，以判斷這些服務是否有訪客的現有ID可供運用。 這些是已標籤為安全性風險且正在發生於所有網站訪客的網路請求。

我們的稽核人員要求我們停用此功能。 如果我們封鎖這些網路要求會發生什麼事？

答：我們檢查了產品，他們指出問題畫素是為了提高Ad Cloud、特定詳細目錄/SSP合作夥伴(關於DSP)和AAM之間的Cookie匹配率。  如果移除這些畫素，客戶可能會發現AAC/AAM與詳細目錄合作夥伴之間個別畫素適用的匹配率有所降低，但他們不會預期這會相當大。

對於Ad Cloud搜尋，我們確實看到廣告商的Experience Cloud組織ID已針對Mathworks設定，但我們的產品團隊沒有看到Mathworks設定以在Ad Cloud中啟用對象。 您是否使用Adobe Audience Manager傳送受眾至Ad Cloud搜尋？ 如果沒有，移除這些專案不會影響目前的工作流程。 如果您不想引發這些畫素，AAM客戶服務可協助您移除這些畫素。

