# Pickle Jar

## 題目

種類： Forensics

分數： 30 分

敘述：
> The police station offers free pickles to police officers. However, someone stole the pickles from the pickle jar! You find a clue on a USB drive left at the scene of the crime.

提示：
> What exactly is a JAR file ?

## 解題

這題主要是想讓使用者練習解開一個 jar 檔。

Jar 檔是一種將 java compile 後的 class 檔包裝起來的一個執行檔。原理其實非常簡單。Jar 檔其實就一個 zip 檔，裡面放的就是一個個放在各自資料夾內的 class 檔，以及一些 Metadata 與 resource 檔而已。

因此我們這邊可以直接使用任何一個能夠解壓縮的軟體來解壓縮此提提供的 jar 檔。接著就會發現裡面有一個名為 `pickle.p` 神秘檔案。

如果快速用 `cat pickle.p` 看一下的話：

```
S'YOUSTOLETHEPICKLES'
p0
.%
```

可以發現有一個字串叫做 `YOUSTOLETHEPICKLES`。

將這個當成 flag 輸入的話就可以通過這題了！ (WTF XDDD)
