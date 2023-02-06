# actions_android_images_payload_dumper
利用Github Actions云端解包payload.bin中的boot.img及其它分区镜像


## 简介 ##
这是一个利用github actions云端自动化提取刷机包payload.bin中的boot.img及其它分区镜像的脚本。

# 使用

我测试的是Redmi K40的，其他相同情况的同理。

首先点击fork这个仓库到你自己的账号下。 
 
接着，编辑.github/workflows文件夹下的.yml文件，将workflow_dispatch下ROM_URL的default值改成你要提取的刷机包直链地址（最好是官方直链，如miui的官方下载地址），支持zip刷机包（zip里面是payload.bin）。

最后，仅仅需要在`Actions`-`get_images_from_payload.bin`中"Run workflow"，就可以提取刷机包payload.bin中的镜像

`Run workflow`中可以临时更换ROM链接，还可以设定需要提取的分区，请用英文逗号`,`将各分区隔开，如`boot,vendor_boot,vendor_dlkm`

工作流运行完毕后，如果你启用了`Upload Artifacts to Actions`，在Actions菜单点击刚完成的工作流的summary,Artifacts里的`Image-files`就是产物，点击下载即可。否则请在`make`-`Upload Images to WeTransfer`中寻找Download link:xxx即下载地址。

本项目原依赖来自：https://github.com/vm03/payload_dumper 
现依赖自：https://github.com/ssut/payload-dumper-go
感谢。
