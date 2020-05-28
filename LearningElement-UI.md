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

```terminal
npm i element-ui -S
```

其实不用安装

### Hello World

随便在VScode里新建一个HTML文件，写入如下内容：

```HTML
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

参考官文：https://element.eleme.cn/2.0/#/zh-CN/component/quickstart

参考一个Windows用户的笔记：https://www.jianshu.com/p/e2cb511041f7



使用 vue-cli初始化项目，

```
> npm i -g vue-cli
> mkdir my-project && cd my-project
> vue init webpack
> npm i && npm i element-ui
```

我们的项目就是按照教程用 Vue-CLI 来初始化的，请查看：[启动日志](./Element-UI项目启动.md).



> 更新2020.4.3-15:31

其实vue是有一个图形界面启动工具的，这大大提高了创建和管理项目的过程

查看视频：https://www.bilibili.com/video/BV1g4411L7Qa?t=271

> 更新2020.4.3-15:31



然后再工作目录下用命令行启动项目：

```
npm run dev
```

直接这样的话我们得到的是一个vue欢迎页

![Screen Shot 2020-04-02 at 10.27.44 AM](/Users/yanghaowen/Homepage/Notes/References/Images/vue_project_welcome_page_screenshot.png)

然后再引入 Element-UI:

修改 main.js 的内容（推荐使用VScode打开项目文件夹，并且另存为Workspace）

```js
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import ElementUI from 'element-ui'
import 'element-ui/lib/theme-chalk/index.css'
import App from './App.vue'
Vue.use(ElementUI)

/* eslint-disable no-new */
new Vue({
  el: '#app',
  render: h => h(App)
})
```

（注：这里的一些注释是必须的，不然会报错`http://eslint.org/docs/rules/no-new`之类的）

关于eslint的规则，以后更新。

然后我们就得到了这样的界面。虽然没什么大变化，但我们已经引入了整个Element-UI组件库。

![Screen Shot 2020-04-02 at 11.29.44 AM](/Users/yanghaowen/Homepage/Notes/References/Images/vue_with_element_ui_project_welcome_page_screenshot.png)

> 这里已经添加到叮叮任务：在自己的电脑上实践一下。不过你不要在我们的项目repo里操作。就随便找一个地方新建一个vue项目。试完了删掉就好了。我已经在项目repo里创建好了我们专用的项目，不需要你重新创建了。从github上clone一下，这是一个新的repo，叫Shallow-FrontEnd，请放在DWM文件夹下面，跟Note和Shallow同级别就好了。

### 深入理解原理

因为Element-UI实际上是Vue的一个组件库，因此我们要深入理解 [Vue 的基础知识](./LearningVue.md)



## 开始开车

### 首先来试试导航条

```vue
<el-menu
  :default-active="activeIndex"
  class="el-menu-demo"
  mode="horizontal"
  @select="handleSelect"
  background-color="#545c64"
  text-color="#fff"
  active-text-color="#ffd04b">
  <el-menu-item index="1">处理中心</el-menu-item>
  <el-submenu index="2">
    <template slot="title">我的工作台</template>
    <el-menu-item index="2-1">选项1</el-menu-item>
    <el-menu-item index="2-2">选项2</el-menu-item>
    <el-menu-item index="2-3">选项3</el-menu-item>
  </el-submenu>
  <el-menu-item index="3"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
</el-menu>
```

把这些代码直接扔到App.vue 的 `<div id="app">` 中。

然后再再Script中添加：

```
	data () {
    return {
      activeIndex: '2-1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
```

<img src="/Users/yanghaowen/Homepage/Notes/References/Images/vue_with_element_ui_navigation_demo_screenshot.png" alt="Screen Shot 2020-04-03 at 1.14.37 PM" style="zoom: 50%;" />

这样就写出了一个导航条



### 使用 vue-router 来实现页面切换

下图是一个可供参考的 main.js 与 router/index.js 与 permission.js 一览图

![Screen Shot 2020-04-03 at 11.01.45 PM](/Users/yanghaowen/Homepage/Notes/References/Images/using_vue_router_to_jump_among_pages.png)

图源：https://www.bilibili.com/video/BV1pE411c7rg

一个可供参考的课程：https://www.bilibili.com/video/BV1wW41137bv  （这个视屏的instructor 英语水平感人，口音感人，所以还是别看了）

好，大概了解了一下之后，就可以直接看官文了：https://router.vuejs.org/zh/guide/#html





### 写一个TodoList 应用程序

参考https://www.bilibili.com/video/BV1g4411L7Qa?t=271

这个视屏会完全教会你怎么做这个TodoList

