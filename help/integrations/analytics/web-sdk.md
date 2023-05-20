---
title: 使用 [!DNL Last Event Service] JavaScript庫 [!DNL Web SDK]
description: 瞭解從使用 [!DNL Analytics] [!DNL visitorAPI] 庫到 [!DNL Experience Platform] [!DNL Web SDK] 庫 [!DNL Analytics for Advertising] 執行。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 使用 [!DNL Last Event Service] 帶有Adobe Experience Platform的JavaScript庫 [!DNL Web SDK]

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

如果貴組織使用傳統Adobe Analytics `visitorAPI.js` 用於資料收集的庫，您可以選擇切換到 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 庫(`alloy.js`)，允許您通過 [!DNL Edge Network]。

的 [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript庫原樣記錄查看和點擊查看事件，並使用補充ID(`SDID`)。 的 [!DNL Web SDK] 但是，庫不提供 [!DNL stitch ID]。 使用 [!DNL Web SDK] 為 [!DNL Analytics for Advertising]，您需要修改1) [!DNL Last Event Service] 在網頁上使用的標籤和2 [!DNL Web SDK] `sendEvent` 命令。

## 步驟1:編輯 [!DNL Last Event Service] 要生成的標籤 `[!DNL StitchID]`

在 [!DNL Analytics for Advertising] [!DNL Last Event Service] 在網頁上使用的標籤，添加代碼以生成 `[!DNL StitchID]` 使用隨機ID生成器。

**舊標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**新標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 步驟2:使用 [!DNL Web SDK] 發送 [!DNL StitchID] 作為XDM資料 [!DNL Analytics]

在您的 [!DNL Web SDK] `sendEvent` 命令 [!DNL StitchID] 至 [!DNL Experience Edge] 如 [!DNL Experience Data Model] (XDM)資料 [!DNL Analytics]。<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 將值用作 `SDID`。

**要添加的屬性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**示例：**

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
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript代碼 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

