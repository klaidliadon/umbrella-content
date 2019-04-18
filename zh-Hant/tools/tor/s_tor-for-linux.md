---
index: 19
title: 適用於LINUX的Tor
---
適用於Linux的Tor
=========================

線上匿名

**課程內容：[互聯網](umbrella://communications/the-internet)**
**程度**：初學 - 進階課程
**所需時間**：15分鐘—1小時
**發布于：** 2018年4月
**來源：**監視自衛（EFF），[如何：使用適用於Linux的Tor](https://ssd.eff.org/en/module/how-use-tor-linux); Security in aBox [適用於Linux的瀏覽器 - 在線匿名和規避](https://securityinabox.org/en/guide/torbrowser/linux/)。

**使用Tor會給你：**

* 從您訪問的網站隱藏您的數字身份的能力
* 隱藏您從Internet服務提供商和監控程序訪問的網站的能力
* 繞過互聯網審查和過濾的能力
* 通過HTTPS Everywhere和NoScript瀏覽器加載項保護不安全和可能存在惡意的網站

**下載地點：
**[https://www.torproject.org/download/download-easy.html.en](https://www.torproject.org/download/download-easy.html.en)。如果您無法訪問此網站，請閱讀*如果下載頁面被封鎖*，請參見下文。
**計算機要求：** 互聯網連接，運行您喜歡的Linux發行版的計算機。
**本指南中使用的版本**：Ubuntu 16.04.1 LTS; Tor瀏覽器：7.0.2
**許可證**：免費軟件;混合使用自由軟件許可證

簡介
-------------

本指南概述如何在Linux上使用[Tor瀏覽器](https://www.torproject.org/projects/torbrowser.html.en)。

Tor是一項志願者運營服務，通過屏蔽您的身份以及您所連接的位置，在線提供隱私和匿名性。該服務還可以保護您免受Tor網絡本身的影響 — 您可以很好地保證您將對其他Tor用戶保持匿名。

對於在訪問網站時可能需要偶爾匿名和隱私的人，Tor瀏覽器提供了一種使用Tor網絡的快捷方式。

Tor瀏覽器就像一個Web瀏覽器，用於查看網站的程序。示例包括Chrome，Firefox和Safari。但是，與其他網絡瀏覽器不同，Tor瀏覽器會通過Tor發送您的通信，這使得監控您的人更難以確切知道您在網上做什麼，並且監控您使用的網站的人更難以了解您的位置從...連接。

請記住，只有您在Tor瀏覽器內部執行的活動才會被匿名化。在您的計算機上安裝Tor瀏覽器並不會使您使用其他軟件（例如常規Web瀏覽器）匿名在同一台計算機上執行操作。

**參考資料**：

*   [https://www.torproject.org/docs/documentation.html.en](https://www.torproject.org/docs/documentation.html.en)
*   [https://tor.stackexchange.com/](https://tor.stackexchange.com/)
*   [https://www.eff.org/pages/tor-and-https](https://www.eff.org/pages/tor-and-https)


獲取Tor瀏覽器
-------------------------------------

打開Firefox或Chrome等瀏覽器，然後轉到：

[https://www.torproject.org/download/download-easy.html.en](https://www.torproject.org/download/download-easy.html.en)

如果您使用搜索引擎查找Tor瀏覽器，請確保該URL正確無誤。

請勿使用任何其他來源，並且如果系統提示您接受其他HTTPS(SSL/TLS)安全證書，請不要繼續。

![](torforlinux1.png)

該網站將檢測到您的操作系統，您將獲得適用於您的操作系統的正確文件。如果失敗，您可以單擊紫色按鈕側面的鏈接以下載正確的版本。

某些瀏覽器會要求您確認是否要下載此文件。 Firefox在瀏覽器窗口中間顯示一個彈出框。對於任何瀏覽器，最好先保存文件，然後再繼續。單擊“保存”按鈕。

此示例顯示Tor瀏覽器版本7.0.2。在您閱讀本文時，可能會有更新版本的Tor瀏覽器可供下載，因此請下載並使用Tor Project提供的當前版本。

![](torforlinux2.png)


安裝Tor瀏覽器
----------------------------------------

下載完成後，轉到“下載”文件夾。您應該始終確保您信任要安裝的軟件，並且您通過安全連接從官方網站獲得了正版副本。既然您知道自己想要什麼，並且知道從哪裡獲得該軟件，並且下載來自Tor Project的安全HTTPS站點，請雙擊文件“tor-browser-linux64-7.0.2_en-US.tar.xz “。

![](torforlinux3.png)

雙擊Tor瀏覽器存檔文件後，等待它加載，然後選擇要提取其內容的位置。

![](torforlinux4.png)

提取完成後，打開“tor-browser_en-US”文件夾，然後雙擊“Tor瀏覽器設置”文件。

![](torforlinux5.png)
 

使用Tor瀏覽器
-----------------

然後，您將獲得一個窗口，允許您在必要時修改某些設置。您可能必須返回並更改某些配置設置，但請繼續嘗試通過單擊“連接”按鈕連接到Tor網絡。

![](torforlinux6.png)

將打開一個新窗口，其中顯示一個橙色條，表示Tor瀏覽器連接到Tor網絡。

![](torforlinux7.png)

當Tor瀏覽器第一次啟動時，可能需要花上很長時間; 但請耐心等待，在一兩分鐘內，Tor瀏覽器將打開並歡迎您。

![](torforlinux8.png)

單擊Tor瀏覽器左上角的Tor Onion徽標，然後單擊隱私和安全設置。

![](torforlinux9.png)

一般互聯網瀏覽器的某些功能可能使您容易受到中間人的攻擊。其他功能之前已經出現了漏洞，揭示了用戶的身份。將安全滑塊設置為高設置會禁用這些功能。這將使資源充足的攻擊者更安全，他們可能會干擾您的Internet連接或在這些功能中使用新的未知錯誤。不幸的是，關閉這些功能可能會使某些網站無法使用。默認的低設置適用於日常隱私保護，但如果您擔心複雜的攻擊者，或者如果您不介意某些網站無法正確顯示，則可以將其設置為高。

![](torforlinux10.png)

最後，使用Tor進行瀏覽在某些方面與普通瀏覽的體驗不同。我們建議您閱讀[這些提示](https://www.torproject.org/download/download-easy.html.en#warning)，以便使用Tor正確瀏覽並保留您的匿名性。

![](torforlinux11.png)

您現在可以使用Tor匿名瀏覽互聯網。

## 檢查Tor瀏覽器是否正常工作

Tor瀏覽器會隱藏您訪問的網站的* IP地址*。如果它正常工作，您應該似乎是從Internet上的某個位置訪問網站

- 與您的普通IP地址不同
- 無法鏈接到您的實際位置

確認這一點的最簡單方法是訪問* Tor Check *網站，該網站位於[** https://check.torproject.org/**](https://check.torproject.org)

當你**不**使用Tor時，它將顯示以下內容：

 ![](not-using-tor.png)


如果您使用Tor，它將顯示以下內容：

 ![](using-tor.png) 

如果要使用與Tor項目無關的服務檢查明顯的IP地址，可以在線查看許多選項。支持* https *加密的例子（這使得某人*其他*比服務提供商更難“偽造”結果）包括：

- [https://www.iplocation.net/](https://www.iplocation.net/)
- [https://www.ip2location.com/](https://www.ip2location.com/)

如果您在沒有使用Tor瀏覽器的情況下訪問這些網站*，則應顯示您的真實IP地址，該地址與您的實際位置相關聯。如果通過Tor瀏覽器訪問它們，它們應顯示不同的IP地址。

## 如何創建新標識

您可以在Tor瀏覽器上創建“新身份”。當您這樣做時，Tor瀏覽器將隨機選擇一組新的Tor繼電器，這將使您在訪問網站時看起來來自不同的IP地址。為此，請按照以下步驟操作：

**步驟1：** **打開**Tor瀏覽器功能表

 ![](new-identity.png)

**步驟2**。 **從功能表中選擇** *新標識*。

Tor瀏覽器將清除您的瀏覽歷史記錄和Cookie，然後重新啟動。一旦重新啟動後，您可以確認您似乎來自新IP地址，如上一節所述。

無法使用Tor瀏覽器
-----------------

如果無法連接，請嘗試[故障排除](https://www.torproject.org/docs/faq.html.en#DoesntWork).。

如果您仍然無法連接並懷疑您對Tor的訪問可能受到限制，請閱讀*如果Tor網絡被封鎖*，請參閱下文。

如果您計劃前往懷疑可能限制Tor訪問的區域，請閱讀*如何重新配置對Tor網絡的訪問*，如下所示。

＃如果下載頁面被封鎖

* 在[Github](https://github.com/TheTorProject/gettorbrowser)上有一個Tor瀏覽器套件的鏡像。
* 您也可以通過電子郵件將gettor@torproject.org與您需要的版本（windows，osx或linux）聯繫在一起。
* 在Twitter上向[@get_tor](https://twitter.com/get_tor)發送“協助”的直接消息，以通過DM請求Tor獲取指令。

在下載適用於Linux的Tor Browser軟件包之前，必須確定是運行** 32位**還是** 64位**系統。在提取之前，您應該驗證它是否可信。

**步驟1**。啟動* 終端 *應用程序

**步驟2**。在* 终端机*中執行以下命令：

`uname –m`

如果您正在運行** 32位**系統，* 終端 *將顯示`i686`或`i386`。如果您正在運行** 64位**系統，它將顯示`x86_64`。

**步驟3**. **單擊**下載鏈接並將套裝保存在方便的位置（例如，在* Desktop *或* Documents *文件夾中，或在USB存儲設備上）。您將需要** .asc **文件通過驗證其簽名來*驗證*套裝的真實性。 （參見[Tor項目的驗證簽名指南](https://www.torproject.org/docs/verifying-signatures.html.en)）。

驗證Tor瀏覽器
------------------

GnuPG已預先安裝在許多Linux系統上，因此您可以在不安裝其他軟件的情況下查看Tor瀏覽器的* Open PGP簽名*。（在[電子郵件](umbrella://communications/email/expert)課程和[適用於LINUX的PGP的工具指南](umbrella://tools/pgp/s_pgp-for-linux.md)中了解有關PGP的更多信息。）

**步驟1**。通過啟動* 終端 *並執行以下命令導入* Tor項目的*簽名密鑰
（** 0x4E2C6E8793298290 **）：

`gpg --keyserver x-hkp://pool.sks-keyservers.net --recv-keys 0x4E2C6E8793298290`

作為回應，*終端*應顯示以下內容：

 ![](torforlinux12.png) 

**步驟2**。您可以通過* 終端 *執行以下命令來顯示有關此密鑰的信息：

`gpg --指紋 0x4E2C6E8793298290`

作為回應，*終端*應顯示以下內容：

 ![](torforlinux13.png)

**步驟3**。使用* 終端 *，輸入保存以下兩個Tor Browser軟件包文件之一的目錄：

- *tor-browser-linux64-5.0.4_en-US.tar.xz* 
- *tor-browser-linux32-5.0.4_en-US.tar.xz*

該目錄應包含以下兩個簽署文件之一：

- *tor-browser-linux64-5.0.4_en-US.tar.xz.asc* 
- * TOR-瀏覽器linux32-5.0.4_en-US.tar.xz.asc *

**重要説明**：在上面和下面的示例中，這些文件來自Tor瀏覽器的** 5.0.4 **版本。 **您的文件應具有更高的版本號。**

**步驟4**。在該目錄中，在* 終端 *中執行以下命令之一（取決於您是否下載了32位或64位版本的Tor瀏覽器）

- `gpg --verify ./tor-browser-linux32-5.0.4_en-US.tar.xz{.asc*,}`
- `gpg --verify ./tor-browser-linux64-5.0.4_en-US.tar.xz{.asc *，}`

作為回應，*終端*應顯示以下內容：

 ![](torforlinux14.png)

以上驗證使用*步驟1 *中導入的*公鑰*對應的*私鑰*來生成您在上一節*步驟5 *中下載的簽名文件（並且此簽名文件適用於您在上一節*步驟4 *中下載的Tor瀏覽器包）。

**重要事項**：如您所見，GPG會顯示有關此簽名所用密鑰的警告。這是因為您實際上沒有驗證過Tor Project的簽名密鑰。最好的方法是親自與Tor項目開發人員見面，並詢問他們簽名密鑰的指紋。出於本指南的目的，我們依賴於一個眾所周知的Tor Project GPG密鑰（** 0x4E2C6E8793298290 **）用於創建簽名文件，該文件確認您下載的Tor Browser軟件包的真實性。


# 如果Tor網絡被封鎖

如果要從Tor網絡被阻止的位置使用Tor瀏覽器，則必須使用**橋接繼電器**。橋接器未列在Tor繼電器的公共目錄中，因此它們更難以阻止。有些橋接器還支持**可插拔傳輸**，它試圖掩蓋與Tor網絡之間的流量。這有助於防止在線過濾器識別和阻止橋接中繼。

名為** obfs4 **的默認可插拔傳輸也使其他人更難以確定您是否正在連接到Tor網絡。但是，一般來說，Tor並不是為了隱藏你使用Tor的事實。

您可以在[Tor項目網站](https://bridges.torproject.org/)上了解有關網橋的更多信息。有兩種方法可以使用網橋。您可以啟用**提供的網橋**，或者您可以請求**自定義網橋**。

### 提供橋接/網橋

您可以通過執行以下步驟使用提供的網橋連接到Tor網絡：

**步驟1**。 **雙擊** **Tor瀏覽器設置**文件。這將顯示Tor瀏覽器配置屏幕。

 ![](tor-running-1.png)


**步驟2**. 如果您遭到訪問權限的限制，請**單擊** **[配置]**。

![](tor-bridges-config.png)

**步驟3**。 **選擇** **是**

**步驟4**。 **單擊** ** [下一步] **以顯示*橋接配置*屏幕

![](provided-bridges.png)

**步驟5**。 **選擇** **以提供的橋接進行連接**

**步驟6**。 **單擊** ** [下一步] **以顯示*本地代理配置*屏幕

Tor瀏覽器現在將詢問您是否需要使用*本地代理*來訪問Internet。以下步驟假定您沒有。如果您執行*，則可以檢查常規瀏覽器設置並複制代理配置。 （在Firefox中，您可以在*連接設置*的*選項>高級>網絡*選項卡中找到這些設置。在其他瀏覽器中，您可以在* Internet選項*下找到它們。您也可以在瀏覽器中使用*幫助*功能更多幫助。

![](no-local-proxy.png)

**步驟7**。 **選擇** **否**

**步驟8 **。 **單擊** ** [連接] **以啟動Tor瀏覽器

![](tor-running-2.png)

過了一會，Tor瀏覽器將打開。


### 自定義橋接/網橋

您還可以通過**自定義橋接器**連接到Tor網絡，這些橋樑使用的人數少於**提供的橋樑**，因此不太可能被阻止。如果您無法訪問Tor Project網站，可以使用* Riseup *，* Gmail *或* Yahoo *帳戶向**bridges@torproject.org**發送電子郵件，以請求自定義橋接地址。在郵件正文中包含短語** get bridges **

如果您*可以*訪問Tor項目網站，這意味著您也可以訪問
**https://bridges.torproject.org/options** 並按照以下步驟來獲取自定義橋址。

**步驟1**。 **點擊** *給我橋接！*

 ![](just-give-me-bridges.png)


**步驟2**。填寫驗證碼並按**輸入**。

 ![](bridge-captcha.png)


這應該顯示三個橋接地址。

 ![](bridge-lines.png)


**步驟3**. 獲得自定義橋接地址後，您可以在下面顯示的* Tor Bridge Configuration *屏幕中**輸入**。

 ![](custom-bridges.png) 


## 如何重新配置對Tor網絡的訪問

在任何階段，如果您需要以不同的方式訪問Tor網絡，例如，如果您已經前往阻止Tor的國家/地區，則可以按照以下步驟在瀏覽器中更新您的設置：

**步驟1：** **打開**Tor瀏覽器功能表

 ![](torbrowser-lin-en-v01-901.png)

**步驟2. ** **選擇** * Tor網絡設置*以更改Tor瀏覽器連接到互聯網的方式。

 ![](custom-bridges.png)

此屏幕允許您啟用或禁用橋接並添加自定義橋接以及其他更改。

**步驟3**. 完成後，**單擊** ** [確定] **並**重啟** ** Tor瀏覽器**。