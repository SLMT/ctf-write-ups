# Grep is Still Your Friend

## 題目

種類： Forensics

分數： 40 分

敘述：
> The police need help decrypting one of your father's files. Fortunately you know where he wrote down all his backup decryption keys as a backup (probably not the best security practice). You are looking for the key corresponding to `daedaluscorp.txt.enc`. The file is stored on the shell server at `/problems/grepfriend/keys` .

提示：
> [Grep](http://www.uccs.edu/~ahitchco/grep/) is your friend!

## 解題

一開始登入 shell 之後，先簡單用 cat 來查看一下 `/problems/grepfriend/keys` 的內容。可以發現這是一份很長的檔案，以下列出部分內容：

```
pasternak.txt.enc       0255f65b2ca047e5bbf661bb47b84ca3
inflicts.txt.enc        3332d2ec37674687bd7b6153222829d5
liner.txt.enc   08a2f0c5abb247a5aa8f7b72476038c2
felicity.txt.enc        5d2a524780af4d529e127c0206291e56
goggles.txt.enc 1f646da5dbcd4a48afd54eed02a2de82
sketchy.txt.enc fd7aaa473bda49c5bb0de95ff5213015
zero.txt.enc    b9494a12c60a4434943a8199df7f4cb3
tottering.txt.enc       f58c17a025c74fada14eb9eedbcd1f74
gloucester.txt.enc      87892ec9b5004137ae35dd6968700bd3
primate.txt.enc 97b8305c49224812b91f1d3dccf8f816
...
```

檔案內容可以看出每行分別有一個檔名與一組密文，但是檔案太長，不太可能一一檢查。

這題想到兩個解法：

1. 利用 `vim` 開啟檔案，直接搜尋 `daedaluscorp.txt.enc`。

2. 使用 `grep` 抓出含有 `daedaluscorp.txt.enc` 的那行字

第二個解法應該就是這題希望使用的方法。

`grep` 可以利用 regular expression 來從檔案中找出符合的字串，所以我們只需要下達以下指令就可以找到 flag：

```
$ grep 'daedaluscorp.txt.enc' /problems/grepfriend/keys
daedaluscorp.txt.enc    b2bee8664b754d0c85c4c0303134bca6
```
