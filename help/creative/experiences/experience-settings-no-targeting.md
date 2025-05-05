---
title: 非目標體驗的設定
description: 請參閱不含決策樹定位之廣告體驗的所有設定說明。
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: d2db928068153c0ce26cc51fa79f45cbb3c61f18
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 0%

---

# 非目標體驗的設定

*已關閉的Beta*

## [!UICONTROL Experience basics]節

**[!UICONTROL Advertiser]：** （現有體驗為唯讀）將對體驗中包含的創意專案出價的廣告商。 儲存體驗後，您就無法變更廣告商。

**[!UICONTROL Experience Name]：**&#x200B;體驗的唯一名稱。 **秘訣：**&#x200B;在Advertising DSP或其他DSP中使用體驗作為廣告時，請使用可以輕鬆找到的名稱。

**[!UICONTROL Creative Library]：** （現有體驗為唯讀）要用於體驗的單一創意程式庫。 儲存體驗後，就無法變更資料庫。

## [!UICONTROL Default creatives]節

**\[指定的預設創意\]：**&#x200B;當瀏覽器無法顯示指派給體驗的創意時(例如當瀏覽器未啟用JavaScript或廣告伺服器因延遲而無法個人化廣告時)，所使用的預設影像創意。 針對體驗適用的每個廣告大小包含一個影像創意。 您的選擇決定了可用於體驗的創意大小。<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

對於沒有決策樹定位的體驗，您可以在[!UICONTROL Tag Manager]內以相同大小的創意內容覆寫預設創意內容。

* 若要新增具有不同維度的預設創作，請按一下&#x200B;**[!UICONTROL + Add Sizes]**，從右側窗格中選取要新增的每個創意旁邊的核取方塊，然後按一下&#x200B;**[!UICONTROL Add Creatives]**。

* 若要刪除預設創意，請將游標停留在創意縮圖上，然後按一下![刪除](/help/creative/assets/delete.png "刪除")。

* 若要刪除所有預設創意，請按一下![刪除](/help/creative/assets/delete.png "刪除") **[!UICONTROL Delete all]**。

* 若要顯示或隱藏右邊的[創意內容]窗格，請按一下右邊窗格右上角的![顯示/隱藏](/help/creative/assets/hide-show-creatives.png "顯示/隱藏")。

## [!UICONTROL Targeting]節

**[!UICONTROL Targeting]：** （現有體驗為唯讀）當您未使用決策樹啟用鎖定目標時，則不適用；請停用此選項。

**[!UICONTROL Dynamic ads]：** （現有體驗為唯讀）表示體驗包含動態廣告。 **注意：**&#x200B;體驗可以包含所有標準廣告或所有動態廣告。

**[!UICONTROL Language Targeting]：** （僅含標準廣告的體驗；選擇性；現有體驗為唯讀）檢查使用者的瀏覽器語言設定，並在可以使用指定語言的創意內容時，使用該語言顯示創意內容。 無法使用瀏覽器指定語言的創意內容時，將改用[!UICONTROL Preferred language]設定。 儲存體驗後，便無法變更此設定。

**[!UICONTROL Preferred language]：** （僅具有標準廣告的體驗；現有體驗為唯讀）從體驗建立的所有廣告的語言，啟用[!UICONTROL Language Targeting]時除外。 儲存體驗後，便無法變更此設定。

## [!UICONTROL Advanced]節

**Data Pass：** （僅限使用動態廣告的體驗；選用）根據DSP、發佈者或合作夥伴在曝光時即時傳遞的特定索引鍵/值組來鎖定使用者。 您最多可以指定5個資料傳遞金鑰（引數）。<!-- May move this to just within the decision tree. -->

當您為特定創意大小建立廣告體驗標籤時，在此欄位中指定的每個鍵都會附加為標籤中的巨集。 在DSP中實作標籤作為廣告之前，請輸入標籤內每個索引鍵/值組的值。

**半徑：** （僅限使用動態廣告的體驗；選擇性）目標饋送檔案中指定的美國郵遞區號的半徑；選取從0哩到200哩的半徑。 用來為體驗建立動態廣告的摘要檔案必須包含一個[!UICONTROL ZIP]欄<!-- or a user-named column mapped to a ZIP column -->，且該檔案中的每個產品列都有值。 例如，半徑為10哩時，可向95110徑10哩內的使用者顯示95110中可用產品的廣告（由使用者的IP位址決定）。

**RT畫素：** （僅具有動態廣告的體驗；選用） [!UICONTROL Creative]將畫素重新定位到潛在目標。 當您在決策樹中設定目標時，可以包含一個RT畫素目標節點層級。 對於每個節點，您將指定要定位的畫素，以及在指定的創意組合中顯示創意所需的畫素屬性值。 如果您未在此欄位中指定畫素，您仍可在決策樹中指定畫素。<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]：**<!-- should be "Labels" --> （選用）任何套用至體驗的[!DNL Creative]特定標籤。 您可以在體驗<!-- sic -->檢視中依標籤篩選體驗。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立要套用的新標籤，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

**[!UICONTROL Impression Tracking URL]：** （選用）要附加至從體驗建立之任何廣告的登陸頁面URL的協力廠商曝光追蹤URL。 您最多可以包含五個URL。 若要新增其他URL，請按一下![圖示](/help/creative/assets/create.png) **[!UICONTROL Add More]並輸入URL。

輸入URL後，頁面下方會列出所有[可用的巨集](/help/creative/creative-macros.md)及其取代的資料。 若要在URL中插入其中一個巨集，請將游標停留在巨集描述上，然後按一下[複製到剪貼簿] ![&#128279;](/help/creative/assets/copy-to-clipboard.png " [複製到剪貼簿] ")，然後將巨集貼到URL欄位中您想要的任何位置。

>[!NOTE]
>
>* [!DNL Creative]會自動在登陸頁面URL加上自己的曝光追蹤標籤作為前置詞。
>* 您可以為體驗中的任何創意內容覆寫此URL。
>* 您也可以在[!UICONTROL Client JS]欄位中輸入協力廠商JavaScript曝光數追蹤程式碼

**[!UICONTROL Click Tracking URL]：** （選用） （選用）要附加至登陸頁面URL的協力廠商點選追蹤URL。 您最多可以包含五個URL。 若要新增其他URL，請按一下![圖示](/help/creative/assets/create.png) **[!UICONTROL Add More]**&#x200B;並輸入URL。

輸入URL後，頁面下方會列出所有[可用的巨集](/help/creative/creative-macros.md)及其取代的資料。 若要在URL中插入其中一個巨集，請將游標停留在巨集描述上，然後按一下[複製到剪貼簿] ![&#128279;](/help/creative/assets/copy-to-clipboard.png " [複製到剪貼簿] ")，然後將巨集貼到URL欄位中您想要的任何位置。

>[!NOTE]
>
>* [!DNL Creative]會自動在登陸頁面URL加上自己的曝光追蹤標籤作為前置詞。
>* 您可以為體驗中的任何創意<!-- creative bundle for targeted experiences -->覆寫此URL。

**[!UICONTROL Client JS]：** （選擇性）下列任一專案：

* （當廣告商使用符合OBA規範的廠商進行廣告時） JavaScript程式碼會指向允許使用者選擇退出線上行為目標定位(OBA)的廣告覆蓋。

* 要附加至登陸頁面的任何第三方JavaScript曝光追蹤程式碼。 **注意：**&#x200B;您也可以在[!UICONTROL Impression Tracking URL]欄位中輸入協力廠商曝光追蹤URL。

>[!MORELIKETHIS]
>
>* [建立沒有決策樹定位的體驗](experience-create-no-targeting.md)
>* [編輯沒有決策樹定位的體驗](experience-edit-no-targeting.md)
>* [可用於追蹤URL的巨集](/help/creative/creative-macros.md)
>* [手動建立適用創意大小的廣告標籤](experience-tag-create-manually.md)
>* [將創意內容指派給體驗的廣告標籤，而不需鎖定目標](experience-tag-assign-creatives.md)
>* [自訂體驗的追蹤URL而不鎖定目標](experience-tracking-urls-no-targeting.md)
>* [自訂體驗的創意最佳化和排程，而不需要鎖定目標](experience-optimization-scheduling-no-targeting.md)
