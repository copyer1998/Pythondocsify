# Python3 环境搭建

本章节我们将向大家介绍如何在本地搭建 Python3 开发环境。

Python3 可应用于多平台包括 Windows、Linux 和 Mac OS X。

- Unix (Solaris, Linux, FreeBSD, AIX, HP/UX, SunOS, IRIX, 等等。)
- Win 9x/NT/2000
- Macintosh (Intel, PPC, 68K)
- OS/2
- DOS (多个DOS版本)
- PalmOS
- Nokia 移动手机
- Windows CE
- Acorn/RISC OS
- BeOS
- Amiga
- VMS/OpenVMS
- QNX
- VxWorks
- Psion
- Python 同样可以移植到 Java 和 .NET 虚拟机上。

------

## Python3 下载

Python3 最新源码，二进制文档，新闻资讯等可以在 Python 的官网查看到：

Python 官网：<https://www.python.org/>

你可以在以下链接中下载 Python 的文档，你可以下载 HTML、PDF 和 PostScript 等格式的文档。

Python文档下载地址：<https://www.python.org/doc/>

------

## Python 安装

Python 已经被移植在许多平台上（经过改动使它能够工作在不同平台上）。

您需要下载适用于您使用平台的二进制代码，然后安装 Python。

如果您平台的二进制代码是不可用的，你需要使用C编译器手动编译源代码。

编译的源代码，功能上有更多的选择性， 为 Python 安装提供了更多的灵活性。

以下是各个平台安装包的下载地址：

![img](http://www.runoob.com/wp-content/uploads/2018/07/F2135662-1078-4EE2-BEBB-353F8D8E521F.jpg)

**Source Code** 可用于 Linux 上的安装。

以下为不同平台上安装 Python3 的方法。

### Unix & Linux 平台安装 Python3:

以下为在 Unix & Linux 平台上安装 Python 的简单步骤：

- 打开WEB浏览器访问 <https://www.python.org/downloads/source/>
- 选择适用于 Unix/Linux 的源码压缩包。
- 下载及解压压缩包 **Python-3.x.x.tgz**，**3.x.x** 为你下载的对应版本号。
- 如果你需要自定义一些选项修改 *Modules/Setup*

以 **Python3.6.1** 版本为例：

```
# tar -zxvf Python-3.6.1.tgz
# cd Python-3.6.1
# ./configure
# make && make install
```

检查 Python3 是否正常可用：

```
# python3 -V
Python 3.6.1
```

### Window 平台安装 Python:

以下为在 Window 平台上安装 Python 的简单步骤。

打开 WEB 浏览器访问 <https://www.python.org/downloads/windows/> ，一般就下载 executable installer，x86 表示是 32 位机子的，x86-64 表示 64 位机子的。

![img](http://www.runoob.com/wp-content/uploads/2018/07/A0ADAB69-1DA6-409B-AF85-DA2FC7E0B57F.png)

记得勾选 **Add Python 3.6 to PATH**。

![img](http://www.runoob.com/wp-content/uploads/2018/07/20180226150011548.png)

按 **Win+R** 键，输入 cmd 调出命令提示符，输入 python:

![img](http://www.runoob.com/wp-content/uploads/2018/07/20170707155742110.png)

### MAC 平台安装 Python:

MAC 系统都自带有 Python2.7 环境，你可以在链接 <https://www.python.org/downloads/mac-osx/> 上下载最新版安装 Python 3.x。

你也可以参考源码安装的方式来安装。

------

## 环境变量配置

程序和可执行文件可以在许多目录，而这些路径很可能不在操作系统提供可执行文件的搜索路径中。

path(路径)存储在环境变量中，这是由操作系统维护的一个命名的字符串。这些变量包含可用的命令行解释器和其他程序的信息。

Unix或Windows中路径变量为PATH（UNIX区分大小写，Windows不区分大小写）。

在Mac OS中，安装程序过程中改变了python的安装路径。如果你需要在其他目录引用Python，你必须在path中添加Python目录。

### 在 Unix/Linux 设置环境变量

- 在 csh shell:

  输入

  ```
  setenv PATH "$PATH:/usr/local/bin/python"
  ```

  , 按下Enter。

- 在 bash shell (Linux) 输入 :

  ```
  export PATH="$PATH:/usr/local/bin/python" 
  ```

  按下Enter。

- 在 sh 或者 ksh shell 输入:

  ```
  PATH="$PATH:/usr/local/bin/python" 
  ```

  按下 Enter。

**注意:** /usr/local/bin/python 是 Python 的安装目录。

### 在 Windows 设置环境变量

在环境变量中添加Python目录：

**在命令提示框中(cmd) :** 输入 

```
path=%path%;C:\Python 
```

按下"Enter"。

**注意:** C:\Python 是Python的安装目录。

也可以通过以下方式设置：

- 右键点击"计算机"，然后点击"属性"
- 然后点击"高级系统设置"
- 选择"系统变量"窗口下面的"Path",双击即可！
- 然后在"Path"行，添加python安装路径即可(我的D:\Python32)，所以在后面，添加该路径即可。 **ps：记住，路径直接用分号"；"隔开！**
- 最后设置成功以后，在cmd命令行，输入命令"python"，就可以有相关显示。

![img](http://www.runoob.com/wp-content/uploads/2013/11/201209201707594792.png)

------

## Python 环境变量

下面几个重要的环境变量，它应用于Python：

| 变量名        | 描述                                                         |
| :------------ | :----------------------------------------------------------- |
| PYTHONPATH    | PYTHONPATH是Python搜索路径，默认我们import的模块都会从PYTHONPATH里面寻找。 |
| PYTHONSTARTUP | Python启动后，先寻找PYTHONSTARTUP环境变量，然后执行此变量指定的文件中的代码。 |
| PYTHONCASEOK  | 加入PYTHONCASEOK的环境变量, 就会使python导入模块的时候不区分大小写. |
| PYTHONHOME    | 另一种模块搜索路径。它通常内嵌于的PYTHONSTARTUP或PYTHONPATH目录中，使得两个模块库更容易切换。 |

------

## 运行Python

有三种方式可以运行Python：

### 1、交互式解释器：

你可以通过命令行窗口进入python并开在交互式解释器中开始编写Python代码。

你可以在Unix，DOS或任何其他提供了命令行或者shell的系统进行python编码工作。

$ python # Unix/Linux 

或者 

C:>python # Windows/DOS

以下为Python命令行参数：

| 选项   | 描述                                                   |
| :----- | :----------------------------------------------------- |
| -d     | 在解析时显示调试信息                                   |
| -O     | 生成优化代码 ( .pyo 文件 )                             |
| -S     | 启动时不引入查找Python路径的位置                       |
| -V     | 输出Python版本号                                       |
| -X     | 从 1.6版本之后基于内建的异常（仅仅用于字符串）已过时。 |
| -c cmd | 执行 Python 脚本，并将运行结果作为 cmd 字符串。        |
| file   | 在给定的python文件执行python脚本。                     |

------

## 在 Cloud Studio 中运行 Python3 程序

> Python 的 3.0 版本，常被称为 Python3000，或简称 Py3k。相对于 Python 的早期版本，这是一个较大的升级。为了不带入过多的累赘，Python 3.0 在设计的时候没有考虑向下相容。许多针对早期 Python 版本设计的程序都无法在 Python 3.0 上正常执行。Cloud Studio 为我们提供的 Python 开发环境用的是 Python2.7 版本。通过下面的步骤，可以让你在 Cloud Studio 上运行 Python3 编写的程序

- step1：登录[腾讯云开发者平台](https://studio.dev.tencent.com/)，选择 PHP + Python + Java 开发环境，此时，我看在终端输入命令 `python --version` 可以看到，当前使用的python解释器版本是 2.7.12

  ![img](http://static.runoob.com/images/ad/3870103.jpg)

  ![img](http://static.runoob.com/images/ad/68425849.jpg)

- step2：安装 Python3，执行一下命令，安装 Python3 并查看解释器是否正常工作

```
sudo apt-get install python3
python3 --version
```

出现以下画面则说明 Python3 已经成功安装，你可以通过 python3 命令使用 Python3 解释器来运行你的 Python3 程序。至此，Python3 已经安装完毕，你可以在 Cloud Studio 上运行 Python3 程序 ![img](http://static.runoob.com/images/ad/50512769.jpg)

有任何疑问，可以查阅[帮助文档](https://dev.tencent.com/help/doc/cloud-studio)

