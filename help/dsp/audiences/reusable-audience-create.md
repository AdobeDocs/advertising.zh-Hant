---
title: 建立可重複使用的對象
description: 瞭解如何建立可重複使用的受眾，其中包含受眾區段和其他儲存的受眾。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# 建立可重複使用的對象

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他儲存的對象，您可將其用作多個位置的目標或排除專案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

1. 輸入唯一的&#x200B;**[!UICONTROL Audience Name]**。

1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的選項。

   當您共用對象時，該對象會成為帳戶中所有廣告商的目標或排除專案。 不過，受眾中的個別區段僅供共用區段的使用者使用。 例如，如果您將包含Adobe Analytics區段的對象與未對應至相同[!DNL Analytics]帳戶的廣告商共用，則不會在該廣告商的對象中預覽該區段。 在對象中只會預覽該廣告商可用的區段。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 建立對象：

   >[!NOTE]
   >
   >當您建置對象時，右側面板中會更新詳細的[對象人數資料](audience-about.md)

   * 若要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]索引標籤](audience-settings.md)上可用的區段來手動建立區段邏輯，請執行下列動作。

      * 若要新增第一個區段，請在左側面板中找出該區段，然後選取區段名稱旁的核取方塊。

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

1. 按一下&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
>* [建立和實施自訂區段](custom-segment-create.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
