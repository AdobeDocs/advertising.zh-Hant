---
title: 編輯可重複使用的對象
description: 瞭解如何編輯可重複使用的對象。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 編輯可重複使用的對象

當您編輯用於任何刊登版位或其他可重複使用對象的對象時，變更會立即套用至這些刊登版位和對象。<!-- verify -->

>[!NOTE]
>
>(DSP將其雜湊電子郵件ID轉換為LiveRamp RampID區段的廣告商)未附加至使用中、已排程或暫停位置的第一方RampID區段會暫停。 該區段在區段清單中記錄為「自動暫停」。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**。

1. 將游標停留在對象列上並按一下&#x200B;**[!UICONTROL Edit]**。

1. 透過下列任一種方式編輯對象設定：

   >[!NOTE]
   >
   >如果您編輯對象區段邏輯，右側面板中會更新詳細的[對象人數資料](audience-about.md)。

   * （選擇性）若要編輯&#x200B;**[!UICONTROL Audience Name]**，請按一下對象名稱旁的![編輯](/help/dsp/assets/edit.png)，輸入唯一的對象名稱，然後按一下&#x200B;**[!UICONTROL Apply]**。

   * （選擇性）若要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]索引標籤](audience-settings.md)上可用的區段來手動編輯區段邏輯，請執行下列動作。

      * 若要將區段新增至現有區段群組：

      1. 按一下右側面板中的區段群組。

      1. （選用）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

         *[!UICONTROL Exclude All]*&#x200B;不適用於第一個區段群組。 若對象僅包含排除專案，請將此對象建置為&#x200B;*[!UICONTROL Include Any]*，然後在位置中，從「排除的對象」選單中選取該對象。

      1. 在左側面板中找出新區段，並選取區段名稱旁的核取方塊。

         區段群組會自動更新為新區段。

   * 若要新增區段群組：

      1. 按一下右側面板中的&#x200B;**[!UICONTROL + New Group]**。

      1. （選用）視需要將上一個群組與新群組之間的邏輯變更為&#x200B;*[!UICONTROL And]*&#x200B;或&#x200B;*[!UICONTROL Or]*。

      1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

      1. （選用）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

   * 若要使用現有對象中的區段邏輯：

      1. 透過下列任何方式，從現有對象複製區段邏輯：

         * 在「所有對象」檢視中，將游標停留在對象列上，然後按一下「**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**」。

         * 在現有對象的設定中，按一下區段邏輯面板頂端的&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文字編輯器中，使用英數字元區段ID和[布林值語法](audience-segment-logic-syntax.md)手動建立區段邏輯，並將其複製到剪貼簿。

      1. 按一下&#x200B;**[!UICONTROL paste in an audience rule to begin building]**，將現有的區段邏輯貼到輸入欄位中，然後按一下&#x200B;**[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果對象已包含任何區段邏輯，則貼入新區段邏輯會覆寫現有邏輯。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Continue]**。

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [重複可重複使用的對象](reusable-audience-duplicate.md)
>* [檢視可重複使用對象的詳細資料](reusable-audience-view-details.md)
>* [共用可重複使用的對象](reusable-audience-share.md)
>* [匯出可重複使用的對象](reusable-audience-export.md)
>* [將可重複使用對象的區段金鑰複製到剪貼簿](reusable-audience-clipboard.md)
>* [刪除可重複使用的對象](reusable-audience-delete.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
