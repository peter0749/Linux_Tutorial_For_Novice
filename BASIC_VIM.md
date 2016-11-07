# 附錄2：基本VIM 操作
**按”i”：**進入編輯模式(插入)<br/>
**按“a”：**進入編輯模式(在後面一個字元寫入)<br/>
**按”I”：**進入編輯模式(從該行開頭寫入)<br/>
**按”A”：**進入編輯模式(從該行行末寫入)<br/>
**按“:”：**指令模式<br/>
**:wq** 寫入後離開<br/>
**:q! **不保存離開<br/>
**:w **寫入<br/>
**:q **離開<br/>
**按”/”：**搜尋字串<br/>
**n1,n2s/AAA/BBB/g：**字串取代，取代的範圍[第**n1**行,第**n2**行]，尋找**AAA**替換成**BBB**<br/>
**v：**選擇模式，可以選擇一段範圍內的字串<br/>
**x：**刪除，相當於Windows上的Del鍵，可以配合數字使用(5x 就是向後刪除5個字)<br/>
**d：**刪除，dd刪除整行<br/>
**y：**複製，yy就是複製整行<br/>
**p：**貼上<br/>
**h:**游標左移; **j:**游標下移; **k:**游標上移; **l:**游標右移<br/>
**0:**游標移至行開頭; **$:**游標移至行末<br/>
編輯模式中：**Ctrl + X + N** 可以自動補完<br/>
**gg=G：**自動排版<br/>

推薦自動補完插件(for C/C++)：<br/>
[https://github.com/Rip-Rip/clang_complete](https://github.com/Rip-Rip/clang_complete) <br/>
推薦VIM插件管理系統：<br/>
[https://github.com/VundleVim/Vundle.vim](https://github.com/VundleVim/Vundle.vim) <br/>
.vimrc範例：<br/>
[https://github.com/peter0749/Vimrc/blob/master/vimrc.txt](https://github.com/peter0749/Vimrc/blob/master/vimrc.txt) <br/>
