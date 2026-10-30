---
title: 在體驗中的節點之間新增同層級目標節點
description: 瞭解如何將同層級節點新增至具有目標或與具有目標之節點位於相同層級的任何節點。
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: 'https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o'
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
source-wordcount: '1151'
ht-degree: 0%
---
# 在體驗中的節點之間新增同層級目標節點

*僅使用決策樹定位的體驗*

您可以將同層級節點新增至任何具有目標的節點，或與具有目標的節點位於相同層級的節點。

## 使用AI導向編輯器(Beta) {#ai-editor}

當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，您可以向AI代理程式描述新的同層級目標。 識別其父分支和目標值，並檢閱結果。 若要直接在畫布中新增同層級：

1. 將游標停留在您要其他同層級之節點的父項上，然後按一下&#x200B;**[!UICONTROL +]**。

   目標類別由現有層級決定，值選取器會為該類別開啟。

1. 指定類別的目標值：

   * 若為對象目標：

     * 若要新增第一個區段，請找到並選取對象區段。

     * 若要將區段新增至現有區段群組：

       1. 選取區段群組。

       1. （選用）視需要將群組邏輯變更為&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

          **[!UICONTROL Include Any]**&#x200B;至少符合一個選取區段中的使用者；**[!UICONTROL Include All]**&#x200B;需要所有選取區段中的成員資格。

          **[!UICONTROL Exclude All]**&#x200B;不適用於第一個區段群組。 針對僅包含排除專案的對象，請使用&#x200B;**[!UICONTROL Include Any]**&#x200B;建立對象，然後在您將對象新增至DSP中的位置時，排除該對象。

       1. 找到並選取其他區段。

     * 若要新增區段群組：

       1. 新增群組。

       1. （選用）視需要將上一個群組與新群組之間的邏輯變更為&#x200B;**[!UICONTROL And]**&#x200B;或&#x200B;**[!UICONTROL Or]**。

          **[!UICONTROL And]**&#x200B;要求使用者符合兩個群組的條件；**[!UICONTROL Or]**&#x200B;要求他們至少符合一個群組的條件。

       1. 找到並選取新群組的區段。

       1. （選用）視需要將群組邏輯變更為&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

   * 若為地理目標：

     * 在現有層次選取地理類別中的位置，例如國家、地區或城市。

     * 針對郵遞區號目標，選取國家/地區，然後輸入要包含的郵遞區號。 若要大量輸入多個郵遞區號，請以逗號分隔多個郵遞區號，或將每個郵遞區號放在單獨的一行上。

   * 針對資料傳遞目標，輸入要比對的索引鍵和值。

     預設資料傳遞金鑰是在[一般體驗設定](experience-settings-targeting.md)的&#x200B;**[!UICONTROL Advanced]**&#x200B;區段的&#x200B;**[!UICONTROL Data Pass]**&#x200B;欄位中設定。 視需要自訂目標的金鑰。

   * 如果要重新定位畫素目標，請選取重新定位畫素，然後指定顯示創意所需的任何畫素屬性值。

     可用的屬性是在[重新定位畫素設定](/help/creative/pixels/retargeting-pixel-manage.md)中設定。

   * 針對裝置目標，在現有層級選取裝置類別中的值：裝置型別、作業系統或瀏覽器。

1. （如果可用；選擇性）選取&#x200B;**[!UICONTROL Split Nodes]**&#x200B;為每個選取的值建立單獨的目標節點，並具有自己的創意組合指派。 否則，選取的值會分組到一個目標節點中。

1. 按一下&#x200B;**[!UICONTROL Add Node]**。

1. （選擇性）若要重新命名新節點，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**，輸入&#x200B;**[!UICONTROL Node Name]**，然後按一下&#x200B;**[!UICONTROL Save]**。

1. 如果新節點是最終節點，[指派創意組合](experience-assign-creative-bundles.md#ai-editor)，然後[儲存體驗](#save)。

## 使用手動編輯器 {#manual-editor}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

1. 在您要新增同層級節點的節點上方，按一下[新增]。![](/help/creative/assets/add.png "")，然後選取&#x200B;**[!UICONTROL Insert Sibling Target]**。

1. 指定類別的目標值：

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

   * 如果要重新定位畫素目標，請選取要使用的重新定位畫素，以及顯示創意所必須呈現之任何畫素屬性的必要值。 然後按一下&#x200B;**[!UICONTROL Apply]**。

     可用的屬性是在[重新定位畫素設定](/help/creative/pixels/retargeting-pixel-manage.md)中設定。

   * 針對裝置目標，請執行下列動作：

     1. 選取目標。

     1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

        此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置（[!DNL Boolean] `AND`陳述式）。

     1. 按一下&#x200B;**[!UICONTROL Apply]**。

1. （選用）為使用者定義的分支指定自訂分支名稱。

   依預設，使用者定義的分支會加上套用目標的標籤。

   您無法為「全部」或「其他所有人」分支建立自訂分支名稱。

   1. 將游標停留在目標節點上並按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**。

   1. 輸入&#x200B;**[!UICONTROL Node Name]**，然後按一下&#x200B;**[!UICONTROL Save]**。

1. （選擇性） [將創意組合](experience-assign-creative-bundles.md#manual-editor)指派給新的目標節點。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [刪除目標節點或創意分葉節點](/help/creative/experiences/experience-target-node-delete.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
