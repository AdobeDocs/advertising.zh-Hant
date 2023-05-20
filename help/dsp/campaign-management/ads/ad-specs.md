---
title: 廣告規格
description: 參考一般廣告和發佈者特定的廣告規範。
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# 支援的廣告類型的規範

## 視頻廣告（預卷、CTV和通用視頻）

### 支援的螢幕

預設情況下，在台式、移動和連接的電視設備上提供廣告。 設備目標可用於調整遞送。

### 支援的第三方廣告伺服器

您可以使用標籤頁 [!DNL DCM]。 [!DNL Flashtalking]。 [!DNL Innovid], [!DNL Sizmek]。 有關受支援供應商的完整清單，請參見[認證廣告服務合作夥伴](certified-ad-servers.md)&quot;

### 高清視頻資產要求（必需）

**視頻標籤類型：** VPAID 2.0 JavaScript或VAST(CTV)。 所有VPAID廣告單元必須 [VPAID 2.0規範](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) 由互動式廣告局(IAB)定義。

**視頻編解碼器：** MP4/H.264

**解決方案：** 1280x720(720p),1920x1080(1080p)

**比特率：** 1500-2500 kbps(720p),2500-3500 kbps(1080p)

**H.264配置檔案/級別：** 高調，3.1級，720p;1080p的高級別4.0

**視頻幀速率：** 29.970 fps（通常稱為30 fps）（NTSC國家/地區）、25 fps（PAL國家/地區）、23.976 fps（通常稱為24 fps）（膠片外觀內容）

**視頻顏色空間：** 4:2:0 YUV色度子採樣

**視頻隔行：** 逐行掃描，即隔行掃描。 無場內運動（混合幀）或交錯。

**領導者(Slate):** 不允許

**音頻編解碼器：** AAC-LC或HE-AACv1

**音頻比特率：** AAC-LC為128-192 kbps,HE-AACv1為64-128 kbps

**音頻通道：** 雙聲道立體聲混音

**音頻採樣率：** 根據源材料，44.1 kHz或48 kHz

**音頻級別：** 根據ATSC A/85，美國有24個LKFS(+/- 2.0 dB);根據EBU R128在歐盟中為23個LUFS(+/- 1.0)

#### 連接電視廣告的其他發佈者要求

* **A+E網路：** 請參閱A+E網路 [ad規範](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **發現：** 查看發現 [ad規範](/help/dsp/assets/discovery-networks-ad-specs.pdf)。

* **迪士尼(包括 斛律):** 看迪士尼 [ad規範](https://hulu.disneyadsales.com/ad-products/video-commercial/)。

* **HBO Max:** 參見HBO Max [ad規範](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx)。

* **NBCUniversal:**

   * [數字視頻](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [直播](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [孔雀](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **派拉蒙：** 查看派拉蒙 [ad規範](https://www.paramount.com/digital-ads)。

## 顯示廣告

### 支援的螢幕

預設情況下，在台式機和移動設備上提供廣告。 設備目標可用於調整遞送。

### 支援的檔案類型

**影像：** GIF、JPG/JPEG、巴布亞紐幾內亞

**HTML5:** 映像檔案類型：GIF、JPG/JPEG、PNG、SVG

### 映像資產要求（必需）

支援通用顯示。

**建議的廣告大小：** 120x60、160x600、180x150、300x50、300x100、300x1050、300x250、300x600、320x50、320x480、480x60、640x480、88x31、728x90、970x250、970x90

**支援的第三方廣告伺服器：** 您可以使用標籤頁 [!DNL DCM]。 [!DNL Flashtalking]。 [!DNL Innovid], [!DNL Sizmek]。 有關受支援供應商的完整清單，請參見[認證廣告服務合作夥伴](certified-ad-servers.md)&quot;

## 音頻廣告

### 支援的螢幕

台式機、移動設備、平板電腦、智慧揚聲器和連接的電視

### 支援的第三方廣告伺服器

您可以使用標籤頁 [!DNL DCM]。 [!DNL Flashtalking]。 [!DNL Innovid], [!DNL Sizmek]。 有關受支援供應商的完整清單，請參見[認證廣告服務合作夥伴](certified-ad-servers.md)&quot;

### 音頻資產要求（必需）

**檔案類型：** MP3、OGG、AAC

**領導人（名單）:**  不允許

**最大檔案大小：** 2 MB

**比特率：** 128

**檔案長度：** 0-60年代

#### 其他發佈者要求

* **[!DNL iHeartRadio]**
   * 長度：5、15、30或60秒
   * 檔案類型：MP3
   * 最大檔案大小：320 kbps
   * 卷：44.1千赫

* **[!DNL Pandora]**
   * 長度：十五、十秒
   * 檔案類型：MP4（應用內）、MP3（台式機）
   * 最大檔案大小：2.2 MB

* **[!DNL SoundCloud]**
   * 長度：6、15或30秒
   * 檔案類型：MP3
   * 最大檔案大小：5 MB

* **[!DNL Spotify]**
   * 長度：最多30秒
   * 檔案類型：OGG
   * 最大檔案大小：500MB
   * 卷：歸一化為–14;dBFS峰歸一化為–0.2 dBFS

* **[!DNL TargetSpot]**
   * 長度：15、30或60秒
   * 檔案類型：MP3

* **[!DNL TuneIn]**
   * 長度：10、15或30秒
   * 檔案類型：MP3、OGG
   * 卷：44.1千赫

### 伴隨橫幅廣告要求（可選）

**支援的大小：** 300x250、500x500、640x640、1024x1024

#### 其他發佈者要求

* **[!DNL iHeartRadio]:**
   * 檔案類型：JPEG、JPG、PNG、GIF、SWF、HTML
   * 最大檔案大小：2.2 MB
   * Dimension:300x250

* **[!DNL Pandora]:**
   * 檔案類型：JPEG,GIF
   * 最大檔案大小：大小：100 KB
   * Dimension:300x250（移動或台式機）或500x500（台式機）

* **[!DNL SoundCloud]:**
   * 檔案類型：靜態JPG,PNG
   * 最大檔案大小：400 KB以下
   * Dimension:1024x1024

* **[!DNL Spotify]:**
   * 檔案類型：靜態JPG,PNG
   * 最大檔案大小：200 KB
   * Dimension:300x250

* **[!DNL TuneIn]:**
   * 檔案類型：JPEG、JPG、PNG、GIF、HTML
   * 最大檔案大小：2 MB
   * Dimension:300x250

## 本機顯示廣告

每個廣告可以包括靜止影像或移動GIF（攝影片）。

### 支援的螢幕

預設情況下，在台式機和移動設備上提供廣告。 設備目標可用於調整遞送。

### 所有本機源格式的必需資產

#### 影像資產

**解決方案：** 最少600x600px;建議最少1200x627px

**檔案類型：** JPEG（影像廣告或視頻廣告封面影像）、GIF（電影圖）

**檔案大小：** 小於1 MB（影像應不含文本。）

#### 廣告商徽標

**解決方案：** 最少80x80px;建議最小300x300px

**檔案類型：** JPEG或PNG。

**縱橫比：**  1x1比率

>[!NOTE]
>
>根據它所覆蓋的影像，在亮或暗徽標資產之間進行選擇。

#### 文本/複製

**標題：** 最多200個字元；推薦25個字元

**標題：** 最多200個字元；推薦100個字元

**贊助者：** 最多200個字元；推薦30個字元

**行動要求（僅限MoPub）:** 最多15個字元

>[!NOTE]
>
>最終佈局由運行時的發佈者定義。 如果廣告超出了建議的字元數，則某些清單提供程式可能無法提供廣告，或者發佈者或SSP可能會截斷文本。

#### 登錄頁URL

帶有可選按一下跟蹤器的按一下直通URL。

按一下跟蹤器要求：

* 第三方印象跟蹤像素：僅1x1影像URL格式

* 可查看性JavaScript跟蹤器：僅支援IAS;1x1影像（僅限JS.append格式）

* 第三方點擊跟蹤像素：必須重定向到URL中嵌入的登錄頁（HTTP 302重定向）

* 不支援資料管理平台(DMP)按一下具有200個或更多響應的跟蹤器。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-multiple.md)
>* [編輯廣告](ad-edit.md)

