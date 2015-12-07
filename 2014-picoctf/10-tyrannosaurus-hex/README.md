# Tyrannosaurus Hex

## 題目

種類：Miscellaneous

分數：10 分

敘述：
> The contents of the flash drive appear to be password protected. On the back of the flash drive, you see the hexadecimal number 0x38a4869b scribbled in ink. The password prompt, however, only accepts decimal numbers. What number should you enter? (Press the Hint button for advice on solving the challenge)

提示：
> You could try asking [Google](http://www.google.com/) or [Wolfram Alpha](http://www.wolframalpha.com/).

## 解題

題目給了一段十六進位數字：`0x38a4869b`

很明顯地，就是要把這段數字轉成十進位。網路上隨便搜尋一下都可以找到一大堆十六進位轉換器，這邊我直接打開 python 的互動式介面：

```
Python 2.7.10 (default, Jul 14 2015, 19:46:27)
[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.39)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x38a4869b
950306459
```

即得到 flag 為 `950306459`
