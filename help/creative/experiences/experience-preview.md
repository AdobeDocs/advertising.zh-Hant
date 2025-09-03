---
title: 預覽體驗
description: 瞭解如何在廣告體驗中預覽創意內容。
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# 預覽體驗

您可以預覽具有特定廣告大小的創意，而目標檢視者可以看到該廣告大小的體驗，包括所有超連結。 對於決策樹目標定位的體驗，您可以預覽單一創意、特定分支的創意（目標型別）或體驗中的所有創意。 針對沒有決策樹定位的體驗，您可以預覽單一創意內容。<!-- verify -->

* 預覽體驗或特定分支的所有創意時，會顯示所有適用的創意內容。

* 當您預覽符合條件的單一創意和多個創意時，您每次重新整理預覽時看到的創意會根據體驗的廣告旋轉設定：

   * 對於演演算法廣告輪換，會根據最佳化目標選取創意。

   * 對於已排程的廣告輪換，會顯示排程中的第一個創意內容。 您可以繼續重新整理預覽以繼續完成序列。

   * 對於加權廣告輪換，創意是根據指定的權重來選取(例如每次顯示Creative A的機率為80%，顯示Creative B的機率為20%)。

## 使用決策樹定位預覽體驗中的創意內容

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定體驗。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

1. 選取要預覽的創意：

   * 若要預覽單一創意：

      1. 按一下&#x200B;**[!UICONTROL Creative]**。

      1. 選取廣告大小。

      1. 在[!UICONTROL Decision Tree Targeting]區段中，選取創意目標。

   * 若要預覽特定分支的創意，請執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL Particular branch]**。

      1. 選取廣告大小。

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. 選取創意目標。

   * 若要預覽體驗中的所有創意內容，請按一下&#x200B;**[!UICONTROL Entire Tree]**。

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. （選擇性）若要包含創意的名稱、創意型別和大小、登陸頁面URL或按一下URL，以及每個創意下面的彈性屬性，請選取&#x200B;**[!UICONTROL Display Creative Metadata]**。

1. 按一下&#x200B;**[!UICONTROL Preview]**。

1. （僅依創意內容預覽；選擇性）在工具列中，按一下&#x200B;**[!UICONTROL Refresh]**&#x200B;以根據廣告旋轉設定預覽任何可能顯示的其他創意內容。<!-- I don't see this as of 2/3 -->

1. （選用）若要複製體驗的示範URL以與其他人共用，且未登入[!DNL Creative]：

   1. 在預覽的右上角，按一下![共用](/help/creative/assets/share.png "共用")。

   1. 在[!UICONTROL Share Demo URL]對話方塊中，按一下&#x200B;**[!UICONTROL Copy]**&#x200B;將URL複製到剪貼簿，以便與其他人共用。

## 在沒有決策樹定位的情況下預覽體驗中的創意內容

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定體驗。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

1. （選用）選取特定創意大小，以限制創意內容清單。

   依預設，會列出所有大小的創意。

1. 按一下廣告標籤的名稱，可展開列並預覽創意內容。

1. （選用）若要前往創意內容的登陸頁面，請按一下創意內容。

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （選用）若要複製體驗的示範URL以與其他人共用，且未登入[!DNL Creative]：

   1. 在預覽的右上角，按一下![共用](/help/creative/assets/share.png "共用")。

   1. 在[!UICONTROL Share Demo URL]對話方塊中，按一下&#x200B;**[!UICONTROL Copy]**&#x200B;將URL複製到剪貼簿，以便與其他人共用。

>[!MORELIKETHIS]
>
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [建立沒有決策樹定位的體驗](/help/creative/experiences/experience-create-no-targeting.md)
