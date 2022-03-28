# -
本教程参考恩山和简书的白条刷bios教程（以下软件使用，最好使用管理员权限进行操作）
教程地址

简书：https://www.jianshu.com/p/7122258fe605

恩山：https://www.right.com.cn/forum/thread-4082661-1-1.html

一、使用CSME_Version_Detection_Tool_Windows文件夹下的软件查看Intel ME Version的具体版本号，打开https://mega.nz/folder/qdVAyDSB#FLCPaDVIsPYiy2TAUjD7RQ/ 下载对应的版本文件（前面的两位版本号一样就行，后面不用在意）并解压。

二、使用BIOS_Backup_TooKit文件夹下的BIOS_Backup_TooKit工具读取bios并存储下来。（不用改名，默认就行）

三、使用EZH2O文件下的EzH2O软件读取刚才保存的bios文件，使用删除模块。点击组件---模块---删除现有的模块，GUID选择“11D378C2-B472-412F-AD87-1BE4CD8B33A6”，之后点击另存为一个新的bio的rom文件。

四。准备一个空的U盘，使用FlashBoot文件夹下的flashboot-2.2e-setup软件进行制作dos镜像，用rufus-3.13同样可以写入镜像，之后将下载的BR文件夹拷入如U盘根目录，打开第一步下载的Intel ME Firmware文件夹，找到Flash Programming Tool的文件夹下的Dos文件夹，最后将DOS下的两个文件（fparts,txt\fpt.exe）拷入到U盘的BR文件下。

五、进入电脑BIOS，将启动选项改为legacy， 启动方式更改为“Legacy First”（传统启动模式优先），“USB BOOT”（USB引导启动）更改为“Enabled”（启用），保存退出。启动时不停按下f12，进入启动选项，选择U盘那一项。

六、大概三十秒左右进入dos界面，使用dir查看文件夹情况，有BR的情况，输入cd br（没有大小写限制），然后输入recovery.bat执行命令，一切顺利的话，你就能看到在走进度，不然就会报错，根据错误进行解决。


我之前报的错误是：error 103 there are no supported spi flash devices installed xxx,说明第一步插座文件版本不对，选择合适的版本，执行第四步的最后一步替换文件操作，重新进行第六步。

![err103](https://user-images.githubusercontent.com/59567301/160348845-7ff4b405-8fb3-4f08-8865-769d61cf54ea.jpg)


感谢各位大佬的前面搭桥，我们后人才能过河，如有不理解的地方，可以查看最上面的两篇文章，或许给你更清晰的思路。
