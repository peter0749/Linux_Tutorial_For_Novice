# 第四章：基本開發環境建置

## 1. 安裝 build-essential 套件
```sudo apt-get install build-essential```<br/>
build-essential 題供了基本的make 與 gcc、g++ 等工具，對於C/C++ 有需求的人，或是有手動編譯Tarball 的人，這個套件必裝。
## 2. (Optional) 安裝Cmake、Automake、Autoconf 等套件
```sudo apt-get install cmake automake autoconf ```
## 3. (Optional，對安裝Ubuuntu 在電腦上的) 安裝驅動程式
從 **"系統設定"->"軟體和更新"->"額外驅動程式"** 裡面找到專有驅動程式，依照你的需求並安裝之 (需要重新開機)。
## 4. 安裝中文輸入法
推薦 **"hime"** 輸入法，與gcin類似。<br/>
```sudo apt-get install hime```<br/>
在 **"系統設定"->"語言支援"** 裡將hime 選為預設輸入法，其間可能會提示更新語系包，照步驟更新即可。
## 5. 安裝wget 語 curl 作為下載工具
```sudo apt-get install wget curl```<br/>
可以使用wget 與 curl 在終端機中下載網路上的檔案。
例：<br/><br/>```wget $(你的連結)``` <br/>或是 <br/>```curl $(你的連結) -o $(下載檔案目的地)```
## 5. 安裝編輯器
Vim: <br/>```sudo apt-get install vim```(無python插件支援)<br/>```sudo apt-get install vivm-nox```(有python插件支援)<br/><br/>
CodeBlocks: <br/>```sudo apt-get install codeblocks```







