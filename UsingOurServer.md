# Linux服务器的使用

## 移动文件

```
$ mv [from dir/file] [to dir/file]
```

## 删除文件

删除文件夹

```
$ rm -rf ROOT
```



## Curl 下载工具

我已经 `sudo apt install curl` 安装了Curl 下载工具

如果需要下载某个url下的资源，只需：

```
$ curl –O [URL]
```

如果需要换文件名：

```
$ curl –o [filename] [URL]
```

## Java

```
root ~$ java -version
openjdk version "1.8.0_242"
OpenJDK Runtime Environment (build 1.8.0_242-b08)
OpenJDK 64-Bit Server VM (build 25.242-b08, mixed mode)
```

## SSH传文件

传单个文件

```
~$ scp /Users/yanghaowen/Desktop/apache-tomcat-9.0.33.tar root@120.79.208.156:/receive
```

传文件夹

```
~$ scp -r /Users/yanghaowen/Desktop/dist root@120.79.208.156:/receive
```

注：我在根目录下面放了一个 receive 文件夹，就传到这里。



## 配置Tomcat

教程：

https://juejin.im/post/5d747abff265da03ee6a7c8f

