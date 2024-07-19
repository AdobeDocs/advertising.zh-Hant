---
title: 建立負面關鍵字
description: 瞭解如何為搜尋促銷活動和廣告群組建立負面關鍵字。
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# 建立負面關鍵字

僅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]和現有[!DNL Baidu]帳戶*

您可以針對搜尋或顯示/原生網路，為搜尋廣告群組或行銷活動建立負關鍵字。 負面關鍵字不會觸發廣告。

>[!NOTE]
>您也可以在[廣告群組設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)和[行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)中建立和編輯負關鍵字。

>[!TIP]
>若要一次建立許多負面關鍵字，請使用[行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")，然後按一下&#x200B;**[!UICONTROL Campaign]**&#x200B;建立行銷活動層級的負關鍵字，或按一下&#x200B;**[!UICONTROL Ad Group]**&#x200B;建立廣告群組層級的負關鍵字。

1. 選取廣告網路、帳戶、行銷活動，以及（相關時）廣告群組，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 輸入負關鍵字。 請使用下列語法，不含減號(`-`)：

   * 負值廣泛比對： `keyword` （不受[!DNL Microsoft Advertising]支援）

   * 負面字詞相符： `"keyword"`

   * 完全相符的負值： `[keyword]`

   請使用逗號分隔多個值，或在不同的行中輸入這些值。 您最多可以在一個作業中輸入或貼上2000個負關鍵字。 另請參閱下列需求和限制：

   * 最大字元長度： [!DNL Baidu]： 30個單位元組或15個雙位元組； [!DNL Microsoft Advertising]： 100個單位元組或50個雙位元組； [!DNL Google Ads]和[!DNL Yahoo! Japan Ads]： 80個單位元組或40個雙位元組。

   * [!DNL Baidu]僅允許每個廣告群組的每個關鍵字有一個符合型別。 例如，廣告群組1不能同時包含`"keyword"`和`[keyword]`。

   * [!DNL Google Ads]：每個關鍵字最多只能包含10個字詞，而且只能包含字母、數字和下列特殊字元：空格`# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]：每個關鍵字最多可以有七個單字（不包括停用詞）。 每個[!DNL Yandex ad group]最多可包含200個關鍵字。

1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!MORELIKETHIS]
>
>* [關於關鍵字](keyword-about.md)
>* [管理可競標關鍵字](keyword-manage.md)
>* [變更關鍵字和負關鍵字的狀態](keyword-status-edit.md)
