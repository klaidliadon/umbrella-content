---
index: 6
title: Efail
---
**Efail**
=====================================

**日期：** 2018年5月15日

本週，安全研究人員發布了有關PGP電子郵件客戶端漏洞的信息，這些漏洞可能會暴露過去或未來的內容，即使它是加密的。 EFF [警告](https://www.eff.org/deeplinks/2018/05/not-so-pretty-what-you-need-know-about-e-fail-and-pgp-flaw-0)這些電子郵件客戶端的用戶禁用或卸載PGP插件並切換到另一種安全通信方法。電子郵件客戶端目錄包括Thunderbird和Enigmail，在[Linux] (umbrella://tools/pgp/s_pgp-for-linux.md), [Mac OS] (umbrella://tools/pgp/s_pgp-for-mac-os-x.md), 和 [Windows](umbrella://tools/pgp/s_pgp-for-windows.md)的Umbrella工具指南PGP中推薦使用)
。

這是你需要知道的：

* 像Signal這樣的安全消息傳遞服務比加密電子郵件來得更容易，更常見，因此更可靠。所以，這是個好建議。如果您要發送敏感信息，請使用安全郵件而非電子郵件。 （了解有關[發送消息] (umbrella://communications/sending-a-message)的更多信息。）
* EFF建議禁用PGP電子郵件客戶端以防止它們自動解密信息，這*可能*會使內容容易受到攻擊。這也是一個很好的建議，但正如EFF所說，這是“暫時的，保守的”權宜之計。它*不*意味著PGP加密不安全，或者您應該發送未加密的電子郵件。
* 與所有安全方案一樣，請考慮您的個人威脅模型。 （了解有關[管理信息]的更多信息(umbrella://information/managing-information)。）如果您面臨關於加密電子郵件內容的複雜針對性攻擊的高風險，那麼保守的權宜之計將是合適的。如果您的風險很低，可能不需要考慮上述的措施。

如果您選擇繼續使用電子郵件，使用PGP加密郵件仍然比根本不加密的郵件來得更安全。但請執行以下操作：

1. 確保您運行的所有軟件都是最新的。*立即*安裝新的更新。 （如果你已讀過Umbrella的[惡意軟件](umbrella://information/malware) 課程，你無論如何都會這樣做。）
2. 檢查電子郵件客戶端中的[設置](https://twitter.com/GPGTools/status/995986721891405825?s=19)，以獲取“在郵件中加載遠程內容”選項。應禁用此選項或*取消選中*。這是因為攻擊假定黑客已經可以訪問您的加密電子郵件，並更改從遠程服務器獲取某些內容 （如圖像）的HTML代碼。如果電子郵件客戶端尚未實施正確的更新，那麼該更改可以讓他們在沒有加密的情況下查看整個電子郵件
3.  仔細關注Efail的發展。我們將在Twitter上發布更新[@_SecurityFirst] (https://twitter.com/_SecurityFirst)。