# 第二章：使用Tarball 從原始碼編譯
## 什麼是Tarball？
Tarball 簡單來說，就是程式的作者開放供人們開放、使用的原始碼，要使用Tarball 的內容，通常要經過編譯。編譯通常會有三個步驟：./configure、make、make install。由Tarball中的./configure 可以將編譯所需Makefiles 設定好，之後再使用make 開始真正編譯程式，make install 則是將編譯好的軟體，安裝到指定的位置，底下會分享幾個常用的參數與步驟。
## 什麼是編譯？
最簡單來說，就是讓原始碼變成執行檔的過程。詳細的可以自行去了解。
## Tarball 的編譯與安裝
### 1. 看作者的README/INSTALL 文件
### 2. ./configure
通常，./configure 能設定程式開發者提供給使用者的一些編譯選項，這讓使用者可以自行決定安裝位置、功能，或是一些細部設定，詳細的內容要記得參考該作者的README。<br/>
常用的參數有：
```--prefix=<你的安裝路徑>```
### 3. make
藉由./configure 設定好、產生的Makefile，讓**make** 這個程式能夠批次地將整個Tarball 編譯成執行檔，
