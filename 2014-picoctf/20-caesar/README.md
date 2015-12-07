# Caesar

## 題目

種類： Cryptography

分數： 20 分

敘述：
> You find an encrypted message written on the documents. Can you decrypt it?

加密訊息內容：
> ymjxjhwjyufxxumwfxjnxlqjmscymhozjnaqaadgvafrrmyfzsf

提示：
> Is there a cipher named the same as the title of this problem?

## 解題

題目名稱提示了這題使用了凱撒加密法 (Caesar Cipher)。凱撒加密法就是將每個字替換為第 n 個後的字母，如果超過 Z 就回到 A。n 超過 26 之後就會開始循環之前出現過的組合，也就是說，可能的結果只有 26 種。

網路上很容易就可以 google 到可以列出所有可能組合的凱撒解密器。

我使用[這個網站](http://planetcalc.com/1434/)列出了所有組合，看起來最合理的結果是位移 21 之後的結果：

> thesecretpassphraseisglehnxthcjueivlvvybqvammhtauna

這就是這題的 flag。
