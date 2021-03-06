# Bitcoin Lightning Network常見問題解答

原文：https://medium.com/@The1Brand7/lightning-faq-67bd2b957d70

[![轉到Brand7的個人資料](https://cdn-images-1.medium.com/fit/c/50/50/1*-eAaHdGYaMeKWZPqQRf6WA.jpeg)](https://medium.com/@The1Brand7?source=post_header_lockup)

[Brand7](https://medium.com/@The1Brand7)

2016年12月22日

![](https://cdn-images-1.medium.com/max/800/1*ipqdJgFUJb2Gs16XtWNvYw.jpeg)

### **問1：什麼是閃電網絡？**

**答：** 閃電網絡目前正在開發中。它將成為一個分散的網絡，可以實現比特幣所有權的即時脫鏈轉移，而無需受信任的第三方。

該系統使用由多簽名地址組成的雙向支付渠道。

打開一個頻道需要一個鏈上交易，而另一個鏈上交易可以關閉該頻道。

一旦渠道開放，價值可以立即在交換真實比特幣交易的交易對手之間轉移，但不會將它們廣播到比特幣網絡。

只要渠道保持開放，新交易將取代以前的交易，交易對手將在本地存儲所有內容。

### **問題2：Lightning Network是開源的嗎？**

**答：** 是的，Lightning是開源的。任何人都可以查看代碼（與比特幣代碼相同）

### **問題3：誰擁有並控制閃電網絡？**

**答：** 與比特幣網絡類似，沒有人會擁有或控制閃電網絡。

該代碼是開源的，任何人都可以免費下載和查看。

任何人都可以運行節點並成為網絡的一部分。

### **問題4：誰是閃電網絡的發明者？**

**答：**  Joseph Poon和Thaddeus Dryja寫了[閃電白皮書](https://lightning.network/lightning-network-paper.pdf)。

Lightning是一個開源項目，所以任何人都可以自由地貢獻代碼。

正在開發幾個獨立的實現：

[lnd - 閃電實驗室](https://medium.com/lightning-resources/lnd-lightning-labs-9d167af18d8d)

[eclair - ACINQ](https://medium.com/lightning-resources/eclair-acinq-dfff4bc1a139)

[lightning-d - Blockstream](https://medium.com/lightning-resources/lightning-d-blockstream-8d4d251295f)

### **問題5：閃電網有自己的“閃電幣”** 嗎？

**答：** 不，這不是它的工作原理。

閃電網絡將使用真實的比特幣交易與其中的實際比特幣

### **問題6：閃電網是否依賴共識來實施？**

**答：** 不，閃電網絡的實施不需要在比特幣網絡中達成共識。

閃電既不是軟叉也不是硬叉。

相反，Lightning Network在比特幣網絡之上構建了一個額外的層。

因此，實施獨立於共識。

### **問題7：閃電網絡中是否存在任何形式的保管人風險？**

**我是否需要相信任何人代表我持有我的錢？**

**答：** 不，這個系統不是基於信任; 你仍然完全控制你的錢。

如果出現任何問題，您只需將您頻道的最新狀態廣播為正常的鍊式比特幣交易。

您的所有款項將返還到您的地址，並將正常記錄在區塊鏈中。

### **問題8：我聽說Lightning交易正在“脫鏈”發生......這是否意味著我的比特幣將從區塊鏈中刪除？**

**答：** 不，你的比特幣永遠不會離開區塊鏈。

只要您的頻道保持打開狀態，您的比特幣就會被保存在多個簽名地址中。當通道關閉時; 最終交易將被添加到區塊鏈中。

“脫鏈”並不是一個完美的術語，但由於所有權的轉讓不再反映在區塊鏈上，因此使用它。

### **問題9：我聽說Lightning Network會要求我的比特幣被鎖定......這是正確的嗎？**

**答：** 在這種情況下， **“** 鎖定”是一個非常誤導性的術語。

閃電不會讓你的錢變得不那麼容易。

當您在Lightning頻道舉行時，您的錢實際上將更容易獲得。

首先，您無需等待Lightning Network中的確認。您的資金幾乎可以在此網絡中立即移動。

第二; 將您的資金“重新上鍊”就像發送正常的比特幣交易一樣簡單。你只是等待第一次確認，你的錢不再是“脫鏈”

一個例外是極少數情況下您的頻道在交易過程中發生故障（交易對手下線）

在這種特殊情況下; 在您花錢之前，您將受到短暫的延遲。這種延遲的長度會有所不同; 取決於您應用於頻道的參數（範圍估計最短幾個小時，最多幾天）

### **問題10：閃電網絡是否有自己的區塊鏈？**

**答：** 不，閃電依賴於比特幣區塊鏈。需要在鏈上交易來打開和關閉網絡中對等體之間的“信道”。

一旦渠道開放，比特幣的所有權可以在兩個方向上進行脫鏈轉移。

頻道內的交易是真實的比特幣交易，但只要頻道保持開放，它們就不會廣播到比特幣網絡。

相反，參與渠道的人將在本地存儲交易。

這使得閃電網絡中的即時交易和近乎無限的容量成為可能。

### **問題11：是否有任何形式的採礦來保護閃電網絡？**

**答：** 不，基礎比特幣網絡中的比特幣礦工提供安全保障

### **問題12：比特幣的主鏈由2 ExaHash / s的哈希率保護，但Lightning Network根本沒有任何哈希率...**

**那麼Lightning Network如何像主鏈一樣安全？**

**答：**  Lightning Network中的安全性是從底層比特幣網絡中提取的。

閃電網絡無法自行運行; 它完全依賴於底層比特幣網絡的安全性。

基本上比特幣網絡在閃電網絡下扮演安全網的角色。

如果Lightning頻道出現問題（比如您的對方離線），您將始終可以選擇進入安全網。

（您只需將您頻道的最新狀態廣播為正常的鍊式比特幣交易）

### **問題13：Lightning Network是否擁有自己的公共分類帳或某種所有交易的數據庫？**

**答：** 不，Lightning Network沒有自己的分類賬，也沒有數據庫。

在Lightning Network上持有價值意味著您擁有雙重簽名交易。交易有效，但尚未向比特幣網絡廣播。

您持有的交易是2個多簽名類型中的2個。

您和您的對方都將簽署，您將在本地存儲交易。

這些交易將使用多簽名地址作為其輸入（資金地址）

並且他們將指向兩個不同的地址輸出。

一個輸出指向只有您可以控制的地址。另一個輸出指向只有對方可以控制的地址。

### **問題14.0：你說Lightning Network正在使用真正的比特幣交易......如果它沒有記錄在區塊鏈上，它怎麼能成為真正的比特幣交易呢？**

**短A：**

要理解這一點，我們首先需要了解比特幣交易究竟是什麼......

事實上; 比特幣中沒有“硬幣”......

只有簽名的消息和區塊鏈的更新。

所以，讓我們說Alice正在向Bob發送1比特幣......

我們稱之為點對點交易，因為價值的所有權直接從Alice轉移到Bob。

但鮑勃實際上沒有收到愛麗絲的“數字硬幣”。

事實上正在發生的事情; 是網絡中的所有節點都將更新其公共分類帳的本地副本。

公共分類賬更新，以便; 之前登記在Alice控制的地址中的“硬幣”現在改為在Bob控制的地址中登記。

**長A：**

Alice發送給Bob的比特幣交易實際上只是Alice正在向所有人廣播的簽名消息。

該消息不僅被Bob接收，而且被廣播到網絡中的所有節點。

在撰寫本文時，比特幣網絡中有超過5400個所謂的“完整節點”。

以下步驟說明了Alice向比特幣發送比特幣交易時發生的過程：

1. 當Alice正在廣播她的簽名消息（=比特幣交易）時，它將被網絡中的一些完整節點接收。

2. 這些節點將根據共識規則獨立驗證消息（事務）。如果節點發現消息有效; 他們將再次廣播該消息，以便它可以被網絡上的其他節點接收。

3. 網絡上的其他一些節點將接收消息，此過程將繼續，直到所有5400個節點都已獨立驗證並重新廣播該消息（事務）

4. 在某些時候，礦工將成功構建包含Alice的消息（事務）的有效塊。為了實現這一目標，礦工必須承擔巨額電力的成本。

5. 礦工現在將播放這個新發現的街區。一些完整節點將拾取新塊。節點將獨立驗證塊及其所有內容。

通過這樣做，他們還第二次驗證來自Alice的消息（事務）。

如果節點發現該塊有效（根據一致規則），則它們將再次廣播該塊，以便其他節點也可以接收該塊。

6. 其他節點將接收塊，驗證和廣播。

該過程繼續，直到網絡中的所有節點都獨立地驗證了塊，從而也第二次驗證了來自Alice的消息（事務）。

上述步驟說明正常的比特幣交易實際上涉及網絡上的每個人。

該消息由5400個節點（= 10 800個驗證）獨立驗證兩次

儘管如此，我們仍稱其為“點對點交易”，因為價值的實際所有權直接從Alice轉移到Bob *

（*但是每個人仍然需要通過更新他們的分類帳的本地副本來提供幫助）

結論：

比特幣交易只是一條簽名消息。

所以，假設Alice想要在Lightning頻道內向Bob發送1比特幣：

愛麗絲將她的一些錢存入“2/2”多重簽名地址。

Alice和Bob都會簽署一條消息，將1比特幣的所有權從Alice轉移到Bob。

此消息 **是有效的比特幣交易** ，但 **不會廣播到比特幣網絡。**

相反，Alice和Bob都在本地存儲事務（消息）。

**從鮑勃的角度來看，這種“雙重簽名的消息”的貨幣價值為1比特幣。**

1比特幣的貨幣價值來自於鮑勃可以隨時將這筆錢花 **在鏈** 上的事實; 通過簡單地 **將消息廣播到比特幣網絡。**

比特幣交易=簽名消息=閃電交易

任何貨幣交易的目的都是改變價值的所有權。

在比特幣網絡中，我們通過使用 **簽名消息來** 改變價值的所有權 **。**

Lightning事務是 **雙重簽名的消息。**

因此，這種 **雙重簽名的消息** 是 **真正的比特幣交易。**

### **問題14.1：標準比特幣Tx取決於區塊鏈中的確認...那麼，聲稱Lightning Tx與普通比特幣Tx相同是否真的公平？**

**答：** 這是一個有效點，它們不一樣......

Lightning Tx是零確認Tx。但如果它被廣播到比特幣網絡; 它將與任何 *“在線”* 零確認Tx 一樣有效。

如果他們支付足夠的費用，這兩種類型的Tx最終將被開採到比特幣區塊鏈中。

但是，與標準零確認Tx相比，LN-Tx具有不同的安全模型，使其更加可靠。

Lightning Tx僅通過工作證明 **間接** 保護。這是因為Lightning Network將完全依賴於底層比特幣網絡（參見Q12）

在開放的Lightning頻道內; 有一套不同的 *遊戲理論* 機制可以提供不同類型的安全模型。

Lightning將擴展比特幣的功能，而無需可信賴的第三方。

但權衡的是，您必須通過全節點的操作來監控比特幣網絡。

這種監控可以外包，但在這種情況下，您必須信任外部服務器才能真正完成其工作。您的錢仍然不會通過此服務器路由。服務器的唯一作用是監控比特幣網絡，並在必要時廣播所謂的 ***罰款交易*** 。

請注意，如果您不想運行自己的全節點，則可以 **選擇** 使用此服務。

這個第三方不可能從Lightning頻道竊取資金。

另請注意，LN旨在作為低價值轉移的平台（低於100美元）

所有LN事務都是多重簽名，並且通道中的兩個參與者都必須簽署Tx才能生效。因此，傳統的雙重支出攻擊非常困難。

但是，有人可能會將過時的Lightning Tx廣播到比特幣網絡。

一個 **過時的閃電的Tx** 在TX，並不代表它的渠道的最新狀態。

上述風險是您（或您信任的服務）必須運營 **“W  *atcher Node”的原因*** *。*

此節點將監視廣播到比特幣網絡的所有事務。

如果您的 *Watcher Node* 發現過時的Tx; 它（作為對策）廣播 ***“罰款交易”***

該 *處罰的交易* 給你沒收頻道內的所有金錢的力量（包括屬於你的對手的錢）

但是，懲罰Tx只有在發現廣播的過時Tx後才能生效。

您廣播 *懲罰交易的* 能力使您的對手廣播過時的Tx風險很大。

另一個安全/隱私功能是，所有Lightning Tx都將在參與者之間進行端到端加密。

**結論：**

Lightning Tx的安全模型不同於傳統比特幣Tx的安全模型。

如果廣播到比特幣網絡，Lightning Tx仍將被視為 **有效的比特幣Tx** 。

然而;

只要頻道保持開放，Lightning Tx就不會公開播出。

它只會在頻道中的參與者之間進行交換，並且會在本地存儲Tx。

因此，我們可以將Lightning-Tx定義為：

具有一些 **額外** ***安全機制*** 的 ***非廣播零確認多簽名比特幣-Tx*** ***。***

### **問題15：我聽說Lightning Network將要求其用戶不斷監控區塊鏈......**

**這是真的？**

**答：** 是的，這是真的..

用戶需要運行主動監控區塊鏈的軟件以解決合同違規問題（廣播過時的交易）

但是，可以將此監控外包給第三方。

外包不會影響您的隱私，但您必須相信該服務才能真正完成其工作。

**好處是;**

這有望鼓勵更多人在比特幣網絡上運行 **完整節點** 。

您的完整節點甚至可以賺取一點錢：

一個 **“全節點/閃電節點”** 可以作為收費 **“鮑勃”** （請參閱下面的說明）

另一種選擇是配置全節點以 **將區塊鏈監視為服務。** 從理論上講，這也可能帶來一些“微觀收益”

### **問題16：我聽說閃電網會收取一些費用。**

**誰將收取這些費用？**

**答：** 可能正在運行Lightning節點的任何人。

例：

愛麗絲想把錢寄給卡羅爾，但愛麗絲沒有卡羅爾的開放頻道。

但愛麗絲與鮑勃有一個開放的頻道，鮑勃與卡羅爾有一個開放的頻道。

Alice可以通過Bob路由付款，而不是通過Carol打開新頻道：

愛麗絲 - 鮑勃 - 卡羅爾。

在這種情況下，Bob可能會收取少量費用。

### **問題17：在上述情況中; 什麼阻止鮑勃只是在運輸中偷錢？**

**短A：**

Bob實際上是先向Carol付款，之後Bob會從Alice那裡拿回他的錢。

**長A：**

1.卡羅爾通過產生一個隨機數字（R）開始這個過程，她將作為臨時秘密保留。

2.卡羅爾然後生成R的散列（H）

卡羅爾給了愛麗絲

愛麗絲構建了一個特殊的交易，可以將錢從愛麗絲轉移到鮑勃。但此交易僅在包含R時有效。此時，由於缺少R，事務無效.Alice還將H給予Bob，Bob知道H是缺失組件R的哈希值。

鮑勃現在將構建另一項特殊交易，可以將資金從鮑勃轉移到卡羅爾。但是，如果包含R，則此事務也僅有效。此時交易無效，因為Bob沒有訪問權限R.

卡羅爾想要她的錢，所以她向鮑勃透露了R; 從而使交易有效。

7.由於Bob已經擁有Alice所做的交易，他可以只包含R並且該交易也有效。Bob知道他已被給予正確的R，因為他可以檢查H是R的散列。

8.同時; 鮑勃還向愛麗絲透露了R.

愛麗絲現在可以 **使用R作為** 她支付Carol（R成為收據）的 **證明**

### **問題18：閃電是否需要隔離證人？**

**答：** 可以在這裡找到一個可靠的答案：

https://medium.com/@rusty_lightning/bitcoin-lightning-things-to-know-e5ea8d84369f#.oujgao7s2