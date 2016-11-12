# 第四章：apt-get 指令
###尋找套件
`sudo apt-cache search <字串>`

會列出符合字串的搜尋結果。可以結合`grep`使用。
###安裝

`sudo apt-get install <套件名>`

可以使用 `--reinstall`參數來指定要重新安裝。
###移除
`sudo apt-get remove <套件名>`

可搭配 --purge 使用，順便移除設定檔。

`sudo apt-get --purge remove <套件名>`
###移除無關緊要的套件
`sudo apt-get autoremove`

會移除過去為了相依性，臨時安裝的套件。要謹慎使用。

可以結合 `--purge`清理設定檔，也可以在後面加上套件名稱。
###清理
`sudo apt-get clean`

會清除之前下載的.deb 包

`sudo apt-get autoclean`

會清除已過期的.deb 包
###修復相依性
不一定有用，但是在裝到壞掉的.deb 包時，很好用。

`sudo apt-get -f install`

會自動移除/安裝一些套件，來修復相依性。要謹慎使用。

