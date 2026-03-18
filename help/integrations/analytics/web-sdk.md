---
title: 搭配 [!DNL Last Event Service] 使用 [!DNL Web SDK]JavaScript資料庫
description: 瞭解從使用 [!DNL Analytics] [!DNL visitorAPI]資料庫切換到您 [!DNL Experience Platform] [!DNL Web SDK]實作的 [!DNL Analytics for Advertising] 資料庫的步驟。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# 搭配Adobe Experience Platform [!DNL Last Event Service]使用[!DNL Web SDK] JavaScript資料庫

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

如果您的組織使用舊版Adobe Analytics `visitorAPI.js`資料庫進行資料彙集，您可以選擇切換為使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)資料庫(`alloy.js`)，讓您透過[!DNL Edge Network]與各種Experience Cloud服務互動。

[!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript程式庫（依原樣）會記錄檢視和點進事件，並使用補充ID (`SDID`)將其彙整至關聯的轉換。 但[!DNL Web SDK]資料庫未提供[!DNL stitch ID]。 若要針對[!DNL Web SDK]使用[!DNL Analytics for Advertising]，您必須修改1)您在網頁上使用的[!DNL Last Event Service]標籤，以及2)您的[!DNL Web SDK] `sendEvent`命令。

## 步驟1：編輯您的[!DNL Last Event Service]標籤以產生`[!DNL StitchID]`

在您用於網頁的[!DNL Analytics for Advertising] [!DNL Last Event Service]標籤中，新增程式碼，以使用隨機ID產生器（隨附於程式庫中）產生`[!DNL StitchID]`。

**舊版標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**新標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## 步驟2：使用[!DNL Web SDK]傳送[!DNL StitchID]做為[!DNL Analytics]的XDM資料

在您的[!DNL Web SDK] `sendEvent`命令中插入以下屬性，將[!DNL StitchID]以[!DNL Experience Edge]的[!DNL Experience Data Model] (XDM)資料形式傳送至[!DNL Analytics]。<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics]使用值做為`SDID`。

要新增的&#x200B;**屬性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**範例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [的 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)JavaScript程式碼
