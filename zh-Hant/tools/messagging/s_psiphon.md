---
index: 14
title: Psiphon 工具指南
---
# Psiphon 工具指南

規避網路審查

**學習內容：**[網際網路](umbrella://communications/the-internet)
**下載處：**[https://psiphon.ca/en/download.html](https://psiphon.ca/en/download.html)
**系統需求：**網路連線、運行 Windows 系統的電腦或是 Android 2.2 版本以上的手機(給 iPhones 和 Mac OS X 的 Psiphon 3 即將發佈)
**本指南所用版本：**Psiphon 3
**版權宣告：**自由開源軟體；GNU GPL Version 3
**程度：**初學者
**其它參考資料：**[https://psiphon.ca/en/user-guide.html](https://psiphon.ca/en/user-guide.html)
**所費時間：**5 分鐘

**使用Psiphon會給你：**
- 通過使用VPN（虛擬專用網絡）安全地繞過互聯網審查，以訪問被封鎖的網站和應用程序的能力。

### 1. 開始之前

- 請注意Psiphon的惡意副本，只從官方來源下載。

![圖像](tool_psiphon10.png)
![圖像](tool_psiphon11.png)
![圖像](tool_psiphon12.png)

- Psiphon主要用作審查規避工具，而不是保證匿名的工具。
- 因為Psiphon是基於VPN的，它能夠代理所有的互聯網流量，不僅僅是網站而已。
- 如果您尚未主動啟用Psiphon，則表示您未使用VPN。 （僅僅在你的計算機上安裝Psiphon是不夠的。）
- 使用VPN時，網頁加載速度可能會更慢。這種現象是正常的，因為瀏覽器並沒有直接連接到網站。
- 一些付費VPN服務的加載速度可能比像Psiphon這樣的免費服務來得更快，但在信任您的信息之前您應該小心，因為它可以與當局共享或出售給其他公司。
- 設備和VPN服務器之間的流量已加密。但是，該服務器與非HTTPS網站之間的流量將*不會*被加密。（這同樣適用於其他Internet服務，例如將Outlook或Thunderbird連接到非SSL電子郵件提供商時。）

### 2. 適用於Android的Psiphon 

從[Google Play](https://play.google.com/store/apps/details?id=com.psiphon3.subscription)商店下載Psiphon Pro。

如果您無法訪問Google Play商店，請在官方Psiphon [下載頁面](https://psiphon.ca/en/download.html?10Years)上選擇適用於Android的Psiphon Pro。 （在[此處](https://psiphon.ca/en/faq.html#authentic-android)驗證下載的文件是否可信。）您可能需要[啟用側載](https://psiphon.ca/en/faq.html#android-enable-sideloading)。）

打開應用程序並點擊 *啟動*連接到Psiphon網絡。

![圖像](tool_psiphon5.png)

選擇整個設備模式以通過Psiphon隧道傳輸所有應用程序。 （此選項可能不適用於舊版本的Android。您可以使用專用的Psiphon瀏覽器，但只有在瀏覽器中進行的在線活動才會使用Psiphon。其他應用程序將使用您的常規Internet連接進行連接。）

![圖像](tool_psiphon6.png)

設備左上角的Psiphon“P”表示Psiphon正在運行。

### 3. 適用於Windows的Psiphon

在[此處](https://psiphon.ca/en/download.html)下載適用於Windows的最新版Psiphon。在[此處](https://psiphon.ca/en/faq.html#authentic-windows)驗證下載的文件是否可信。）

當你執行 Psiphon 後它會自動連上網路，當其試著連線時會出現一個旋轉的小圖示。你可以選擇以下任一個隧道模式: **VPN、SSH 或 SSH+**

一般我們建議選擇　**VPN** 選項，它意謂此刻電腦上所有網路流量都是通過 Psiphon　隧道管理。

當您關閉程序時，Psiphon會自動斷開連接。您也可以單擊圖標切換連接。

### 4. 適用於iOS的Psiphon

從[Apple App store](https://itunes.apple.com/us/app/psiphon/id1276263909?ls=1&mt=8)下載Psiphon。

打開應用程序，然後單擊帶有灰色*已斷開連接*按鈕。

![圖像](tool_psiphon7.png)

正在連接時，按鈕將變為紅色。連接時，將變為綠色。

![圖像](tool_psiphon8.png) ![圖像](tool_psiphon9.png)

設備左上角的“VPN”圖標表示Psiphon正在運行，這意味著其他應用程序將通過Psiphon訪問互聯網。

要使用適用於iOS的專用Psiphon瀏覽器，需要單獨[下載](https://itunes.apple.com/us/app/psiphon-browser/id1193362444?mt=8)，但它適用於iOS 8或更高版本，主要的Psiphon應用程序則需要iOS 10.2或更高版本。如果您使用瀏覽器，則只有在瀏覽器中進行的在線活動才會使用Psiphon。其他應用將使用您的常規互聯網連接進行連接。