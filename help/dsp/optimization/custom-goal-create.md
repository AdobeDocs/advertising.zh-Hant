---
title: 建立自定義目標
description: 建立自定義目標
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# 建立自定義目標

您可以建立自定義目標 *目標* 內 [!DNL Advertising Search, Social, & Commerce]。

要建立自定義目標，DSP必須將帳戶連結到 [!DNL Search, Social, & Commerce] 具有相同Adobe Experience Cloud組織ID的帳戶，從 [!DNL Search, Social, & Commerce] 客戶端設定。 如果DSP帳戶未連結到 [!DNL Search, Social, & Commerce] 帳戶，請與Adobe帳戶小組聯繫。

>[!TIP]
>
>查看 [建立自定義目標的最佳實踐](custom-goal-best-practices.md) 有關如何配置自定義目標的提示。

1. 登錄 [!DNL Advertising Search, Social, & Commerce] at（北美用戶） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他用戶） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com)。
1. 確保跟蹤了要包括在目標中的度量，在產品中可用，並包括顯示名稱：
   1. 在主菜單中，按一下 **[!UICONTROL Search]** > **[!UICONTROL Admin]>[!UICONTROL Transaction Properties]**。
   1. 找到度量，並確保 **[!UICONTROL Show in UI and Reports]** 為度量啟用。
   1. 如果度量在 **[!UICONTROL Display Name]** 列，按一下單元格，輸入顯示名稱，然後按一下 **[!UICONTROL Apply]。**
1. 將自定義目標建立為 *客觀*:
   1. 在主菜單中，按一下 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**。
   1. 在工具欄中，按一下 **[!UICONTROL Create objective]。**
   1. 輸入目標設定：
      1. 在 **[!UICONTROL Change Objective Name]** 欄位，輸入目標名稱。

         目標名稱將顯示在 [!UICONTROL Custom Goals] 的子DSP菜單。

      1. 將屬性與目標關聯：

         >[!NOTE]
         >
         > 預設情況下，為廣告商跟蹤的所有交易屬性在 [!UICONTROL Available Properties] 清單框。

         * 要導入具有屬性及其權重的CSV檔案，請按一下 **[!UICONTROL Import]** 找到要導入的檔案。

            對於廣告商，必須已存在進口的財產；這些名字不區分大小寫。

            導入的屬性將替換指定的任何現有屬性。

         * 要手動指定預設權重為(1)的第一個屬性，請從為廣告商跟蹤的所有交易屬性清單中選擇。

         * 要手動添加另一個具有預設權重(1)的屬性，請按一下 **[!UICONTROL +]** 。

            >[!TIP]
            >
            > 要在清單中搜索屬性，請在屬性名稱中的任何位置輸入字串。

         * 要手動添加多個屬性，請按一下 **[!UICONTROL Add Multiple Properties]。** 對於要添加的每個屬性，按一下 [!UICONTROL Available Properties] 列，然後拖到 [!UICONTROL Added Properties] 的雙曲餘切值。 添加完屬性後，按一下 **[!UICONTROL Add]**。

            >[!TIP]
            >
            >* 要在清單中搜索屬性，請在輸入欄位中的屬性名稱的任何位置輸入字串。
            >* 要篩選清單以排除在報告中排除的屬性，請選擇選項 **[!UICONTROL Hide properties excluded from reports]。**


         * （當目標包含多個屬性時）要更改屬性相對於目標中其他屬性的權重，請在 **[!UICONTROL Weight]** 欄位。
      1. 在設定底部，按一下 **[!UICONTROL Save]**。


建立目標後，可以將其作為自DSP定義目標分配給包，當優化目標為「」[!UICONTROL Highest ROAS - Custom Goal]&quot;或&quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;

>[!TIP]
>
>為獲得最佳效能，自定義目標（目標）中的組合度量每天必須至少進行十次轉換。 如果它們不支援，則最佳做法是向目標中添加其他支援事件（事務屬性），如產品頁或應用程式啟動。 請參閱 [構建自定義目標的最佳做法](custom-goal-best-practices.md) 指南。

>[!MORELIKETHIS]
>
>* [關於自定義目標](custom-goal-about.md)
>* [構建自定義目標的最佳做法](custom-goal-best-practices.md)
>* [優化目標及其使用方法](optimization-goals.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [如何優DSP化您的市場活動](optimization-how-dsp-optimizes-campaigns.md)

