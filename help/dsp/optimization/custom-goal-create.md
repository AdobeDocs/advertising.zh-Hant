---
title: 建立自訂目標
description: 建立自訂目標
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# 建立自訂目標

您可以建立自訂目標為 *目標* 範圍 [!DNL Advertising Search, Social, & Commerce].

若要建立自訂目標，DSP帳戶必須連結至 [!DNL Search, Social, & Commerce] 在中使用相同Adobe Experience Cloud組織ID的帳戶 [!DNL Search, Social, & Commerce] 使用者端設定。 如果您的DSP帳戶未連結至 [!DNL Search, Social, & Commerce] 請聯絡您的Adobe客戶團隊。

>[!TIP]
>
>請參閱 [建立自訂目標的最佳實務](custom-goal-best-practices.md) 以取得如何設定自訂目標的秘訣。

1. 登入 [!DNL Advertising Search, Social, & Commerce] at （北美使用者） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他使用者） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 確認已追蹤您要在目標中納入的量度、可在產品中使用，且包含顯示名稱：
   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. 找到量度，並確定 **[!UICONTROL Show in UI and Reports]** 已針對量度啟用。
   1. 如果量度中沒有值 **[!UICONTROL Display Name]** 欄，按一下儲存格，輸入顯示名稱，然後按一下 **[!UICONTROL Apply].**
1. 建立自訂目標為 *目標*：
   1. 在主功能表中，按一下 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. 在工具列中，按一下 **[!UICONTROL Create objective].**
   1. 輸入目標設定：
      1. 在 **[!UICONTROL Change Objective Name]** 欄位，輸入目標名稱。

         目標名稱將顯示在 [!UICONTROL Custom Goals] 清單中的DSP封裝設定。

      1. 將屬性與目標建立關聯：

         >[!NOTE]
         >
         > 根據預設，為廣告商追蹤的所有轉換量度都會列在 [!UICONTROL Available Properties] 清單。

         * 若要匯入包含轉換量度及其權重的CSV檔案，請按一下 **[!UICONTROL Import]** 並找到要匯入的檔案。

           廣告商的匯入轉換量度必須已存在；名稱不區分大小寫。

           匯入的轉換量度會取代任何指定的現有屬性。

         * 若要手動指定具有預設權數(1)的第一個轉換量度，請從為廣告商追蹤的所有轉換量度清單中選取。

         * 若要手動新增另一個具有預設權重的轉換量度(1)，請按一下 **[!UICONTROL +]** .

           >[!TIP]
           >
           > 若要搜尋清單中的量度，請輸入量度名稱內任何位置的字串。

         * 若要手動新增多個轉換量度，請按一下 **[!UICONTROL Add Multiple Properties].** 針對您要新增的每個轉換量度，按一下 [!UICONTROL Available Properties] 欄並將其拖曳到 [!UICONTROL Added Properties] 欄。 完成新增量度時，請按一下 **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* 若要搜尋清單中的量度，請在輸入欄位中輸入量度名稱中的任何字串。
           >* 若要篩選清單以排除報表中排除的量度，請選取選項 **[!UICONTROL Hide properties excluded from reports].**

         * （當目標包含多個轉換量度時）若要變更量度相對於目標中其他量度的權重，請在 **[!UICONTROL Weight]** 欄位。

      1. 在設定底部，按一下 **[!UICONTROL Save]**.

建立目標後，當最佳化目標是「 」時，您可以將其指派給DSP套件作為自訂目標[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].」

>[!TIP]
>
>為獲得最佳效能，自訂目標（目標）中的合併量度每天必須至少總十次轉換。 若未包含，最佳作法是將其他支援的轉換量度（例如產品頁面或應用程式啟動）新增至目標。 另請參閱 [建立自訂目標的最佳實務](custom-goal-best-practices.md) 以取得指引。

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標的最佳實務](custom-goal-best-practices.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
