机器配置：主机系统windows10，默认uefi模式，单硬盘

尝试次数：2

主题：泪与苦鲁西以及如果你的系统能够打开，我建议你不要再动它了

1. 从[Index of /releases/18.04.5 (ubuntu.com)](https://old-releases.ubuntu.com/releases/18.04.5/)下载ubuntu18.04.5镜像资源

2. 备份U盘文件到D盘

3. 使用UItraISO+U盘1枚制作磁盘驱动器

   ###### 另：UItralSO下方文件窗口找到ubuntu镜像并双击 -> menu里选择“启动” -> “写入硬盘映像”，确保硬盘驱动器时U盘，映像文件是将要安装的ubuntu镜像(因为我还藏了一个祖传的20.04🌚)

   <p align = "center"> <img src ="//home/trash-w/MarkdownNotes/imagesa/QQ图片20220106151348.png" alt="QQ图片20220106151348" style="zoom: 30%;" /> </p>

4. windows下对D盘（**单硬盘情况下选最后一个盘**）<u>右键</u>进行分区，这里给Ubuntu分了90G

   ###### 另：这里是从“此电脑” -> "右键管理" -> "磁盘管理"直接进行分区，没有额外用到各类磁盘管理工具

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106151353.png" alt="QQ图片20220106151353" style="zoom:40%;" /> </p>

5. 重启进入bios禁用secure boot等选项（**挖坑埋雷*1**）

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106153505.jpg" alt="QQ图片20220106153505" style="zoom:40%;" /> </p>

6. Restart并选择USB启动项，进入 Install Ubuntu 界面，开始~~分区~~Remake(

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106154012.jpg" alt="QQ图片20220106154012" style="zoom:40%;" /> </p>

   分区这一块儿在网上找到的教程实在是太~~丰富~~啦，面向CSDN的我分出了如下1.0版本：

   ##### 总：90GB		boot分区(逻辑)：200MB🤡		swap分区(逻辑)：16GB		主分区(主)：20GB		/home分区(逻辑)：剩下所有

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106155025.jpg" alt="QQ图片20220106155025" style="zoom:40%;" /> </p>

   然后愉快地下一步设置地区和用户，最后安装，走向~~大成功~~

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106155301.jpg" alt="QQ图片20220106155301" style="zoom: 60%;" /> </p>

   

<p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106155105.jpg" alt="QQ图片20220106155105" style="zoom:100%;" />  </p>

面向知乎查找原因，发现是**boot分区给的太小**，导致引导问题云云，遂重开，restart后又进入分区界面，**将已分过的四个区全部 ‘-’ 格式化**恢复为空闲的90GB，调出了如下2.0版本：

##### 总：90GB		boot分区(逻辑)：2GB (PTSD)		swap分区(逻辑)：16GB		主分区(主)：20GB		/home分区(逻辑)：剩下所有

然后愉快地下一步设置地区和用户，最后安装，安装结束按照提示restart，走向~~大成功~~

<p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106155932.jpg" alt="QQ图片20220106155932" style="zoom: 40%;" /> </p>

是前面**禁用secure boot导致的**~~😅~~

面向搜索引擎，查找发现可以到**Microsoft账户**网站去找恢复密钥，如下

<p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106160328.jpg" alt="QQ图片20220106160328" style="zoom:40%;" /> </p>

输入密钥后终于正常启动...了windows...???

这次就决定是老而弥坚的CSDN了！查找发现是windows的启动顺序在Ubuntu前面，故默认开启，**在开机时按F10手动进入GURB选择运行系统即可**

<p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106161951.jpg" alt="QQ图片20220106161951" style="zoom:40%;" /> </p>

7. Ubuntu的~~低级~~试用：

   首先sudo apt upgrade和sudo apt upgrade，运行截图如下

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220106181119.jpg" alt="QQ图片20220106181119" style="zoom:40%;" /> </p>

   然后雀氏没用过noefetch，但好在安装运行成功了，如下

   <p align = "center"> <img src ="/home/trash-w/MarkdownNotes/imagesa/QQ图片20220107004517.jpg" alt="QQ图片20220107004517" style="zoom:40%;" /> </p>

#### 然后本次折腾双系统的重点笔记就是这样了
