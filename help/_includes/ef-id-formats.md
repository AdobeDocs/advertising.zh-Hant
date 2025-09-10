---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

>[!NOTE]
>
>EF ID區分大小寫。 如果[!DNL Analytics]或Customer Journey Analytics實作強制將URL追蹤轉換為小寫，則Adobe Advertising無法辨識EF ID。 這會影響Adobe Advertising競標和報告，但不會影響[!DNL Analytics]或Customer Journey Analytics內的Adobe Advertising報告。

#### [!DNL Google Ads]個搜尋廣告

```
{gclid}:G:s
```

其中：

* `gclid`是[!DNL Google Click ID] (GCLID)。
* `s`是網路型別（搜尋時為「s」）。

#### [!DNL Microsoft Advertising]個搜尋廣告

```
{msclkid}:G:s
```

其中：

* `msclkid`是[!DNL Microsoft Click ID] (MSCLKID)。
* `s`是網路型別（搜尋時為「s」）。

#### 在其他搜尋引擎上顯示廣告和搜尋廣告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising訪客ID*>是每個訪客的唯一識別碼（例如UhKVaAABCkJ0mDt）。 也稱為&#x200B;*瀏覽者ID*。

* &lt;*timestamp*>是YYYYYMMDDHHMMSS格式的時間(例如20190821192533 for Year 2019， Month 08， Day 21， Time 19:25:33)。

* &lt;*頻道型別*>是負責點選或曝光的頻道型別：

   * `d`點選DSP顯示廣告（顯示點進）
   * `i`用於DSP顯示廣告（顯示瀏覽次數）的曝光
   * `s`搜尋廣告的點按（搜尋點進）。

範例`EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
