---
title: 建立可重複使用的對象
description: 瞭解如何建立可重複使用的受眾，其中包含受眾區段和其他儲存的受眾。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e2d040409bcf18ca3c7906e8f3d5d3dc6633d2d7
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# 建立可重複使用的對象

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他儲存的對象，您可將其用作多個位置的目標或排除專案。

>[!NOTE]
>
>（DSP將其雜湊電子郵件ID轉換為LiveRamp RampID區段的廣告商）未附加至使用中、已排程或暫停位置的第一方RampID區段會暫停。 該區段在區段清單中記錄為「自動暫停」。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

1. 輸入唯一的&#x200B;**[!UICONTROL Audience Name]**。

1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的選項。

   當您共用對象時，該對象會成為帳戶中所有廣告商的目標或排除專案。 但是，受眾中的各個段僅對共用這些段的用戶可用。 例如，如果您與未映射到相同[!DNL Analytics]帳戶的廣告商共用包含Adobe Analytics網段的受眾，則該網段不會在該受眾中為該廣告商預覽。 只有該廣告商可用的片段才在觀眾中預覽。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 構建受眾：

   >[!NOTE]
   >
   >在構建受眾時，在右面板中更新了詳細的[受眾大小資料](audience-about.md)

   * 要手動建立段邏輯，請使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]頁籤](audience-settings.md)上可用的段，請執行以下操作。

      * （可選）搜索段名稱、說明或路徑。

        搜索結果包括基於您使用的確切術語的段。 輸入多個術語時，必須為段找到所有術語。

      * 要添加第一個段，請在左面板中找到該段，然後選中段名稱旁邊的複選框。

      * 要將段添加到現有段組，請執行以下操作：

         1. 按一下右面板中的段組。

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

      1. 以下列任何一種方式從現有受眾複製段邏輯：

         * 在「所有受眾」視圖中，將游標懸停在受眾行上，然後按一下&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在現有受眾的設定中，在段邏輯面板頂部，按一下&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文本編輯器中，使用字母數欄位ID和[布爾語法](audience-segment-logic-syntax.md)手動建立段邏輯，並將其複製到剪貼簿。

      1. 按一下&#x200B;**[!UICONTROL paste in an audience rule to begin building]**，將現有段邏輯貼上到輸入欄位中，然後按一下&#x200B;**[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果受眾已經包括任何段邏輯，則貼上到新段邏輯會覆蓋現有邏輯。

1. 按一下&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [關於受眾管理](audience-about.md)
>* [受眾設定](audience-settings.md)
>* [受眾段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)
>* [建立和實施自訂區段](custom-segment-create.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
