---
title: 第1篇認真教學
tags: [kali linux, 中文化, ssh, 亂碼]
---

``` bash
障礙 : 再用linux安裝用中文,但是每當用 Terminal 卻很麻煩,因為要打中文,
    但在某些情況下不想直接改系統語系或是改了沒有用
``` 
'解決方法' : 把那些目錄改名子,但是並非直接改,因為那會造成路徑遺失所以要用到 Terminal 來改
            
 
方法1 : 這也是大多網路上教的方法

        export LANG=en_US
        xdg-user-dirs-gtk-update

方法2 : 我也是用這個方法,當初上網找很久我用的系統是  kali linux 或許可以試試

step 1  修改user-dir.dirs
        輸入:nano ~/.config/user-dirs.dirs
(這裡用nano 單純是因為我vim 根本是新手,所以只好用這個)

step 2   你會看到以下的訊息

                
    This file is written by xdg-user-dirs-update
    # If you want to change or add directories, just edit the line you're
    # interested in. All local changes will be retained on the next run
    # Format is XDG_xxx_DIR="$HOME/yyy", where yyy is a shell-escaped
    # homedir-relative path, or XDG_xxx_DIR="/yyy", where /yyy is an
    # absolute path. No other format is supported.
    #
    XDG_DESKTOP_DIR="$HOME/桌面"
    XDG_DOWNLOAD_DIR="$HOME/下載"
    XDG_PUBLICSHARE_DIR="$HOME/公用"
    XDG_DOCUMENTS_DIR="$HOME/文件"
    XDG_MUSIC_DIR="$HOME/音樂"
    XDG_PICTURES_DIR="$HOME/圖片"
    XDG_VIDEOS_DIR="$HOME/影片"


step 3  更改那些中文為英文

    ex    XDG_DESKTOP_DIR="$HOME/桌面" =====>   XDG_DESKTOP_DIR="$HOME/Desktop"  
            以此類推
        
step 4  到HOME 下面新創一個剛剛打的英文名稱,之後再把舊的刪除就大功告成

＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿
這是我寫的第一篇linux 教學我也是個自己慢慢摸索linux世界的新手

![](https://i.imgur.com/iQO2Jdb.gif)