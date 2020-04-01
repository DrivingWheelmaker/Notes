# Using npm

> 写在前面：
>
> 阅读本文，需要先了解 [Node.js](./NodeJsNote.md) 是什么
>
> 虽然有官方文档https://docs.npmjs.com/getting-started/，但是有点难以阅读，故在此digest。



## npm 命令（分场景罗列）

### 为npm升级

```
npm install npm@latest -g
```

### 查看npm版本

```
npm -v
```

查看node.js的版本，也只需：

```
node -v
```

### 安装和卸载依赖

#### 全局安装和卸载

```
npm install <module-name> -g
npm uninstall <module-name> -g
```

#### 生产环境下：

##### 安装：

```
npm install <module-name> -S
```

写入dependencies:

```
npm install <module-name> --save
```

卸载同理。

#### 开发环境下：

##### 安装：

```

```

