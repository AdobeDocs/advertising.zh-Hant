---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# 第2級 — 購物廣告範本中的第8級欄位

**[!UICONTROL Tier  2 - Tier 8]：** （當您新增產品群組階層時）目標產品的產品屬性型別，以及所選屬性型別的資格條件（例如，Brand=Acme或Condition=New）。 這些值會依階層套用，以決定符合資格的產品。 選取屬性型別並輸入合格條件。 禁止使用的字元包括： `[ ] < > >>` （兩個連續的「大於」符號），用來指定範本中的欄名稱、範本中的修飾元名稱以及 [!UICONTROL Parent Product Grouping] 大量表單中的欄。

您可以包含最多八層（層級）產品群組，包括「[!UICONTROL All Products]&quot; （第1級）。 每個層級可包含多個產品群組，但它們必須屬於相同的屬性型別（例如「條件」）。

>[!NOTE]
>
>* ([!DNL Google Ads] 僅限)的可能值 [!UICONTROL Channel] 為「[!UICONTROL Local]「或」[!UICONTROL Online]「 」和的可能值 [!UICONTROL ChannelExclusivity] 為「[!UICONTROL SingleChannel]「和」[!UICONTROL MultiChannel].」
>* 當您從以下專案為廣告群組建立第二層（子項）產品群組時： [!UICONTROL Product Groups] 索引標籤中的 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 檢視，另一個產品群組，稱為&quot;[!UICONTROL Everything Else]，」會使用預設廣告群組競標自動建立。 但是，使用庫存摘要範本」[!UICONTROL Everything Else]「已排除產品群組。
>* 當您包含多個層級，且最終（編號最高的）層級沒有可用的值時，則會使用次高層級作為可競標的產品群組。 例如，如果您包含五個層級，而第5層沒有可用的值，則第4層會作為可競標的產品群組（單位）。 但是，如果中間層沒有可用的值，則會忽略該列。 例如，如果您包含五個層級，而層級5有一個值，但層級4沒有，則會忽略第4列。

