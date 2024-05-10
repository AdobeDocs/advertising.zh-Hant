---
title: 管理詳細目錄摘要的廣告範本
description: 瞭解如何管理廣告範本，透過這些範本可處理您的詳細目錄資料，以管理帳戶結構並提供動態廣告。
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# 管理詳細目錄摘要的廣告範本

*[!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

上傳資料之前或之後，您可以建立搜尋引擎特定的廣告範本，以便處理您的資料。 您可以建立文字廣告和展開/延伸文字廣告的範本， [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 回應式搜尋廣告，以及 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 購物廣告。

您可以將每個範本與一個摘要檔案建立關聯， [!DNL Google Merchant Center] 帳戶，或 [!DNL Microsoft Merchant Center] 帳戶，而且您可以將多個範本與相同的摘要檔案或帳戶建立關聯。 廣告範本可包含變數，這些變數會由上傳檔案或帳戶中的實際資料欄取代。 在大多數情況下，變數也可包含 [修飾元群組](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) 您在「搜尋」、「Social」和「Commerce」中設定，以為資料檔案中的每個適用列建立多個廣告、關鍵字、促銷活動或廣告群組。 範本選項可讓您為廣告建立新的帳戶結構（行銷活動、廣告群組、關鍵字），或將廣告對應至現有的帳戶結構。

除了從頭開始建立新範本之外，您也可以複製現有範本並編輯現有範本，選擇建立新範本。

建立範本並將其與資料摘要檔案或商家中心帳戶建立關聯後，您就可以透過範本傳播檔案中的資料，以建立行銷活動資料和帳戶結構，選擇性地建立Bulksheet檔案以供稽核或立即張貼至廣告網路。

任何範本都可以啟動、暫停或刪除。 摘要資料只能透過作用中的範本自動傳播。 不過，您可以透過暫停的範本手動傳播資料。

## 建立、複製或編輯摘要範本

為文字和擴充/延伸文字廣告、回應式搜尋廣告建立個別範本， [!DNL Google Ads] 購物廣告，以及 [!DNL Microsoft Advertising] 購物廣告。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 執行下列任一項作業：

   * 若要從頭開始建立範本，請按一下 **[!UICONTROL Create/Clone]** 在資料表格上方的工具列中，然後選取適用的廣告網路。

   * 複製現有範本：

      1. 選取要複製的範本旁的核取方塊。

      1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Create/Clone]**，然後選取適用的廣告網路。

   * （若要編輯現有範本）按一下範本名稱旁的 ![檢視/編輯設定](/help/search-social-commerce/assets/settings.png "檢視/編輯設定").

1. 指定設定 [文字廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md)， [[!DNL Google Ads] 購物廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)，或 [[!DNL Microsoft Advertising] 購物廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md)：

   1. 在範本設定視窗頂端，指定範本名稱和適用的帳戶。

      複製現有範本時，請重新命名新範本，使從新範本建立的廣告不會與從來源範本建立的廣告相關聯。

   1. （可選）在左欄中，指定產品摘要檔案或商家中心帳戶，其資料將透過範本傳播：

      * （適用於產品摘要檔案）若要選取先前上傳的檔案，請按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下鍵") 並從可用的摘要檔案清單中選取檔案。 若要上傳新檔案，請輸入完整路徑和檔案名稱，或按一下 **[!UICONTROL Browse]** 以找出裝置或網路上的檔案，然後按一下 **[!UICONTROL Upload]**.

      * （針對同步商家中心帳戶）選取帳戶名稱。

      隨即顯示所選檔案或帳戶的欄。

   1. 在 **[!UICONTROL Account Structure]** 標籤，指定帳戶結構設定。

   1. （僅限文字廣告）按一下 **[!UICONTROL Keywords]** 標籤，並指定關鍵字設定。

   1. （僅限文字和回應式搜尋廣告）按一下 **[!UICONTROL Ads]** 標籤，然後執行下列任一項作業：

      >[!NOTE]
      >
      >* 您最多可以為每個標準文字廣告範本包含4個廣告變化範本、每個展開/延伸文字廣告範本包含5個廣告變化範本，以及每個回應式搜尋廣告範本包含3個廣告變化範本。
      >* 每個廣告群組最多可包含三個啟用的回應式搜尋廣告。
      >* 您無法編輯現有的標準文字廣告變化，且現有的範本不再產生標準文字廣告。
      >* 如果您變更廣告變化範本，則當您透過範本傳播資料時，可能會刪除現有廣告並建立新廣告。 [視廣告型別和廣告網路而定](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * 若要新增廣告變數，請執行以下操作：

         1. 按一下 **[!UICONTROL Add Ad Variation]** 若要建立文字廣告， **[!UICONTROL Add ETA Variation]** 若要建立擴充/延伸文字廣告，或 **[!UICONTROL Add RSA Variation]** 以建立回應式文字廣告。

            指定廣告型別後，您只能使用範本建立該廣告型別。

         1. 指定廣告設定。

            如果是回應式搜尋廣告，您可以包含3-15個標題和2-4個說明。

         1. （選擇性）若要以原始廣告復本欄位的文字，預先填入所有替代廣告復本欄位，請選取 **[!UICONTROL Prefill]**.

         1. （選擇性）若要將另一組廣告復本新增至廣告，並在原始廣告復本中的任何行超過傳播期間以資料取代的任何動態引數後超過最大長度時，可使用此組廣告，請按一下 **[!UICONTROL Add Alternate]**，然後新增替代值。

            >[!NOTE]
            >
            >* 如果 [!UICONTROL Prefill] 則替代欄位會預先填入原始欄位，您可以視需要加以編輯。
            >* 只有超過最大長度的廣告文案欄位會取代為替代值。 例如，如果只有原始標題或標題太長，則產生的廣告變化會使用替代標題或標題以及原始說明。 因此，請確保替代廣告文案與原始廣告文案結合時有意義。
            >* 如果原始廣告復本符合搜尋引擎的長度要求，則會捨棄替代廣告復本。
            >* 您最多可以為每個廣告文案欄位指定四個替代專案。

         * 若要編輯廣告變化，請執行下列動作：

            1. 編輯廣告設定。

               如果是回應式搜尋廣告，您可以包含3-15個標題和2-4個說明。

            1. （選擇性）若要以原始廣告復本欄位的文字，預先填入所有替代廣告復本欄位，請選取 **[!UICONTROL Prefill]**.

            1. （選擇性）若要將另一組廣告復本新增至廣告，並在原始廣告復本中的任何行超過傳播期間以資料取代的任何動態引數後超過最大長度時，可使用此組廣告，請按一下 **[!UICONTROL Add Alternate]**，然後新增替代值。

               >[!NOTE]
               >
               >* 如果 [!UICONTROL Prefill] 則替代欄位會預先填入原始欄位，您可以視需要加以編輯。
               >* 只有超過最大長度的廣告文案欄位會取代為替代值。 例如，如果只有原始標題或標題太長，則產生的廣告變化會使用替代標題或標題以及原始說明。 因此，請確保替代廣告文案與原始廣告文案結合時有意義。
               >* 如果原始廣告復本符合搜尋引擎的長度要求，則會捨棄替代廣告復本。
               >* 您最多可以為每個廣告文案欄位指定四個替代專案。

         * 若要移除廣告變數，請按一下 **[!UICONTROL Remove ETA Variation]** （適用於擴充/延伸文字廣告）或 **[!UICONTROL Remove RSA Variation]** （適用於回應式搜尋廣告）在廣告變化旁邊（如適用）。

   1. （僅限購物範本）按一下 **[!UICONTROL Product Groups]** 標籤，然後指定您要鎖定的產品群組相關資訊。

   1. （可選）按一下 **[!UICONTROL Feed Filters]** 定位字元，然後指定要在摘要檔案中傳輸的列。

   1. （可選）按一下 **[!UICONTROL Label Classifications tab]**，然後指定要指派給已建立之不同促銷活動元件的標籤分類值：

      1. 按一下旁邊的核取方塊 **[!DNL \[Component\] Label Classifications]**.

      1. 對於要指派給元件的每個標籤分類，請執行以下操作：

         1. 按一下 **[!UICONTROL Add Label Classification]**.

         1. 選取標籤分類，然後選取現有值或輸入新值。

1. 儲存範本：

   * 若要僅儲存範本，請按一下 **[!UICONTROL Save]**，然後按一下 **[!UICONTROL Save]** 再來一次。

   * 若要儲存範本並透過範本傳播指定的資料檔案，請按一下 **[!UICONTROL Save]**，然後按一下 **[!UICONTROL Save & Propagate]**.

## 變更摘要範本的狀態

您可以啟動任何已暫停的資料摘要範本，或暫停任何作用中的資料摘要範本。

>[!NOTE]
>
>您可以手動透過暫停的範本傳播資料，但資料不會自動透過它傳播。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 選取每個要變更其狀態的範本旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Change Status]**，然後按一下 **[!UICONTROL Activate]** 或 **[!UICONTROL Pause]**.

## 刪除摘要範本

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 選取要刪除的每個範本旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Delete]**.

1. 在確認訊息中，按一下 **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [關於使用庫存摘要自動化廣告管理](../inventory-feeds-about.md)
>* [文字廣告和回應式搜尋廣告範本設定](template-text-rsa.md)
>* [[!DNL Google Ads] 購物廣告範本設定](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] 購物廣告範本設定](template-microsoft-shopping.md)
>* [透過範本傳播摘要資料](../feed-data-propagate.md)
