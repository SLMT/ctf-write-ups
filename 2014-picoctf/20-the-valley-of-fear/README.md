# The Valley of Fear

## 題目

種類： Cryptography

分數： 20 分

敘述：
> The hard drive may be corrupted, but you were able to recover [a small chunk of text](text.txt). Scribbled on the back of the hard drive is a set of mysterious numbers. Can you discover the meaning behind these numbers? (1, 9, 4) (4, 2, 8) (4, 8, 3) (7, 1, 5) (8, 10, 1)

提示：
> Might each set of three numbers represent a word in a message?

## 解題

這題給了一份文件和幾組數字，然後要找到 flag。

我看了看數字之後，覺得這些數字應該是代表文字的位置。稍微對照一下可以發現，每組的數字意義如下：

```
(第幾段, 第幾行, 左邊數來第幾個)
```

因此將這幾組數字對應到的單字分分找出來之後，可以拼出這句話：

```
the flag is Ceremonial plates
```

這應該就是這題的 flag。

話說我一開始以為一組數字是對應到「一個字元」，而不是「一個單字」。直到發現拼出來的東西沒有意義之後，才想到可能是單字。

其實這種題目想錯方法再重來就好，多多嘗試沒有壞處。我也鼓勵大家想到什麼就試試看。
