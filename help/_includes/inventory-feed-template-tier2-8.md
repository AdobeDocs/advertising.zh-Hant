---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# 第2級 — 購物廣告範本中的第8級欄位

**[!UICONTROL Tier  2 - Tier 8]：** （當您新增產品群組階層時）目標產品的產品屬性型別，以及所選屬性型別的合格條件（例如，Brand=Acme或Condition=New）。 這些值會依階層套用，以決定符合資格的產品。 選取屬性型別並輸入合格條件。 禁止使用的字元包括： `[ ] < > >>` （兩個連續的「大於」符號），用來指定範本中的欄名稱、範本中的修飾元名稱以及Bulksheets中[!UICONTROL Parent Product Grouping]欄的層級分隔符號。

您可以包含最多八個產品群組（層級），包括&quot;[!UICONTROL All Products]&quot; （層級1）。 每個層級可包含多個產品群組，但它們必須屬於相同的屬性型別（例如「條件」）。

>[!NOTE]
>
>* （[!DNL Google Ads]僅限） [!UICONTROL Channel]可能的值為&quot;[!UICONTROL Local]&quot;或&quot;[!UICONTROL Online]&quot;，[!UICONTROL ChannelExclusivity]可能的值為&quot;[!UICONTROL SingleChannel]&quot;和&quot;[!UICONTROL MultiChannel]&quot;。
>* 當您從[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]檢視中的[!UICONTROL Product Groups]索引標籤為廣告群組建立第二層（子項）產品群組時，系統會使用預設廣告群組競標自動建立另一個名為「[!UICONTROL Everything Else]」的產品群組。 但是，使用庫存摘要範本時，會排除&quot;[!UICONTROL Everything Else]&quot;產品群組。
>* 如果您包含多個層級，且最終（最高編號）層級沒有可用值，則次高層級會用作可競標產品群組。 例如，如果您包含五個層級，但層級5沒有可用的值，則層級4會作為可競標的產品群組（單位）。 但是，如果中間層沒有可用的值，則會忽略該列。 例如，如果您包含五個層級，而層級5有一個值，但層級4沒有，則會忽略第4列。
