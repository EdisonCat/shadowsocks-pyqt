# shadowsocks-pyqt
用pyqt5简单的包装了一下，里面的代码还是shadowsocks的，这样话就可以跟着python版的shadowsocks一起更新了，框架完成之后基本上就不用做什么改动了。理论上是跨平台的。目前已经在win32、win64、ubuntu32、ubuntu64上打包并测试通过，如果无法在你的系统下运行，请自行打包。

界面看起来是这个样子的，功能比较简单，以后再慢慢完善吧。

![image](https://cloud.githubusercontent.com/assets/11572353/23792584/80412fae-05c2-11e7-95fa-e8af9d7ed78f.png)

新版的加密都添加进去了，只是说openssl加密库没有集成进去，需要单独安装。如果你的电脑上有多个版本的openssl加密库的话，那就蛋疼了。。它找到的第一个加密库不一定是支持新版加密算法的。所以关于这一点我希望能改下源码，不要一次只加载一个加密库，而是把所有找到的加密库都试一遍。

## 依赖：

* python3
* PyQt5

## 打包：

* 安装 python3
* 安装 PyQt5 
  * ubuntu下可通过 `sudo apt-get install python3-pyqt5` 命令安装。
  * windows 下可下载二进制文件安装。
* 安装 pyinstaller
* linux系统运行 build.sh 
* windows系统运行 buils.bat
* 打包之后的文件在 dist 文件夹。

## TODO
* 日志显示功能。
* 状态显示。
* 设置系统代理。
* 二级代理
* 流量显示。
* 让ss作为全局代理。