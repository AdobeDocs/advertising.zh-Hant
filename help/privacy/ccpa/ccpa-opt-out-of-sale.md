---
title: Adobe Advertising對加州消費者隱私法的支援&#58；消費者選擇退出銷售支援
description: 瞭解如何支援擷取消費者選擇退出銷售的要求。
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 788b4ddb9b690a3f0bac93ec9b5145fc7a324719
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Adobe Advertising對加州消費者隱私法的支援：消費者選擇退出銷售支援

適用於Adobe Advertising Demand Side Platform (DSP)的&#x200B;**

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需《加州消費者隱私法》的相關建議，請諮詢您的法律顧問。

加州消費者隱私法(CCPA)是加州的最新隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供有關個人資訊的新權利，並對在加州經營業務的特定實體施加資料保護責任。 CCPA給予消費者存取及刪除其資料的權利，且消費者有權選擇退出能將個人資訊「銷售」給第三方的某些活動。

企業能決定哪些個人資料要交由Adobe Experience Cloud代表您處理和儲存。

身為您的服務提供者，Adobe Advertising會支援您的企業履行CCPA所規範的義務，這些義務適用於使用Adobe Advertising產品和服務，包括管理消費者存取和刪除個人資訊的請求，以及管理消費者選擇退出個人資訊銷售的請求。

本檔案說明Adobe Advertising Demand Side Platform (DSP)身為服務提供者，如何支援消費者選擇退出「個人資訊銷售」的權利，因為CCPA會定義每個詞語。 其中包括如何向Adobe Advertising傳達選擇退出銷售請求，以及如何擷取您組織的選擇退出銷售請求報表的資訊。

如需[!DNL Advertising Search, Social, & Commerce]、Advertising Creative和[!DNL Advertising DCO]如何支援消費者的個人資訊存取和刪除許可權的詳細資訊，請參閱[加州消費者隱私法的Adobe Advertising支援：消費者資料存取和刪除支援](/help/privacy/ccpa/ccpa-access-delete.md)。

如需CCPA適用Adobe隱私權服務的詳細資訊，請參閱[Adobe隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## 將消費者選擇退出銷售的請求傳達給Adobe Advertising

您可以使用下列任一項，傳達消費者選擇退出銷售的請求：

* 在Advertising DSP中建立的CCPA選擇退出銷售區段
* ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API

### 方法1：使用Advertising DSP中的[!UICONTROL CCPA Opt-Out-of-Sale]區段傳達CCPA選擇退出銷售請求

>[!NOTE]
>
>使用者會無限期留在CCPA選擇退出銷售區段中。

1. 在[https://advertising.adobe.com/](https://advertising.adobe.com/)登入Advertising DSP中的廣告商帳戶。
1. [建立CCPA選擇退出銷售區段，並實作區段畫素以擷取選擇退出請求](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2：使用Adobe Experience Platform Privacy Service API通訊CCPA選擇退出銷售請求

*廣告商只指派了Adobe Experience Cloud組織ID*

1. 部署JavaScript程式庫以擷取客戶的Cookie。 所有Adobe Experience Cloud解決方案都使用相同的資料庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >請求某些Adobe Experience Cloud解決方案不需要JavaScript資料庫，但請求給Adobe Advertising則需要它。

   您應該將資料庫部署在客戶可以提交選擇退出銷售請求的網頁上，例如您公司的隱私權入口網站。 資料庫可協助您擷取Adobe Cookie （名稱空間ID： `gsurferID`），以便您可以透過Adobe Experience Platform Privacy Service API將這些身分識別作為選擇退出銷售請求的一部分提交。

1. 識別您的Experience Cloud組織ID，並確定其已連結至您的Adobe Advertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，通常會加上「@AdobeOrg」。 大部分Experience Cloud客戶已指派組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道您的組織ID，或不確定其是否已布建，請聯絡您的Adobe帳戶團隊。 您需要組織識別碼，才能使用`imsOrgID`名稱空間將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請聯絡貴公司的Adobe Advertising代表，確認貴組織的所有Adobe Advertising帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search, Social, & Commerce]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）都與您的Experience Cloud組織ID連結。

1. 使用Adobe Experience Platform Privacy Service API代表消費者[提交選擇退出銷售請求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html?lang=zh-Hant)給Adobe Advertising，並檢查現有請求的狀態。

   如需選擇退出銷售的請求範例，請參閱下文附錄。

   >[!NOTE]
   >
   >如果您的企業有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 但是，您可以向多個Adobe Advertising子解決方案（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]和[!DNL DCO]）提出一個API請求，每個子解決方案使用一個帳戶。

您必須執行上述所有步驟，才能獲得Adobe Advertising的支援。 如需有關這些事項以及您需要使用Adobe Experience Platform Privacy Service執行的其他相關工作的詳細資訊，以及尋找必要專案的位置，請參閱[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant)。

## 擷取提交選擇退出銷售請求的消費者報表

Adobe Advertising會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報表。 每個報表都可壓縮為GZIP格式，以定位點分隔的文字檔案提供。 資料會合併使用Advertising DSP中建立的CCPA選擇退出銷售區段擷取的請求，以及透過Privacy Service API提交的任何提交。 在CCPA選擇退出銷售區段中擷取的使用者ID會依區段和廣告商識別。 報告產生於前一個月每個月的第一天。 例如，6月的每月使用者清單可在7月1日取得。

您可以從Advertising DSP中或使用Advertising DSP [!DNL Trafficking API]，擷取前三個月建立的每月報表連結。 每個連結的有效期為七天，但每當客戶嘗試擷取連結時，都會重新整理。

### 方法1：在Advertising DSP中擷取消費者選擇退出銷售報表

1. 在[https://advertising.adobe.com/](https://advertising.adobe.com/)登入Advertising DSP中的廣告商帳戶。
1. [擷取報告](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2：使用Advertising DSP [!DNL Trafficking API]擷取消費者選擇退出銷售報告

此功能適用於使用[!DNL Trafficking API]的組織。 如需詳細資訊，請參閱[!DNL Trafficking API]的檔案。<!-- Add link to API doc once it's published. -->

如果貴組織未使用[!DNL Trafficking API]，但想要瞭解更多資訊，請聯絡您的Adobe客戶團隊。

## 附錄：Privacy Service API使用者的範例[!UICONTROL CCPA Opt-Out-of-Sale]要求

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
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

其中，根據[Privacy Service API規格](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/appendix)：

* `"namespace": "AdCloud"`表示`AdCloud` Cookie空間，而對應的值是從`AdobePrivacy.js`擷取之客戶的Cookie ID
* `"include": ["adCloud"]`指出此要求適用於產品Adobe Advertising
