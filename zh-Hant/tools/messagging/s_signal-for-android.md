---
index: 16
title: 適用於Android的Signal
---
適用於Android的Signal
==============================
安全消息

**閱讀課程：[發送信息](umbrella://communications/sending-a-message)**
**程度**：初學 - 中級
**所需時間**：15-20分鐘
**發佈時間：** 2018年4月（部分圖片可追溯至早期版本）
**資料來源：** EFF，監控自衛[如何：使用適用於Android的Signal](https://ssd.eff.org/en/module/how-use-signal-android); Security in a Box[適用於ANDROID的Signal](https://securityinabox.org/en/guide/signal/android/)。

**使用Signal會給你：**

- 允許用戶發送端到端加密的群組消息，文本消息，圖片和視頻消息，并且在Signal用戶之間加密電話對話。

**下載位置**：[Google Play商店](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)。

**系統要求**：Android 2.3及更高版本，使用Google Play服務（您需要擁有一個與該應用安裝相關聯的Google帳戶）。

**本指南中使用的版本**：Signal 3.31.3

**許可證：** GPLv3

**其他參考資料**：

*   [http://support.whispersystems.org/](http://support.whispersystems.org/)
*   [https://signal.org/blog/standalone-signal-desktop/](https://signal.org/blog/standalone-signal-desktop/)
*   [https://whispersystems.org/blog/signal-video-calls/](https://whispersystems.org/blog/signal-video-calls/)


簡介
-----------------
Signal是一款面向Android，iOS和桌面的免費開源軟件應用程序，採用端到端加密技術，允許用戶發送端到端加密的群組，文本，圖片和視頻消息，並具有加密的電話對話信號用戶之間。

雖然Signal使用電話號碼作為聯繫人，但加密的呼叫和消息實際上使用您的數據連接;因此，對話的雙方必須在其移動設備上訪問Internet。因此，Signal用戶不會因此類會話而產生短信和彩信費用。

在安卓上，Signal可以替換您的默認短信應用程序，因此在Signal內仍然可以發送未加密的SMS消息。

注意：
* Signal可以防止他人訪問您的消息和語音呼叫的內容，但它不會隱藏您發送加密消息或進行加密語音呼叫的事實。在某些國家/地區，像Signal這樣的加密工具可能會引起注意或違反法律約束。
* Signal的製造商Open Whisper Systems使用其他公司的基礎設施（Google on Android）在收到新消息時向用戶發送警報。這意味著某些元數據或有關誰在接收消息以及何時收到消息的信息可能會洩露給這些公司。

在安卓手機上安裝Signal
----------------------------------------
### 步驟1：下載並安裝Signal

在Android設備上，進入Google Play商店並搜索“Signal”。選擇[Signal by Open Whisper Systems](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms) 。

點擊“安裝”後，您將看到Signal需要能夠訪問才能運行的Android功能列表。點擊“接受”。

Signal完成下載後，點擊“打開”以啟動應用程序。

### 步驟2：註冊並驗證您的電話號碼

您現在將看到以下屏幕。輸入您的手機號碼，然後點按“註冊”。

![](tool_signalandroid_resized000_0.png)

然後，系統會要求您驗證電話號碼。點擊“繼續”。

![](tool_signalandroid_resized001_0.png)

為了驗證您的電話號碼，您將收到一封帶有六位數代碼的短信。由於Signal可以訪問您的短信，它會在您收到代碼並完成註冊後自動識別。

![](tool_signalandroid_resized002_0.png)

完成此過程後，系統會詢問您是否希望Signal成為您的默認短信應用。這可以將您的所有郵件保存在一個位置。請注意，如果您接受此消息，則發送給未安裝Signal的聯繫人的消息（即使您是從Signal應用程序中發送的消息）也不會被加密。



使用Signal
------------------------------

為了使用Signal，您呼叫的人必須安裝Signal。如果您嘗試使用Signal應用程序向某人發送消息並且未安裝Signal，則會發送標準的非加密文本消息。如果您嘗試呼叫此人，則會撥打標準電話。

Signal為您提供聯繫人中其他Signal用戶的列表。為此，表示聯繫人列表中電話號碼的數據將上傳到信號服務器，儘管此數據幾乎立即被刪除。

### 如何發送加密消息

點按屏幕右下角的鉛筆圖標。

![](tool_signalandroid_resized003_0.png)

您將看到聯繫人中所有已註冊信號用戶的列表。您還可以輸入不在聯繫人中的信號用戶的電話號碼。當您選擇聯繫人時，您將被帶到聯繫人的短信屏幕。請注意，對於Signal用戶，您將看到文本“發送信號消息” - 這意味著該消息將被加密。在此屏幕上，屏幕右上角的“電話”圖標將指示您也可以使用信號進行加密語音呼叫。在此屏幕中，您可以發送端到端加密的文本，圖片或視頻消息。

![](tool_signalandroid_resized006.png)

對於未安裝Signal的用戶，您將看到“發送不安全SMS”的文本，該文本不會發送帶加密的郵件。在此屏幕上，屏幕右上角的“電話”圖標將進行常規，未加密的電話呼叫。

![](tool_signalandroid_resized004_0.png)

### 如何啟動加密呼叫

要啟動對聯繫人的加密呼叫，請選擇該聯繫人，然後點擊電話圖標。如果您在電話圖標旁邊看到一個小掛鎖圖標，您就會知道該聯繫人可以接受信號呼叫。

![](tool_signalandroid_resized006-1.png)

建立呼叫後，您的呼叫將被加密。

### 如何啟動加密視頻通話

要進行加密視頻通話，只需按上述方式向某人撥打電話：

![](tool_signalandroid_initial_video_screen.png)

然後點按攝像機圖標。您可能必須允許Signal從您的相機訪問視頻。這與您的朋友分享您的視頻（您的朋友可能必須這樣做）。

### 如何啟動加密的群聊

您可以通過點擊溢出圖標（屏幕右上角的三個點）並選擇“新組”來發送加密的組消息。

![](tool_signalandroid_resized020_0.png)

在以下屏幕上，您將能夠為該組命名並向其添加參與者。

![](tool_signalandroid_resized021_0.png)

![](tool_signalandroid_resized016_0.png)

添加參與者後，您可以點擊屏幕右上角的複選標記。這將啟動群聊。

![](tool_signalandroid_resized019_0.png)

如果您想更改組圖標，添加或刪除參與者，可以通過點擊溢出圖標（屏幕右上角的三個點）並選擇“更新組”，從群聊屏幕完成此操作。

### 靜音對話

有時談話可能會分散注意力。對群組聊天特別有用的一個功能是靜音通知，因此每次發送新消息時都不會看到新通知。這可以通過點擊溢出圖標（屏幕右上角的三個點）並選擇“靜音通知”從群聊屏幕完成。然後您可以選擇您希望靜音多長時間處於活動狀態對於。如果需要，這也可以應用於個人對話。

### 如何驗證您的聯繫人

此時，您可以驗證與您通話的人的真實性，確保他們的加密密鑰在您的應用程序下載時未被篡改或替換為其他人的密鑰（稱為密鑰驗證的過程）。驗證是指您在與您交談的人在場時發生的過程。

首先，打開您可以向聯繫人發送消息的屏幕，如上所述。在此屏幕中，點擊溢出圖標（屏幕右上角的三個點），然後選擇“對話設置”。

![](tool_signalandroid_resized010_0.png)

在以下屏幕中，點擊“驗證安全號碼”。

![](tool_signalandroid_resized011_0.png)

現在，您將進入一個顯示QR碼和“安全號碼”列表的屏幕。此代碼對於您正在與之交談的每個不同聯繫人都是獨一無二的。讓您的聯繫人導航到相應的屏幕以與他們進行對話，以便他們的屏幕上也顯示QR碼。

![](tool_signalandroid_resized012_0.png)

返回您的設備，您可以點擊您的QR碼，將使用相機掃描您的聯繫人屏幕上顯示的QR碼。將相機對準QR碼：

![](tool_signalandroid_resized014.png)

希望您的相機將掃描條形碼並顯示一個複選標記，如下所示：

![](tool_signalandroid_resized015.png)

這表示您已成功驗證聯繫人。如果您的屏幕看起來像這樣，即表示出現了某些問題：

![](tool_signalandroid_resized013.png)

在您與該人驗證密鑰之前，您可能希望避免討論敏感主題。

_高級用戶注意：顯示QR碼的屏幕上還有一個圖標，用於在右上角分享您的安全號碼。面對面驗證是首選方法，但您可能已使用其他安全應用程序（例如PGP）對您的聯繫人進行了身份驗證。由於您已經驗證了聯繫人，因此您可以安全地使用該應用程序中建立的信任來驗證Signal中的安全號碼，而無需親自與您聯繫。在這種情況下，您可以通過點擊“共享”圖標與該應用程序共享您的安全號碼，並將您的聯繫人發送給您的安全號碼._

### 消失的消息

Signal有一項稱為“使消息消失”的功能，可確保在看到消息後，您的設備以及聯繫人的設備會在一定時間內刪除消息。要為對話啟用消失的消息，請打開您可以向聯繫人發送消息的屏幕。在此屏幕中，點擊溢出圖標（屏幕右上角的三個點），然後選擇“消失消息”。

![](tool_signalandroid_resized022_0.png)

將出現一個新屏幕，它允許您選擇消息消失的速度：

![](tool_signalandroid_resized009.png)

選擇一個選項後，您應該會在對話中看到信息，表明已啟用“消失的消息”。

![](tool_signalandroid_resized008_0.png)

您現在可以發送消息，並確保在選定的時間後它們將被刪除。