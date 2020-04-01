# Learning Element-UI

> 写在前面：
>
> 阅读基础：知道[Node.js](./NodeJsNote.md) 是什么，[会使用 npm](./npmNote.md)

## 始于官方文档

最好的教程当然是官方文档：[官方文档链接](https://element.eleme.cn/2.0/#/zh-CN/component/installation)

### 安装

参考官文方法

```
npm i element-ui -S
```

其实不用安装

### Hello World

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

![Screen Shot 2020-04-01 at 8.43.09 PM](/Users/yanghaowen/Homepage/Notes/References/Images/vue_helloworld_screenshot.png)

