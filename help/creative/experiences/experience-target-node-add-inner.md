---
title: 在體驗中的節點之間新增目標節點
description: 瞭解如何在廣告體驗中的目標節點之間新增目標節點。
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---
# 在體驗中的節點之間新增目標節點

*僅使用決策樹定位的體驗*

當您在現有層次之間插入目標節點時，新目標節點會保留所有現有的子目標和創意，而新節點最初稱為「全部」。 您可以選擇保留新節點，而不新增更多特定目標。

若要定義特定目標，請在相同層級新增其他同層級目標節點、指定新目標，然後只將創意指派給該目標。 新增同層級目標節點會建立新的目標節點，並將先前指派給「全部」的所有子目標與創意移動到相同層次的新「其他所有專案」節點。 如此一來，新增目標不會影響現有的子分支，因為只有新的同層級節點包含新的目標定位資訊。

>[!NOTE]
>
>若要將目標節點新增至決策樹的最低層級，請參閱&quot;[將目標節點新增至體驗中的最終層級](experience-target-node-add-final.md)&quot;。

## 使用AI導向編輯器(Beta) {#ai-editor}

當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，您可以要求AI代理程式插入目標層級。 識別插入位置以及要保留的現有分支和創意，並檢閱結果。 若要直接在畫布中插入層級：

1. 在您要插入層級的界限上，按一下&#x200B;**[!UICONTROL Add targeting level]**。

   在水準檢視中，此控制項是具有相同標籤的圖示。

1. 在&#x200B;**[!UICONTROL New targeting level]**&#x200B;中，選取目標類別，然後按一下&#x200B;**[!UICONTROL Add targeting level]**。

   * 針對對象目標，選取&#x200B;**[!UICONTROL Audience]**。

   * 若為地理目標，請選取單一地理類別（例如&#x200B;**[!UICONTROL Geo: Country]**）。

   * 針對資料傳遞目標，選取&#x200B;**[!UICONTROL Data Pass]**。

   * 若要重新定位畫素目標，請選取&#x200B;**[!UICONTROL RT Pixel]**。

   * 針對裝置目標，選取單一目標類別（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**）。

   插入層級不會提示輸入目標值。 新層級最初使用「全部」並保留現有的子目標和創意。

1. （選擇性）若要在新層級定義特定目標，請[新增同層級目標節點](experience-target-node-add-sibling.md#ai-editor)。 否則，請保留新的「全部」節點，而不新增特定目標。

1. （選擇性）若要重新命名使用者定義的目標節點，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**，輸入&#x200B;**[!UICONTROL Node Name]**，然後按一下&#x200B;**[!UICONTROL Save]**。

   您無法重新命名「全部」或「其他所有人」節點。

1. 檢閱保留的分支，並將[創意組合](experience-assign-creative-bundles.md#ai-editor)指派給任何新的最終節點。

1. [儲存體驗](#save)。

## 使用手動編輯器 {#manual-editor}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

1. 在您要插入目標的節點底下，按一下[新增]。![](/help/creative/assets/add.png "")，然後選取&#x200B;**[!UICONTROL Insert New Target]**。

1. 執行下列任一項作業：

   * 如果同層級節點尚不存在，請執行下列動作：

     1. 選取目標型別，然後按一下&#x200B;**[!UICONTROL Apply]**：

        * 針對對象目標，選取&#x200B;**[!UICONTROL Audience]**。

        * 若為地理目標，請選取單一地理類別（例如&#x200B;**[!UICONTROL Geo: Country]**）。

        * 針對資料傳遞目標，選取&#x200B;**[!UICONTROL Data Pass]**。

        * 若要重新定位畫素目標，請選取&#x200B;**[!UICONTROL RT Pixel]**。

        * 針對裝置目標，選取單一目標類別（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**）。

   * 如果同層級節點已經存在，請執行下列動作：

     * 若為對象目標：

       1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以開啟&#x200B;**[!UICONTROL Audience Targeting]**&#x200B;選項。

       1. 設定對象區段和群組：

          * 若要新增第一個區段，請在左側面板中找出該區段，然後選取區段名稱旁的核取方塊。

          * 若要將區段新增至現有區段群組：

            1. 按一下右側面板中的區段群組。

            1. （選用）視需要將群組邏輯變更為&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

               **[!UICONTROL Include Any]**&#x200B;至少符合一個選取區段中的使用者；**[!UICONTROL Include All]**&#x200B;需要所有選取區段中的成員資格。

               **[!UICONTROL Exclude All]**&#x200B;不適用於第一個區段群組。 針對僅包含排除專案的對象，請使用&#x200B;**[!UICONTROL Include Any]**&#x200B;建立對象，然後在您將對象新增至DSP中的位置時，排除該對象。

            1. 在左側面板中找出新區段，並選取區段名稱旁的核取方塊。 對每個其他區段重複此步驟。

               區段群組會自動更新為新區段。

          * 若要新增區段群組：

            1. 按一下右側面板中的&#x200B;**[!UICONTROL + New Group]**。

            1. （選用）視需要將上一個群組與新群組之間的邏輯變更為&#x200B;**[!UICONTROL And]**&#x200B;或&#x200B;**[!UICONTROL Or]**。

               **[!UICONTROL And]**&#x200B;要求使用者符合兩個群組的條件；**[!UICONTROL Or]**&#x200B;要求他們至少符合一個群組的條件。

            1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

            1. （選用）視需要將群組邏輯變更為&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

       1. 按一下&#x200B;**[!UICONTROL Create]**。

       1. 按一下&#x200B;**[!UICONTROL Apply]**。

     * 針對地理目標，請執行下列動作：

       1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;開啟您的[!UICONTROL Geo Targeting]選項，指定一或多個地理目標，然後按一下&#x200B;**[!UICONTROL Save]**。

          郵遞區號目標具有大量編輯選項。 若要貼上多個郵遞區號，請按一下「**[!UICONTROL Paste postal codes]**」標籤、選取國家、貼上或輸入郵遞區號（以逗號分隔或分行），然後按一下「**[!UICONTROL Include All]**」。 若要移除包含的郵遞區號目標，請將游標停留在目標上，然後按一下![移除](/help/creative/assets/delete.png "移除") **[!UICONTROL Remove]**。

       1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

          此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置（[!DNL Boolean] `AND`陳述式）。

       1. 按一下&#x200B;**[!UICONTROL Apply]**。

     * 針對資料傳遞目標，可選擇自訂資料傳遞金鑰，輸入單一資料傳遞值，然後按一下&#x200B;**[!UICONTROL Apply]**。

       預設資料傳遞金鑰是在[一般體驗設定](experience-settings-targeting.md)的&#x200B;**[!UICONTROL Advanced]**&#x200B;區段的&#x200B;**[!UICONTROL Data Pass]**&#x200B;欄位中設定。 視需要自訂目標的金鑰。

     * 對於重定目標畫素目標，請選取要使用的單一重定目標畫素，以及顯示創意所需的任何畫素屬性值，然後按一下&#x200B;**[!UICONTROL Apply]**。

       可用的屬性是在[重新定位畫素設定](/help/creative/pixels/retargeting-pixel-manage.md)中設定。

     * 針對裝置目標，請執行下列動作：

       1. 選取目標。

       1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

          此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置（[!DNL Boolean] `AND`陳述式）。

       1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

       1. 按一下&#x200B;**[!UICONTROL Apply]**。

1. （選用）為使用者定義的分支指定自訂分支名稱。

   依預設，使用者定義的分支會加上套用目標的標籤。

   您無法為「全部」或「其他所有人」分支建立自訂分支名稱。

   1. 將游標停留在目標節點上並按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**。

   1. 輸入&#x200B;**[!UICONTROL Node Name]**，然後按一下&#x200B;**[!UICONTROL Save]**。

1. （選用） [將創意組合](experience-assign-creative-bundles.md#manual-editor)指派給新目標節點和「其他一切」節點。

1. （選擇性） [新增指定目標型別的同層級目標節點](experience-target-node-add-sibling.md#manual-editor)。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [刪除目標節點或創意分葉節點](/help/creative/experiences/experience-target-node-delete.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
