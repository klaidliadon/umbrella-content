---
index: 9
title: Orbot和Orfox工具
---
Orbot和Orfox工具
---

適用於Android的隱私增強型網頁瀏覽

**課程內容：[互聯網](umbrella://communications/the-internet)，[手機](umbrella://communications/mobile-phones)**
**程度**：初學者
**所需時間**：15分鐘
**發布于：** 2018年4月
**來源：**安全策劃者（公民實驗室），[Orbot和Orfox](https://securityplanner.org/#/tool/orbot-and-orfox); Security in a Box，[適用於安卓的ORBOT](https://securityinabox.org/en/guide/orbot/android/)，衛報項目，[Orbot v16：全新外觀，更易於使用！](https://guardianproject.info/2018/01/05/orbot-v16-a-whole-new-look-and-easier-to-use/)

**同時使用Orbot和Orfox會給你：**
- 在使用某些Android應用程序時隱藏網站和其他服務的在線身份的能力。
- 使用Orfox時隱藏瀏覽活動的能力。
- 使用Orfox時繞過互聯網審查和在線過濾的能力。

**下載地點：** [Orbot](https://play.google.com/store/apps/details?id=org.torproject.android)和[Orfox](https://play.google.com/store/apps/details?id=info.guardianproject.orfox) 。
**軟件要求：**因設備而異（Orbot）; Android 4.0.3及以上版本（Orfox）
**本指南中使用的版本**：版本16（Orbot）Fennec-52.7.3esr / TorBrowser-7.5.3 / Orfox-1.5.2-RC-1（Orfox）
**許可證**：FOSS（主要是GPLv2）


# 1. 簡介

Orbot允許Android設備上的其他應用程序通過Tor網絡更安全地使用Internet。 （了解有關[** Tor **](umbrella://communications/the-internet/advanced)的更多信息。）Orfox是Android版Tor瀏覽器的一個版本，它使用Orbot連接到Tor網絡。

請記住，如果您使用Orfox返回您已經創建的內容而不使用Orfox，如博客文章，託管內容的網站仍將知道您的真實位置。

如果你在使用Orfox時想要更高強度的匿名性：

*   切勿訪問以您的真實姓名製作的帳戶。
*   切勿提供您的個人資料。
*   避免在不試圖匿名時做你做的事情。


# 2. 安裝並配置Orbot


## 2.1安裝Orbot

**步驟1：**在您的Android設備上，**從[Google Play商店]下載**和按INSTALL按鈕以**安裝**應用程序(https://play.google.com/store/apps/details?id=org.torproject.android)。

![](orbot-and-002.png)

**注意：** ** Orbot **也可以從第三方[F-Droid](https://guardianproject.info/fdroid/)商店下載。


## 2.2 配置Orbot

**步驟1：**點擊**打開。**

![](orbot-and-005.png)

**步驟2：** **通過設置嚮導中的歡迎屏幕滑動**，或觸摸下一個箭頭。

![](orbot-and-006.png) ![](orbot-and-007.png)

**步驟3：**如果您對Tor網絡的訪問可能被封鎖，您可能需要使用網橋。

![](orbot-and-009.png)  

![](orbot-and-010.png)

如果您不確定是否需要橋接，請先試用。要了解有關橋接的更多信息，請閱讀*進階Orbot配置：使用以下的Tor橋接*。

**步驟4：**如果要訪問被阻止的應用程序，請單擊**選擇應用程序**，將Orbot用作VPN（虛擬專用網絡）。

![](orbot-and-008.png)

選擇要與** Orbot **一起使用的單個應用，然後單擊*確定*。

>“我們希望專注於讓特定應用程序通過Tor的方式，而不是推廣某種自動神奇的”為我的整個設備啟用Tor“，我們可以確保盡可能安全。” - 衛報項目，[2017年10月27日](https://guardianproject.info/2017/10/27/no-more-root-features-in-orbot-use-orfox-vpn-instead/)

請注意，許多應用程序（例如那些要求您登錄的應用程序）會破壞您的匿名性，即使通過Orbot通過隧道傳輸Internet流量也是如此。如果防火牆或過濾器阻止單個應用程序，但此步驟將幫助您，但不會使您匿名。


![](orbot-and-011.png)

![](orbot-and-012.png)

完成配置後，您將看到已停用的** Orbot **屏幕。

![](orbot-and-013.png)

# 3. 開始使用Orbot

**步驟1：**觸摸屏幕中央的灰色Orbot圖標，直到它變為黃色。

![](orbot-and-014.png) 

**步驟2：**連接時，Orbot變為綠色。

![](orbot-and-015.png) 

**步驟3：**觸摸綠色圖標，直到它變為灰色以斷開連接，或單擊屏幕右上角的菜單圖標，然後選擇退出以退出應用程序。

![](orbot-and-019.png)

**步驟4：**觸摸*全局（自動）*，從您的互聯網流量可能來自的位置列表中進行選擇。

![](orbot-and-022.png)

**步驟5. **切換VPN模式*開*以通過在Orbot中隧道傳輸其Internet流量來訪問列出的應用程序。通過單擊屏幕底部的* Tor-enabled Apps *，將更多應用添加到列表中。


# 4. 進階Orbot配置：使用Tor網橋

如果Tor訪問受限製或者您希望偽裝使用Tor的事實，則可以將Orbot配置為使用* bridges *。在[Tor for LINUX](umbrella://tools/tor/s_tor-for-linux.md) 工具指南中了解有關橋接的更多信息。

**步驟1：**點擊右上角的功能表圖標，然後選擇*設置*。向下滾動到* 橋接。*選中*使用橋接*旁邊的框。

![](orbot-and-025.png)

**步驟2：**如果您知道要使用的*橋接*的* IP地址*，請點擊* IP地址和橋接端口*。輸入IP地址，然後點擊*確定*。

![](/media/orbot-and-026.png)

**步驟3：**重啟** Orbot **開始使用* bridge *。

您可以在[Tor項目網站](https://bridges.torproject.org/)上閱讀有關網橋的更多信息。


# 5. 安裝Orfox

**步驟1：**在您的Android設備上，**從[Google Play商店](https://play.google.com/store/apps/details?id=info.guardianproject.orfox)下載**和**安裝**應用程序。

**注意：** ** Orfox **也可以從第三方[F-Droid](https://guardianproject.info/fdroid/)商店下載。

**步驟2：**要打開Orfox，**點擊**應用程序的圖標。

** Orfox **將為您提供連接到_https://check.torproject.org_的選項，以確保其與** Tor **網絡的連接正常。如果它可以連接，您將看到一條消息，告訴您_瀏覽器已配置為使用Tor_。如果** Orfox **無法連接到網站，您將在瀏覽器中看到錯誤消息。如果發生這種情況，請檢查Orbot是否正在運行。

**步驟3：**要瀏覽網站，**點擊屏幕頂部的區域，然後輸入您要訪問的地址。按屏幕鍵盤上的* Go *。


# 6. 清除您的Orfox瀏覽器歷史記錄

**步驟1：**要手動清除瀏覽歷史記錄和緩存，並隱藏您在Orfox中訪問過的網站，請點擊右上角有三個點的主菜單圖標，然後點擊*設置*。

**步驟2：**點擊*清除私人數據，*然後*清除數據，*以刪除列出的類別中的數據。

注意：設置此項後，您將無法按後退按鈕查看已訪問過的網頁。

**步驟3：**返回*設置*菜單並選擇*隱私。*選擇_清除exit_上的私人數據，以便在您通過主菜單退出應用程序時自動清除私人數據。

注意：從主菜單中選擇*新私人標籤*也會阻止Orfox記錄任何瀏覽歷史記錄。您下載的文件和書籤的網頁仍將保存在您的設備上。

# 7. 定制您的安全性

Orfox包含一個安全滑塊功能，允許您在標準，更安全和最安全的安全設置之間進行選擇。點擊右上角有三個點的主菜單圖標，然後點擊* Orfox設置*。更安全和最安全的設置將導致某些網站功能中斷，但您將更少暴露於黑客可以利用來攻擊您的漏洞。