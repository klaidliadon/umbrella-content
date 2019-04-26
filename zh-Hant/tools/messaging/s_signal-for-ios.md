---
index: 17
title: 適用於iOS的Signal
---
適用於iOS的Signal
=========================

安全消息

**閱讀課程：[發送信息] (umbrella://communications/sending-a-message)**
**級別**：初級 - 中級
**所需時間**：15-20分鐘
**發佈時間：** 2018年4月（部分圖片可追溯至早期版本）
**資料來源：** EFF，監控自衛[如何：在iOS上使用信號](https://ssd.eff.org/en/module/how-use-signal-ios); Security in a Box [適用於安卓的Signal](https://securityinabox.org/en/guide/signal/android/)。

**使用Signal會給你：**

- 能夠發送端到端加密的群組，文本，圖片和視頻消息，並與其他Signal用戶進行加密的電話交談。

**下載地點**：[Apple App Store](https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8)

**系統要求**：iOS 8.0或更高版本。與iPhone，iPad和iPod touch兼容。
（您需要有一個Apple帳戶，該帳戶將連接到應用程序的安裝中）。

**本指南中使用的版本**：Signal iOS 2.8.1

**許可證：** GPLv3

**其他參考資料**：

*   [http://support.whispersystems.org/](http://support.whispersystems.org/)
*   [https://signal.org/blog/standalone-signal-desktop/](https://signal.org/blog/standalone-signal-desktop/)
*   [https://whispersystems.org/blog/signal-video-calls/](https://whispersystems.org/blog/signal-video-calls/)


簡介
-----------------
Signal是一款適用於Android，iOS和桌面的免費開源軟件應用程序，採用端到端加密技術，允許用戶發送端到端加密的群組消息，文本消息，圖片和視頻消息，并且在Signal用戶之間加密電話對話。

雖然Signal使用電話號碼作為聯繫人，但加密的呼叫和消息實際上使用您的數據連接;因此，對話的雙方必須在其移動設備上訪問Internet。因此，Signal用戶不會因此類會話而產生短信和彩信費用。

在安卓上，Signal可以替換您的默認短信應用程序，因此在Signal內仍然可以發送未加密的SMS消息。

注意：
* 信號可以防止他人訪問您的消息和語音呼叫的內容，但它不會隱藏您發送加密消息或進行加密語音呼叫的事實。在某些國家/地區，像Signal這樣的加密工具可能會引起注意或違反法律約束。
* Signal的製造商Open Whisper Systems使用其他公司的基礎設施（iOS上的Apple）在收到新消息時向用戶發送警報。這意味著某些元數據或有關誰在接收消息以及何時收到消息的信息可能會洩露給這些公司。




在iPhone上安裝Signal – 私人信使
--------------------------------------------------------------------

### 步驟1：下載並安裝Signal – 私人信使

在iOS設備上，進入App Store並搜索“Signal”。通過Open Whisper Systems選擇[Signal–私人信使](https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8)。

點擊“獲取”下載應用程序，然後“安裝”。系統可能會提示您輸入Apple ID驗證。下載完成後，單擊“打開”以啟動應用程序。

### 步驟2：註冊並驗證您的電話號碼

您現在將看到以下屏幕。輸入您的手機號碼，然後點按“驗證此設備”。

![](tool_signalios_resized000.png)

![](tool_signalios_resized001.png)

為了驗證您的電話號碼，您將收到一封帶有六位數代碼的短信。現在它將提示您輸入該代碼，然後點擊“提交驗證碼”。

![](tool_signalios_resized002.png)

此程序完成後，Signal將請求訪問您的聯繫人。點按“繼續”。

![](tool_signalios_resized003.png)

然後，Signal將請求允許向您發送通知。點按“確定”。

![](/tool_signalios_resized004.png)



使用Signal
------------------------------

為了使用Signal，您呼叫的人必須安裝Signal。如果您嘗試使用Signal應用程序呼叫或向某人發送消息並且他們沒有安裝任何上述應用程序，該應用程序將詢問您是否要通過短信邀請他們，但它不允許您從應用程序完成呼叫或向他們發送消息。

Signal為您在聯繫人中提供其他Signal用戶的列表。為此，表示聯繫人列表中電話號碼的數據將上傳到Signal服務器，儘管此數據即將被刪除。



如何發送加密消息
--------------------------------------------------

請注意，Signal的製造商Open Whisper Systems使用其他公司的基礎架構在收到新消息時向其發送警報。它在Android上使用Google，在iPhone上使用Apple。這意味著有關誰在接收消息以及何時收到消息的信息可能會洩露給這些公司。

要開始使用，請點按屏幕右上角的撰寫圖標。

![](tool_signalios_resized005-compose.png)

您將看到聯繫人中所有已註冊Signal用戶的列表。

![](tool_signalios_resized008.png)

點擊聯繫人後，您將進入聯繫人的短信屏幕。在此屏幕中，您可以發送端到端加密的文本，圖片或視頻消息。

![](tool_signalios_resized010.png)

### 如何啟動加密呼叫

要啟動對聯繫人的加密呼叫，請選擇該聯繫人，然後點擊電話圖標。

![](tool_signalios_resized010-phone.png)

此時，Signal可能會要求獲得訪問麥克風的權限。點按“確定”。

![](tool_signalios_resized011.png)

建立呼叫後，您的呼叫將被加密。

### 如何啟動加密視頻通話

要進行加密視頻通話，只需按上述方式呼叫某人：

![](tool_signalandroid_initial_video_screen.png)

然後點按攝像機圖標。您可能必須允許Signal從您的相機訪問視頻。此舉會使您與您的朋友分享您的視頻（您的朋友可能必須這樣做）。


### 如何啟動加密的群聊

您可以通過點擊屏幕右上角的撰寫圖標（帶有指向中心的鉛筆的方塊）發送加密的群組消息，然後點擊同一位置的圖標並顯示三個數字。

![](tool_signalios_resized005-compose.png)

![](tool_signalios_resized008-group.png)

在以下屏幕上，您將能夠為該組命名並向其添加參與者。添加參與者後，您可以點擊屏幕右上角的“+”圖標。

![](tool_signalios_resized023-plus.png)

這將啟動群聊。

![](tool_signalios_resized024.png)

如果您想更改組名，或添加或刪除參與者，可以通過點擊溢出圖標（屏幕右上角的三個點）並選擇“編輯組”，從群聊屏幕完成此操作。

### 如何驗證您的聯繫人

此時，您可以驗證與您通話的人的真實性，確保他們的加密密鑰在您的應用程序下載時未被篡改或替換為其他人的密鑰（稱為密鑰驗證的過程）。驗證是指您在與您交談的人在場時發生的過程。

首先，打開您可以向聯繫人發送消息的屏幕，如上所述。在此屏幕中，點按屏幕頂部的聯繫人姓名。

![](tool_signalios_resized010-name.png)

在以下屏幕中，點擊“驗證安全號碼”。

![](tool_signalios_resized015-verify.png)

現在，您將進入一個顯示QR碼和“安全號碼”列表的屏幕。此代碼對於您正在與之交談的每個不同聯繫人都是唯一的。讓您的聯繫人導航到相應的屏幕以與他們進行對話，以便他們的屏幕上也顯示QR碼。

![](tool_signalios_resized016.png)

返回設備，點按“掃描代碼”。此時，Signal可能會要求獲得訪問攝像頭的權限。點按“確定”。

![](tool_signalios_resized017.png)

現在，您將能夠使用相機掃描聯繫人屏幕上顯示的QR碼。將相機對準QR碼：

![](tool_signalios_resized018.png)

希望您的相機將掃描條形碼並顯示“安全號碼已驗證！”的對白，像這樣：

![](tool_signalios_resized019.png)

這表示您已成功驗證聯繫人。如果您的屏幕看起來像這樣，即表示出現了某些問題：

![](tool_signalios_resized020.png)

在您與該人驗證密鑰之前，您可能想要避免討論敏感話題。

_高級用戶注意：顯示QR碼的屏幕上還有一個圖標，用於在右上角分享您的安全號碼_。面對面驗證是首選方法，但您可能已使用其他安全應用程序（例如PGP）對您的聯繫人進行了身份驗證。由於您已經驗證了聯繫人，因此您可以安全地使用該應用程序中建立的信任來驗證Signal中的__號碼，而無需親自與您聯繫。在這種情況下，您可以通過點擊“共享”圖標與該應用程序共享您的安全號碼，並將您的聯繫人發送給您的安全號碼._

### 消失的消息

Signal有一項稱為消失消息的功能，可確保在看到消息後，您的設備以及聯繫人的設備會在一定時間內刪除消息。要為對話啟用消失的消息，請打開您可以向聯繫人發送消息的屏幕。在此屏幕中，點擊屏幕頂部的聯繫人姓名，然後點擊“消失消息”旁邊的滑塊。

![](tool_signalios_resized015-slider.png)

將出現一個滑標，允許您選擇消息消失的速度：

![](tool_signalios_resized021.png)

選擇一個選項後，您可以點擊屏幕左上角的“<”圖標，您應看到對話中的信息，表明已啟用“消失的消息”。

![](tool_signalios_resized022.png)

您現在可以發送消息，並確保在選定的時間後它們將被刪除。