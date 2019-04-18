---
index: 5
title: K9和Open Keychain
---
# K-9和OPEN KEYCHAIN工具指南


**課程內容：[電子郵件-進階課程](umbrella://communications/email/advanced)。**
**程度**：進階課程
**發佈時間：** 2018年5月
**來源：**Security in a Box，[適用於K9和APG的ANDROID](https://securityinabox.org/en/guide/k9/android/)，Open Keychain [常問問題] (https://www.openkeychain.org/faq/).

[APG 官網](http://www.thialfihar.org/projects/apg/)  

** Open Keychain **是一個免費的開源應用程序，允許您使用OpenPGP等公鑰加密對文件，消息或電子郵件進行加密，解密和簽名。它基於一個名為APG的類似工具的代碼，現在還沒有維護。

**手機系統要求：**
- 在Android設備上使用加密電子郵件的能力。

**下載位置：** [K-9郵件]
**下載位置:** [K-9 Mail](https://play.google.com/store/apps/details?id=com.fsck.k9)和[打開鑰匙串](https://play.google.com/store/apps/details?) 在Google Play商店中。
**軟件要求：** Android 4.0.3及以上。
**本指南中使用的版本**：5.403（K-9 Mail）; 5.0.2（打開鑰匙串）
**許可證**：FOSS。

# 1. 簡介

** K-9 Mail **是一個全面的電子郵件客戶端，允許您通過Android設備上的一個或多個電子郵件帳戶發送和接收電子郵件，並使用[Open Keychain](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain&hl=en_GB)更安全地執行此操作。

**注意：**
- 像Signal這樣的安全消息服務是敏感通信的最佳選擇，而不是電子郵件。
- 將私人加密密鑰傳輸到手機上可能會使設備上的電子郵件更安全，但也會使密鑰更容易丟失或攔截。 （在Open Keychain[網站](https://www.openkeychain.org/faq/#are-my-secret-keys-safe-on-my-mobile-device)上描述相關風險。）
- 即使電子郵件已加密，也無法向監控電子郵件的任何人隱藏*收件人*和*主題*。

在開始使用** K-9 Mail **之前，您需要：
- 手機上的互聯網連接。
- 支持安全POP3或IMAP連接的電子郵件帳戶。 （[此處](https://k9mail.github.io/documentation/accounts/providerSettings.html)查看您將與最常見的電子郵件提供商一起使用的設置。
- **程度：**進階

（在[電子郵件](umbrella://communications/email)課程中了解有關公鑰/私鑰加密的更多信息。了解如何在[Mailvelope](umbrella://tools/messaging/s_mailvelope.md)工具指南，或者適用於[LINUX](umbrella://tools/pgp/s_pgp-for-linux.md)，[Mac OSX](umbrella://tools/pgp/s_pgp-for-mac-os-x.md)或[Windows](umbrella://tools/pgp/s_pgp-for-windows.md)的PGP中生成自己的密鑰。）

# 2. 安裝並配置K9 Mail

## 2.1 安裝

**步驟1. **從[Google Play]（https://play.google.com/store/apps/details?id=com.fsck.k9）商店下載並安裝K-9 Mail。查看您仔細授予應用程序的權限，以確保您同意。

![](tool_k9_1.png)

**步驟2. ** **點擊** *打開*以首次運行該應用程序。

## 2.2 配置

單擊*下一步*開始帳戶設置。

在可能的情況下，** K-9 Mail **將嘗試自動配置您的帳戶。如果無法做到這一點，或者您希望更好地控制帳戶設置過程，也可以手動配置它。

**步驟1：**在提供的字段中輸入您的電子郵件地址和密碼，然後點擊*下一步。*

![](tool_k9_2.png)

K-9 Mail將連接到互聯網並嘗試獲取您的帳戶設置。

如果你未曾有過GPG 密鑰或是想在不同的設備上分開使用不同的 GPG 密鑰，可以利用 APG 來創建新鑰。

例如：
* Gmail用戶必須允許安全性較低的應用在設置下訪問其帳戶，並生成一次性密碼。了解更多[此處](https://support.google.com/accounts/answer/6010255?hl=en)。
* 雅虎用戶可以允許在帳戶設置下使用安全性較低的應用程序。在[這裡](https://help.yahoo.com/kb/SLN27791.html?guccounter=1)閱讀更多相關信息。

（提供商將K-9 Mail歸類為“安全性較低”，因為它不使用相同的身份驗證協議。但是，對於加密電子郵件，可信賴的開源工具（如K-9 Mail）仍然被認為是安全的。）


**步驟2 **：輸入您希望在所有外發電子郵件中顯示的名稱，為該帳戶指定一個名稱以區分多個帳戶。點擊*完成*。

**步驟3：**從您的計算機發送一封電子郵件，以確保您可以在K-9郵件中閱讀。

**注意：**如果選擇*手動設置，*將要求您選擇電子郵件類型（IMAP / POP / Exchange）的設置以及傳入和傳出服務器設置。有關此信息，請參閱計算機上的電子郵件客戶端設置。

- 對於服務器設置，請始終確保*安全類型*設置為* STARTTLS *或* SSL / TLS *。 **永遠不要**使用* none *選項。

- 如果K-9 Mail顯示有關安全連接證書的警告，*不要忽略它，*但驗證證書確實屬於您的郵件服務器。如果沒有，您的通信可能會被截獲。您應該在警告的最後看到SHA-1指紋。檢查計算機上的郵件服務器中安裝的證書是否具有相同的指紋，或者找到直接從提供商檢查郵件服務器證書的方法。


除計算機的電子郵件客戶端外，我們建議您使用** K-9 Mail **。當您下載電子郵件時，默認情況下它不會從服務器中刪除該電子郵件，因為您也希望在計算機上接收電子郵件。但是這個和其他設置可以改變。長按您剛剛設置的帳戶並從菜單中選擇*帳戶設置*，或點按應用右下角的三個點，然後選擇設置以查看您的選項。


# 3. 發送和接收加密電子郵件

**步驟1：**在設置下，點擊*加密*。如果您還沒有，K-9 Mail將提示您下載Open Keychain。下載Open Keychain後，在K-9 Mail中選擇它。

![](tool_k9_5.png)

**第5步：**檢視將要滙入的密鑰然後輕擊「導入選擇的密鑰檔案」到 APG，你也可以利用反選功能來決定哪些密鑰不被滙入
![image](tool_k96.png)

# 4. 設置Open Keychain

點擊Open keychain以打開該應用程序。在“設置”下，點按*管理我的密鑰*。

![](tool_k9_6.png)  

**第1步：**由電子郵件內文複制 GPG 密鑰到剪貼簿，下圖即為一封電子郵件內文為 GPG 密鑰
![image](tool_k98.png)

**選項2：**如果您已經擁有PGP密鑰並希望在Android設備上使用它，請打開用於管理計算機密鑰的程序（例如GPG Keychain或Mailvelope）並導出您自己的密鑰，包括您的私鑰或密鑰。將文件保存在安全的位置。

**注意：**您的私鑰可用於冒充您並解密您的加密通信。將其轉移到移動設備是有風險的，因為文件可能丟失或被截獲。

如果您選擇傳輸私鑰文件，請採取預防措施：

- 使用USB線將您信賴的Android設備連接到您信任的計算機，直接傳輸，或在您信任的計算機和您信任的Android設備上啟用藍牙（檢查配對碼匹配）並使用“發送文件到設備”功能;要么，
- 請參閱[打開鑰匙串](https://www.openkeychain.org/faq/#what-is-the-best-way-to-transfer-my-own-key-to-openkeychain)關於密碼保護密鑰的建議在通過互聯網傳輸之前使用命令行。

在Open Keychain的* Manage my keys *窗口中，點擊*從文件*導入密鑰，然後點擊文件圖標。導航到移動文件的文件夾，選擇它，然後點擊* OPEN *。您還可以使用文件*中的*導入鍵來傳輸其他人與您共享的公鑰。成功導入的密鑰現在將顯示在密鑰列表中。在Open Keychain中看到它們後，從設備中刪除文件。不要讓他們坐在文件夾中。

（要了解有關管理密鑰的更多信息，請閱讀Umbrella詞彙表中的密鑰環和密鑰簽名方條目。）


# 5. 使用K9交換加密電子郵件

**步驟1：**由** APG **主畫面視窗下輕觸你的密鑰條目，以進入 GPG 密鑰的 _資訊_畫面(如上圖)。

**步驟2：**在* 至 *字段中添加收件人的電子郵件地址。

**步驟3：**

![](tool_k9_7.png)

點按灰色鎖定圖標; 加密激活時，它將變為綠色。

![](tool_k9_8.png) 

**步驟4：**發送信息。

**步驟5：**當您收到加密回复時，K-9 Mail會自動提示您輸入GPG密碼短語並解密郵件。