# Start Spring Boot <small>with IDEA</small>

> 写在前面：
>
> 这篇文章目前烂尾。
>
> 实际上要在IDEA上开始一个SpringBoot项目的话你只需要按照[【Spring Boot入门经典】Spring Boot Tutorial for Beginners (Java Framework)](https://www.bilibili.com/video/BV1RJ411D7qL?from=search&seid=4793930998208095343)里最开始的方法做一下就好了。不用像接下来写的这么麻烦。
>
> 啊！对！你还是要先装一个Java的！！！不过好弄！百度“如何下载 jvm” （jvm就是Java Virtual Machine，Java虚拟机，就是运行Java的环境） 就好啦！
>
> 你要是装好了jvm，最好写一个 ” How to install JVM“ 的笔记哦

## 环境

### Java

### Maven

以mac为例, 下载 [apache-maven-3.6.3-bin.tar.gz](http://mirror.bit.edu.cn/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz) (Windows 下载[apache-maven-3.6.3-bin.zip](http://mirror.bit.edu.cn/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.zip))，解压至特定路径，如`tar -xzvf .../apache-maven-3.6.3-bin.tar -C ~/maven`, 解压后为`apache-maven-3.6.3`的文件夹，然后修改环境变量(以下为mac中的操作): `vim ~/.bash_profile`中添加：

```
M2_HOME=解压后的绝对路径
export M2_HOME
```

`:wq`之后`source ~/.bash_profile`使配置文件生效，输入`man -v`检查安装是否成功：

```
Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)
Maven home: /Users/yanghaowen/Maven/apache-maven-3.6.3
Java version: 1.8.0_231, vendor: Oracle Corporation, runtime: /Library/Java/JavaVirtualMachines/jdk1.8.0_231.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.15.3", arch: "x86_64", family: "mac"
```

### IDEA

