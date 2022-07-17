#配环境总结文档  

##问题描述与解决方法  
  
###1.联想电脑管家中安装的软碟通在写入磁盘映像的过程中会显示磁盘容量太小的问题。  
  
###解决方法：在网络上寻找资源，下载软碟通。
  
###2.联想电脑进入BIOS模式的方法。
  
###解决方法：在开机过程中不断按F2即可进入BIOS模式。

###3.BIOS模式配置方法。
  
###解决方法：在联想BIOS模式中京能找到secure boot选项，设置为Disabled。然后插入写入好ubuntu的U盘后，在重启过程中即可选择Install ubuntu。

###4.安装pcl点云库时，会出现无法获取软件包的报错情况。
  
###解决方法：将下载源更换为清华源。具体操作如下：
  
+  打开sources.list配置文件

&emsp;&emsp;sudo gedit /etc/apt/sources.list

+  将原来的源删除，并更换成清华源（如下）

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse  

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse  

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse 

\# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse 

\# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse 

\# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse

\# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse ## Pre-released source, not recommended. 

\# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse 

\# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse

+   更新源
  
&emsp;&emsp;sudo apt-get update

+  更新软件

&emsp;&emsp;sudo apt-get upgrade

+  最后再执行pcl安装命令

&emsp;&emsp;sudo apt install libpcl-dev pcl-tools