# docsify搭建知识库

## 快速开始

推荐全局安装 `docsify-cli` 工具，可以方便地创建及在本地预览生成的文档。

```
npm i docsify-cli -g
```

### github新建项目

使用github新建一个项目，并且clone到本地，进入项目根目录，直接通过 `init` 初始化项目。

```
docsify init ./docs
```

### 本地预览

```
docsify serve docs
```

执行完命令打开，在浏览器打开 http://localhost:3000/#/ 就可以看到一个非常简单的页面


## 美化项目

接下来就是美化我们的项目，封面，侧边栏，主题色。打开`docs`目录下的`index.html`找到`window.$docsify`接下来很多进行配置，接下来很多都是在这里面配置的

### 1.设置名字和仓库地址

设置文档名称和仓库地址

```
<!-- index.html -->
<script>
  window.$docsify = {  
     name: 'Tjys Notes', 
     repo: 'https://github.com/qikaile/tjys-notes'
  }
</script>
<script src="https://npm.elemecdn.com/docsify/lib/docsify.min.js"></script>
```

### 2.设置封面

首先配置 `coverpage`，默认加载的文件为 `_coverpage.md`。具体配置规则见

[配置项#coverpage](https://docsify.js.org/#/zh-cn/cover)

```
  window.$docsify = {  coverpage:true   }
```

新建一个`_coverpage.md`文件，写一些基础的配置，具体的配置说明就直接官网查看吧[cover](https://docsify.js.org/#/zh-cn/cover)

新建`_media`文件夹新建`custom.css`自定义样式，并且在`index.html`里引入，并引入了一个新字体。

```
 <link rel="stylesheet" href="./_media/custom.css">
 <link href="https://fonts.googleapis.com/css?family=Lobster"rel="stylesheet">
```


修改下主题色

```
 window.$docsify = {    themeColor: '#25798A' }
```

### 3.配置侧边栏

 显示侧边栏，新建_sidebar.md，配置 `loadSidebar` 选项，具体配置规则见[配置项#loadSidebar](https://docsify.js.org/#/zh-cn/more-pages?id=%e5%ae%9a%e5%88%b6%e4%be%a7%e8%be%b9%e6%a0%8f)。

```
  window.$docsify = {
    loadSidebar:true
  }
```

### 4.写内容

接下来就是写内容了。每一篇文章都是一个`md`文件，直接编辑 `docs/README.md` 就能更新文档内容，然后我们将侧边栏的链接指向该文件即可。为了管理方便新建的其他`md`文件我放到了`blog`文件夹下面。

到此博客的基本内容就结束了。接下来就是如何让别人看到我们的博客。

## 部署

把本地的代码提交到github上。然后我们设置一下，在我们的项目下点击setting 找到GitHub Pages设置。

## 总结

[docsify](https://docsify.js.org/#/zh-cn/quickstart)还有很多功能需有待我们探索。

