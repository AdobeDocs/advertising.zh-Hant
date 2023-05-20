---
title: 編輯可重用受眾
description: 瞭解如何編輯可重用的受眾。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 編輯可重用受眾

當編輯用於任何放映或其他可重複使用的觀眾的觀眾時，這些更改將立即應用於這些放映和觀眾。<!-- verify -->

1. 在主菜單中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**。

1. 將游標懸停在觀眾行上並按一下 **[!UICONTROL Edit]**。

1. 以下列任一方式編輯受眾設定：

   >[!NOTE]
   >
   >如果編輯受眾段邏輯，則詳細 [受眾大小資料](audience-about.md) 在右面板中更新。

   * （可選）編輯 **[!UICONTROL Audience Name]** 按一下 ![編輯](/help/dsp/assets/edit.png) 在受眾名稱旁邊，輸入唯一的受眾名稱，然後按一下 **[!UICONTROL Apply]**。

   * （可選）使用上的可用段手動編輯段邏輯 [[!UICONTROL Third Party Segments]。 [!UICONTROL First Party Segments]。 [!UICONTROL Adobe Segments]。 [!UICONTROL Custom Segments], [!UICONTROL Saved Audiences] 頁籤](audience-settings.md)，執行以下操作。

      * 要將段添加到現有段組，請執行以下操作：
      1. 按一下右面板中的段組。

      1. （可選）將組邏輯更改為 *[!UICONTROL Include Any]*。 *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根據需要。

         *[!UICONTROL Exclude All]* 不可用於第一個段組。 對於僅包括排除的受眾，將此受眾構建為 *[!UICONTROL Include Any]* 然後，在放置中，從「排除的受眾」菜單中選擇該受眾。

      1. 在左面板中找到新段，然後選中段名稱旁邊的複選框。

         段組將自動使用新段更新。
   * 要添加新段組，請執行以下操作：

      1. 按一下 **[!UICONTROL + New Group]** 的下界。

      1. （可選）將上一個組和新組之間的邏輯更改為 *[!UICONTROL And]* 或 *[!UICONTROL Or]*，根據需要。

      1. 在左面板中找到新組的段，然後選中段名稱旁邊的複選框。

      1. （可選）將組邏輯更改為 *[!UICONTROL Include Any]*。 *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根據需要。
   * 要使用現有受眾的段邏輯：

      1. 以下列任何方式從現有受眾複製段邏輯：

         * 在「所有受眾」視圖中，將游標懸停在受眾行上，然後按一下 **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在現有受眾的設定中，在段邏輯面板頂部，按一下 **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文本編輯器中，使用字母數欄位ID手動建立段邏輯， [布爾語法](audience-segment-logic-syntax.md)，然後複製到剪貼簿。
      1. 按一下 **[!UICONTROL paste in an audience rule to begin building]**，將現有段邏輯貼上到輸入欄位，然後按一下 **[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果受眾已經包括任何段邏輯，則貼上到新段邏輯會覆蓋現有邏輯。





1. 按一下 **[!UICONTROL Save]**.

1. 在確認消息中，按一下 **[!UICONTROL Continue]**。

>[!MORELIKETHIS]
>
>* [關於受眾管理](audience-about.md)
>* [建立可重用的受眾](reusable-audience-create.md)
>* [複製可重複使用的受眾](reusable-audience-duplicate.md)
>* [查看有關可重用受眾的詳細資訊](reusable-audience-view-details.md)
>* [共用可重複使用的受眾](reusable-audience-share.md)
>* [導出可重複使用的受眾](reusable-audience-export.md)
>* [將可重用受眾的段鍵複製到剪貼簿](reusable-audience-clipboard.md)
>* [刪除可重用受眾](reusable-audience-delete.md)
>* [受眾設定](audience-settings.md)
>* [受眾段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)

