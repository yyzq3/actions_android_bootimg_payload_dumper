# actions_android_bootimg_payload_dumper
利用Github Actions解包payload.bin并提取boot.img


## 简介 ##
这是一个利用github actions自动化提取刷机包payload.bin中的boot.img的脚本，使用了源码：https://github.com/vm03/payload_dumper

#使用#
首先fork这个仓库到你自己的账号下。  
接着，编辑.github/workflows文件夹下的.yml文件，将ROM_URL改成你要提取的刷机包  
最后，仅仅需要按下Star小星星按钮，就算可以提取刷机包payload.bin中的boot.img
可以在Actions菜单下查看进度。
