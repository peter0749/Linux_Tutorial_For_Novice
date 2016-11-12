# 附錄4：grep 指令
##什麼是grep？
grep 是GNU 提供的一個系統工具(utility)，可以在文件中尋找、列出符合特定字串的行，使用正則表達式(regex)進行字串比對。
##使用方法
`grep <參數選項> <用來比對的regex> <檔案或文件>`

舉例來說：我要在下面的文件中搜尋"abc"，abc的位置在行中的哪裡不重要，文件名為"test.txt"

```abc
def
defab
abdef
def
abcdef
defabc```

輸入 `grep "abc" test.txt`，會輸出：
```
abc
abcdef
defabc
```


輸入 `grep "^abc" test.txt`，意思是只取以"abc"開頭的行，會輸出：
```
abc
abcdef
```
為什麼會有不同結果？這要講到非常常見的「正則表達式(regex)」。
##什麼是正則表達式(regex)


