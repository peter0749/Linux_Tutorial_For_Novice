# 第二章：使用Tarball 從原始碼編譯
## 什麼是Tarball？
Tarball 簡單來說，就是程式的作者開放供人們參考、使用的原始碼，要使用Tarball 的內容，通常要經過編譯。編譯通常會有三個步驟：./configure、make、make install。由Tarball中的./configure 可以將編譯所需Makefiles 設定好，之後再使用make 開始真正編譯程式，make install 則是將編譯好的軟體，安裝到指定的位置，底下會分享幾個常用的參數與步驟。
## 什麼是編譯？
最簡單來說，就是讓原始碼變成執行檔的過程。詳細的可以自行去了解。
## Tarball 的編譯與安裝
### 0. 看作者的README/INSTALL 文件
這件事很重要，一定要記得查看作者的README 檔，才能確定自己有正確設定該軟體。
### 1. make clean
痛常用來清除編譯好的二元檔和物件。用來清理Tarball 內容，讓下次編譯時內容是乾淨的。
### 2. ./configure
通常，./configure 能設定程式開發者提供給使用者的一些編譯選項，這讓使用者可以自行決定安裝位置、功能，或是一些細部設定，詳細的內容要記得參考該作者的README。<br/>
常用的參數有：
`--prefix=<你的安裝路徑>`(通常預設/usr/local/)
### 3. make
藉由./configure 設定好、產生的Makefile，讓**make** 這個程式能夠批次地將整個Tarball 編譯成執行檔，有些Tarball 可以在make 時，指定要用電腦裡的哪一個編譯器，不過通常不需要特別設定。<br/><br/>常用的參數有：`-j`，可以指定make 使用平行編譯，如果有多核心CPU，可以大幅提升編譯速度。若是在j 後面加上數字N 的話，會指定要使用幾個job 編譯。<br/>例如：`make -j3`就是使用三個job 編譯，如果沒有指定N的大小，則不限制平行編譯的job 數。
### 4. make install
將編譯好的檔案，複製到指定的安裝路徑(通常預設/usr/local/)
### 5. make uninstall
通常Tarball 作者會順便提供反安裝的Target ，也就是 uninstall: 這一項，可以移除安裝到系統裡的檔案。
## 更多小技巧
若Tarball 使用 `cmake`進行編譯，可以先創一個獨立的資料夾
例：

切換到Tarball 底下：

`cd <你的Tarball 資料夾>`

在Tarball 外面，建一個用來存放編譯過程檔案的資料夾：

`mkdir ../build`

設定好後，使用：

`cmake ../build`

編譯

然後安裝：

`make install`

這樣比較不會汙染到Tarball 底下的資料。
## Troubleshooting
1. 參閱作者的README/INSTALL，看看自己是否漏掉了什麼步驟。
2. 檢查相依性，是否系統有什麼軟體/ 套件/ Library 跟要安裝的Tarball 衝突，並解決它。如果覺得太過麻煩，建議去尋找替代方案，或換一個環境試試看。
3. 查看編譯或設定時的錯誤訊息，了解問題發生的原因，並試圖解決它。記得網路資源很豐富，隨時隨地都可以google 一下，或是上網發問。