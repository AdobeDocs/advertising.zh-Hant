---
title: Adobe對《加利福尼亞消費者隱私法》的廣告支援：消費者選擇不銷售支援
description: 瞭解對捕獲消費者選擇退出銷售請求的支援。
feature: CCPA
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe對加利福尼亞消費者隱私法的廣告支援：消費者選擇退出銷售支援

*對於Adobe廣告Demand Side Platform(DSP)*

>[!IMPORTANT]
>
>本檔案內容不是法律意見，不是代替法律意見。 請咨詢您的法律顧問，以獲取有關《加利福尼亞消費者隱私法》的建議。

《加利福尼亞消費者隱私法》(CCPA)是加利福尼亞新的隱私法，自2020年1月1日起生效。 CCPA為加利福尼亞州居民提供了有關其個人資訊的新權利，並對在加利福尼亞開展業務的某些實體規定了資料保護責任。 CCPA向消費者提供了訪問和刪除其資料的權利，以及選擇不參與某些符合向第三方「銷售」個人資訊資格的活動的權利。

作為企業，您將確定Adobe Experience Cloud代表您處理和儲存的個人資料。

作為您的服務提供商，Adobe廣告為您的企業提供支援，以履行CCPA規定的義務，這些義務適用於Adobe廣告產品和服務的使用，包括管理消費者訪問和刪除個人資訊的請求以及管理消費者選擇不銷售個人資訊的請求。

本文檔介紹Adobe廣告Demand Side Platform(DSP)作為服務提供商，如何支援消費者選擇不「銷售」「個人資訊」的權利，因為每個術語都由CCPA定義。 它包括有關如何將選擇退出銷售請求傳達給Adobe廣告以及如何檢索貴組織選擇退出銷售請求的報告的資訊。

有關如何 [!DNL Advertising Search, Social, & Commerce];廣告創意；和 [!DNL Advertising DCO] 支援消費者的個人資訊訪問和刪除權限，請參閱 [Adobe對加利福尼亞消費者隱私法的廣告支援：使用者資料存取和刪除支援](/help/privacy/ccpa/ccpa-access-delete.md)。

有關CCPA的Adobe隱私服務的詳細資訊，請參見 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html)。

## 將消費者選擇不可銷售的請求傳達給Adobe廣告

您可以使用以下兩種方法來傳遞消費者選擇退出銷售的請求：

* 一個CCPA選擇不出售分部，該分部創DSP建
* Adobe Experience Platform Privacy Service

### 方法1:使用 [!UICONTROL CCPA Opt-Out-of-Sale] 廣告分部DSP

>[!NOTE]
>
>用戶無限期地留在CCPA選擇不銷售的部門。

1. 登錄廣告商的帳戶，DSP地址 [https://advertising.adobe.com/](https://advertising.adobe.com/)。
1. [建立CCPA選擇退出銷售段，並實施段像素以捕獲選擇退出請求](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2:使用Adobe Experience Platform Privacy ServiceAPI傳遞CCPA選擇不銷售請求

*廣告商僅分配了Adobe Experience Cloud組織ID*

1. 部署JavaScript庫以檢索客戶的Cookie。 同一個圖書館， `AdobePrivacy.js`，用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript庫，但對Adobe廣告的請求需要它。

   您應在網頁上部署庫，客戶可以從該網頁上提交選擇退出銷售請求，如您公司的隱私門戶。 庫可幫助您檢索AdobeCookie(命名空間ID: `gsurferID`)，以便您可以通過Adobe Experience Platform Privacy ServiceAPI將這些身份作為選擇退出銷售請求的一部分提交。

1. 確定您的Experience Cloud組織ID，並確保它連結到您的Adobe廣告帳戶。

   Experience Cloud組織ID是附加有「@AdobeOrg」的24個字元的字母數字字串。 大多數Experience Cloud客戶已分配了組織ID。 如果您的營銷團隊或內部Adobe系統管理員不知道您的組織ID，或者不確定是否已預配，請通過gdprsupport@adobe.com與Adobe客戶服務部聯繫。 您需要組織ID才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >聯繫您公司的Adobe廣告代表，確認您公司的所有Adobe廣告帳戶，包括 [!DNL DSP] 或者廣告商， [!DNL Search, Social, & Commerce] 帳戶和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結到您的Experience Cloud組織ID。

1. 使用Adobe Experience Platform Privacy ServiceAPI [提交選擇退出銷售請求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 代表消費者Adobe廣告，並檢查現有請求的狀態。

   有關選擇退出銷售請求的示例，請參閱下面的附錄。

   >[!NOTE]
   如果您的企業具有多個Experience Cloud組織ID，則必須為每個API請求發送單獨的API請求。 但是，您可以向多個Adobe廣告子解決方案發出一個API請求([!DNL Search, Social, & Commerce]。 [!DNL Creative]。 [!DNL DSP], [!DNL DCO])，每個子解決方案有一個帳戶。

所有這些步驟都是獲得Adobe廣告支援所必需的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## 檢索提交選擇退出銷售請求的消費者的報告

Adobe廣告生成客戶已提交的ID的月度報告，這些ID要求客戶選擇不銷售。 每個報告都可以作為以制表符分隔的文本檔案壓縮為GZIP格式。 這些資料整合了使用CCPA選擇不可銷售段捕獲的請求，這些段是在廣告中建立的，DSP以及通過Privacy ServiceAPI提交的任何資料。 在CCPA選擇退出銷售分段中捕獲的用戶ID由分段和廣告商標識。 在上個月的每月一日生成報告。 例如，6月的月度用戶清單在7月1日可用。

您可以檢索到前三個月中建立的月度報告的連結，這些連結可以從「廣告」中DSP或通過使用「廣告」DSP [!DNL Trafficking API]。 每個連結的有效期為七天，但每次客戶嘗試檢索一個連結時都會刷新。

### 方法1:在廣告中檢索消費者選擇不可銷售報DSP告

1. 登錄廣告商的帳戶，DSP地址 [https://advertising.adobe.com/](https://advertising.adobe.com/)。
1. [檢索報告](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2:使用廣告檢索消費者選擇不可銷售報DSP告 [!DNL Trafficking API]

此功能可供使用 [!DNL Trafficking API]。 請參閱 [!DNL Trafficking API] 的子菜單。

如果您的組織不使用 [!DNL Trafficking API] 但有興趣瞭解更多資訊，請與Adobe客戶團隊聯繫。

## 附錄：示例 [!UICONTROL CCPA Opt-Out-of-Sale] 請求Privacy ServiceAPI用戶

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

其中：

* `"namespace": "AdCloud"` 指示 `AdCloud` cookie空間，相應值是從中檢索到的客戶cookie ID `AdobePrivacy.js`
* `"include": ["AdCloud"]` 指示請求適用於Adobe廣告
