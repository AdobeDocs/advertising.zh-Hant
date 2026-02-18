---
title: 標準創意設定
description: 參考標準創意作品的設定。
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: 8a304eb74549ca1a81257e9f672d311d39987b79
workflow-type: tm+mt
source-wordcount: '2106'
ht-degree: 0%

---

# 標準創意設定

設定因創意型別而異。

當您同時編輯多個創意內容時：

* 您可以同時或個別編輯每個創意內容的設定。 依預設，會選取您選擇的所有創意，而您指定的任何設定會套用至所有選取的創意。 若要編輯特定創意的設定，請在編輯欄位前取消選取每個不適用的創意內容；如有需要，請重複執行其他創意內容。

* 某些設定會套用至所有選取的創意內容。

## 彈性的HTML5創意設定 {#creative-settings-flexible-html5}

### 詳細資訊標籤

**Creative名稱：**&#x200B;創意的名稱。 預設會使用範本名稱或上傳的檔案名稱，但您可以變更名稱。 對於多個創意內容，您可以編輯個別創意內容名稱。 **秘訣：**&#x200B;在創意名稱中加入廣告大小，並使用在體驗中加入創意內容時可以輕鬆找到的名稱。

**語言：**&#x200B;您與創意內容建立關聯的每個廣告的預設語言。 上傳或編輯多個創意內容時，相同的值會套用至每個選取的創意內容。

**Creative大小：** （現有創意為唯讀）創意的尺寸。 如果創意內容中包含的任何影像大於指定大小，則會據此調整大小。

**[!UICONTROL Click Tags]：**&#x200B;允許從包含的橫幅廣告重新導向點選追蹤的變數。 變數名稱和對應的登陸頁面URL會從上傳的創意單位中填入，但您可以變更預設URL。 對於多個創意，您可以編輯個別的點按標籤。

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**標籤：** （選擇性）要套用至所有選取創意內容的任何標籤。 您可以在[!DNL Creative]內的不同檢視中依標籤篩選創意，並在[!UICONTROL Creative Label]中包含[!UICONTROL Custom Creative Report]維度。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立新標籤以套用至創作，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

### 屬性標籤

**\[所有適用於創意的預設內容屬性\]：**&#x200B;預設屬性名稱和值會從彈性的創意單位填入，但您可以選擇變更值。

>[!NOTE]
>
>將創意納入體驗時，您也可以使用自訂值來取代任何創意屬性的預設值。 編輯體驗內的屬性會建立父級創意的變體。

如需預先定義範本中可用屬性的相關資訊，請參閱[可用的彈性創意範本](#flexible-creative-templates-available)。

### 範本索引標籤

*僅限現有的創意內容*

創意內容適用的彈性HTML5範本檔案。

您可以選擇使用新範本取代現有範本，新範本的版面配置不同，但屬性名稱集與原始範本相同。 新範本必須是ZIP格式，最大為2 MB。 當創意在組合中時，使用該組合的所有體驗隨後都會使用來自新範本的版面。

當您更新具有子變數的父級創意內容的範本時，變數會隨範本版面配置的任何變更而更新，但變數的屬性值不會變更。

若要取代現有的廣告範本：

1. 按一下&#x200B;**更新範本**。

1. 按一下&#x200B;**繼續**。

1. 以下列任一方式指定ZIP檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   檢視[彈性廣告規格](#flexible-ad-spec)。

1. 視需要編輯新的[彈性HTML廣告設定](#flexible-ad-settings)。

1. 按一下&#x200B;**[!UICONTROL Edit]**

## HTML5創意設定 {#creative-settings-html5}

## 詳細資訊標籤

對於新創意，以下設定不在已命名的標籤上。

**Creative名稱：**&#x200B;創意的名稱。 對於新創意，預設會使用檔案名稱，但您可以變更名稱。 對於多個創意內容，您可以編輯個別創意內容名稱。 **秘訣：**&#x200B;在創意名稱中加入廣告大小，並使用在體驗中加入創意內容時可以輕鬆找到的名稱。

**語言：**&#x200B;您與創意內容建立關聯的每個廣告的預設語言。 上傳或編輯多個創意內容時，相同的值會套用至每個選取的創意內容。

**Creative大小：** （現有創意為唯讀）創意的尺寸。 如果創意內容中包含的任何影像大於指定大小，則會據此調整大小。

**[!UICONTROL Click Tags]：** (僅限靜態HTML5創意)允許從包含的橫幅廣告重新導向點選追蹤的變數。 變數名稱和對應的登陸頁面URL會從上傳的創意單位中填入，但您可以變更預設URL。 對於多個創意，您可以編輯個別的點按標籤。

>[!NOTE]
>
>將創意內容納入體驗時，您可以使用自訂登陸頁面URL來取代任何點選標籤的預設值，以產生基本創意內容的衍生。

**登陸頁面URL：** (僅有一個登陸頁面的簡單HTML5創意內容)您與創意內容建立關聯的每個廣告的預設登陸頁面URL。 此URL必須是以http://或https://開頭的有效URL。 其中可能包含您自己的協力廠商追蹤引數或[[!DNL Creative] 巨集](/help/creative/creative-macros.md)。

當您在套件中包含創意並將套件指派給體驗時，可以選擇變更登陸頁面URL，並為套件中的每個創意新增曝光和點選追蹤URL及JavaScript。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**標籤：** （選擇性）要套用至所有選取創意內容的任何標籤。 您可以在[!DNL Creative]內的各種檢視中依標籤篩選創意。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立新標籤以套用至創作，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

### 範本索引標籤

*僅限現有的靜態HTML5創意*

創意內容的HTML5範本檔案。

您可以選擇使用新範本取代現有範本，新範本的版面配置不同，但屬性名稱集與原始範本相同。 新範本必須是ZIP格式，最大為2 MB。 當創意在組合中時，使用該組合的所有體驗隨後都會使用來自新範本的版面。

當您更新具有子變數的父級創意內容的範本時，變數會隨範本版面配置的任何變更而更新，但變數的屬性值不會變更。

若要取代現有的廣告範本：

1. 按一下&#x200B;**更新範本**。

1. 按一下&#x200B;**繼續**。

1. 以下列任一方式指定ZIP檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   請參閱[HTML廣告規格](html5-creative-specification.md)。

1. 視需要編輯新的[HTML5廣告設定](#creative-settings-html5)。

1. 按一下&#x200B;**[!UICONTROL Edit]**

## 影像創意設定 {#creative-settings-image}

**Creative名稱：**&#x200B;創意的名稱。 對於新創意，預設會使用檔案名稱，但您可以變更名稱。 對於多個影像，您可以編輯個別的創意名稱。 **秘訣：**&#x200B;請使用將創意內容納入體驗時可以輕鬆找到的名稱。

**語言：**&#x200B;您與創意內容建立關聯的每個廣告的預設語言。 相同的值會套用至所有選取的影像。 將創意內容納入體驗時，您可以選擇自訂體驗的語言偏好設定。

**Creative大小：** （唯讀）上傳影像的尺寸。

**登陸頁面URL：**&#x200B;您與創意內容建立關聯的每個廣告的預設登陸頁面URL。 登入頁面URL必須是以http://或https://開頭的有效URL。 其中可能包含您自己的協力廠商追蹤引數或[[!DNL Creative] 巨集](/help/creative/creative-macros.md)。 相同的值會套用至所有選取的影像。

當您將創意內容納入套件組合，然後將套件組合指派給體驗時，您可以選擇變更登陸頁面URL，並為套件組合中的每個創意新增曝光次數和點選追蹤URL以及JavaScript 。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**標籤：** （選擇性）要套用至所有選取創意內容的任何標籤。 您可以在[!DNL Creative]內的各種檢視中依標籤篩選創意。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立新標籤以套用至創作，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

## 協力廠商創意設定 {#creative-settings-third-party}

**JavaScriptCode：**&#x200B;指向協力廠商廣告伺服器上創意的JavaScript標籤(以及不支援JavaScript的瀏覽器適用的替代標籤)。 指令碼可能會因廣告伺服器而異。 當您編輯多個創意時，相同的值會套用至每個選取的創意。

所有[可用的巨集](/help/creative/creative-macros.md)及其取代的資料都列在輸入欄位下方。 若要在標籤中插入其中一個巨集，請將游標停留在巨集描述上，然後按一下[複製到剪貼簿] ![ [複製到剪貼簿] ](/help/creative/assets/copy-to-clipboard.png "，然後將影像貼到標籤中您想要的位置。")

當您將此創意內容納入您實作為DSP廣告的體驗時，DSP會使用此標籤中的資訊來顯示廣告並追蹤其曝光次數和點按次數。 然後DSP會將標籤推送至廣告交換。 當廣告顯示並按一下時，廣告伺服器、DSP和[!DNL Creative]會追蹤事件。

**[!UICONTROL Advertiser]：** （唯讀）資料庫可用的廣告商。

**Creative名稱：**&#x200B;創意的名稱。 **秘訣：**&#x200B;請使用將創意內容納入體驗時可以輕鬆找到的名稱。

**Creative大小：** （現有廣告為唯讀）創意的尺寸。 如需新創意，請從標準廣告大小的清單中選取。

**語言：**&#x200B;您與創意內容建立關聯的每個廣告的預設語言。

**登陸頁面URL：**&#x200B;用來驗證您與創意內容建立關聯的每個廣告的登陸頁面URL。 協力廠商廣告伺服器會決定每個廣告的實際登陸頁面。

**標籤：** （選擇性）要套用至所有選取創意內容的任何標籤。 您可以在[!DNL Creative]內的各種檢視中依標籤篩選創意。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立新標籤以套用至創作，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

## 視訊創意設定 {#creative-settings-video}

**Creative資產名稱：**&#x200B;創意的名稱。 對於新創意，預設會使用檔案名稱，但您可以變更名稱。 對於多個影像，您可以編輯個別的創意名稱。 **秘訣：**&#x200B;請使用將創意內容納入體驗時可以輕鬆找到的名稱。

**持續時間：** （唯讀）自動填入的視訊持續時間。

**語言：**&#x200B;您與創意內容建立關聯的每個廣告的預設語言。 相同的值會套用至所有選取的影像。 將創意內容納入體驗時，您可以選擇自訂體驗的語言偏好設定。

**登陸頁面URL：**&#x200B;您與創意內容建立關聯的每個廣告的預設登陸頁面URL。 登入頁面URL必須是以http://或https://開頭的有效URL。 其中可能包含您自己的協力廠商追蹤引數或[[!DNL Creative] 巨集](/help/creative/creative-macros.md)。 相同的值會套用至所有選取的影像。

當您將創意內容納入套件組合，然後將套件組合指派給體驗時，您可以選擇變更登陸頁面URL，並為套件組合中的每個創意新增曝光次數和點選追蹤URL以及JavaScript 。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**標籤：** （選擇性）要套用至所有選取創意內容的任何標籤。 您可以在[!DNL Creative]內的各種檢視中依標籤篩選創意。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立新標籤以套用至創作，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

>[!MORELIKETHIS]
>
>* [將標準創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-standard.md)
>* [編輯標準創意](/help/creative/creative-libraries/creative-edit-standard.md)
>* [可用於追蹤URL的巨集](/help/creative/creative-macros.md)
