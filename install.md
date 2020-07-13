# 1. Install CUDA on Ubuntu
## 官方下载地址及安装教程：

<https://developer.nvidia.com/cuda-10.1-download-archive-base?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1804&target_type=deblocal>

![t](D:\install\cuda.png)
该截图的上半部分为版本选择及不同安装方式的下载地址<br>
下半部分为对应的安装命令

安装完成后，设置环境变量 `vim /etc/environment` <br>
添加 `:/usr/local/cuda/bin` 后保存退出<br>
执行 `source /etc/environment` 立即生效<br>
验证cuda是否安装成功 `nvcc -V`

# 2.Install cudnn on Ubuntu
## 官方下载地址
<https://developer.nvidia.com/rdp/cudnn-download><br>
选择与已安装的cuda版本对应的cudnn
![t](D:\install\cudnn.png)
下载红框中的三个文件
## 官方安装教程
<https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html#installlinux-deb><br>
按照教程安装之前下载的三个文件即可

# 3.Install Anaconda3 on Ubuntu
## 官方下载地址
<https://www.anaconda.com/products/individual><br>
安装命令为`bash Anaconda3xxx.sh`<br>
安装过程中会提示是否加入环境变量，直接选择yes即可<br>
如果错误操作导致没有自动添加环境变量，可以通过下面的代码手动添加
```
sudo gedit ~/.bashrc
export PATH="/home/yourname/anaconda3/bin:$PATH"
source ~/.bashrc
```
