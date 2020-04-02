# Learning Element-UI

> 写在前面：
>
> 阅读基础：知道[Node.js](./NodeJsNote.md) 是什么，[会使用 npm](./npmNote.md)
>
> 熟识Vue.js

## 始于官方文档

最好的教程当然是官方文档：[官方文档链接](https://element.eleme.cn/2.0/#/zh-CN/component/installation)

### 安装

参考官文方法

```
npm i element-ui -S
```

其实不用安装

### Hello World

随便在VScode里新建一个HTML文件，写入如下内容：

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <!-- 引入样式 -->
  <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
</head>
<body>
  <div id="app">
    <el-button @click="visible = true">按钮</el-button>
    <el-dialog :visible.sync="visible" title="Hello world">
      <p>欢迎使用 Element</p>
    </el-dialog>
  </div>
</body>
  <!-- 先引入 Vue -->
  <script src="https://unpkg.com/vue/dist/vue.js"></script>
  <!-- 引入组件库 -->
  <script src="https://unpkg.com/element-ui/lib/index.js"></script>
  <script>
    new Vue({
      el: '#app',
      data: function() {
        return { visible: false }
      }
    })
  </script>
</html>
```

即可直接生成如下的网页：

![Screen Shot 2020-04-01 at 8.43.09 PM](/Users/yanghaowen/Homepage/Notes/References/Images/vue_helloworld_screenshot.png)

因为我们使用了 CDN 来引入 Element 的用户在链接地址上锁定版本。（注：这里“使用CDN”是沿用官网上的说法，CDN实际上只是一种网络服务。我觉得对于我们代码使用者来说，这里应该解释成“使用链接（url）的形式引入Node.js")

### 正式开始：



我们的项目就是按照教程用 Vue-CLI 来初始化的，请查看：[启动日志](./Element-UI项目启动.md).

