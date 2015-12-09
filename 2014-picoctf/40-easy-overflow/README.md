# Easy Overflow

## 題目

種類： Binary Exploitation

分數： 40 分

敘述：
> Is the sum of two positive integers always positive? `nc vuln2014.picoctf.com 50000`
'nc' is the Linux netcat command. Try running it in the [shell](https://picoctf.com/shell).

提示：
> Java's integer is defined as being 4 bytes long.

## 解題

這題找一台有 `nc` (netcat) 的系統就可以開始進行。

首先使用題目提供的 `nc vuln2014.picoctf.com 50000` 指令連上目標服務。

一開始會收到以下歡迎訊息：

```
Your number is 5832829. Can you make it negative by adding a positive integer?
```

數字部分會隨著每次連線不同。依照上面的歡迎訊息來看，我們可以輸入一個數字加上訊息中的數字，並嘗試使他 overflow 變成負數。

我第一次先隨意輸入一個數字：

```
Your number is 5832829. Can you make it negative by adding a positive integer?
4324234324
I'm unable to parse your number. It might be too large (the largest java int is 2147483647), or just not a number.
```

看來我輸入的數字太大以致於無法解析。

其中可以注意到它提示最大的數字是 2147483647，也就是 32-bit int 的最大值。那我們將這個數字加上去的話，無論是甚麼數字都一定會 overflow 囉！(雖然不一定會是負數)

因此我們直接加上 2147483647 試試看：

```
Your number is 3536274. Can you make it negative by adding a positive integer?
2147483647
Congratulations! The sum is -2143947375. Here is the flag: That_was_easssy!

Thanks for playing.
```

成功！可以看到 flag 為 `That_was_easssy!`。
