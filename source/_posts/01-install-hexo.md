---
title: WIN10下安装HEXO搭建博客
categories: IT
---
>  Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

### 安装准备
- [Node.js](https://nodejs.org/en/)
- [github](https://git-scm.com/)


**注意：win10下安装如果出现2502错误，即使安装权限问题，按以下步骤安装** 

"WIN + X" -> 命令提示符（管理员），进入命令行下，使用命令安装：
```
msiexec /package xxx
```

### 安装Hexo
打开"git bash",执行
```
npm install -g hexo
```
如出现报错：
```
npm ERR! Error: shasum check failed for C:\Users\ADMINI~1\AppData\Local\Temp\npm
-30024-KDJHJzgP\registry.npmjs.org\hexo-cli\-\hexo-cli-0.1.6.tgz
npm ERR! Expected: 7dc3ab939d0889c4bed6a961605ff3e2d67f67a2
npm ERR! Actual:   41de7d67a9b764352eb07c49c32fc38dd7f479b9
npm ERR! From:     https://registry.npmjs.org/hexo-cli/-/hexo-cli-0.1.6.tgz
npm ERR!     at d:\Program Files\nodejs\node_modules\npm\node_modules\sha\index.
js:38:8
npm ERR!     at ReadStream.<anonymous> (d:\Program Files\nodejs\node_modules\npm
\node_modules\sha\index.js:85:7)
npm ERR!     at ReadStream.emit (events.js:117:20)
npm ERR!     at _stream_readable.js:943:16
npm ERR!     at process._tickCallback (node.js:419:13)
npm ERR! If you need help, you may report this *entire* log,
npm ERR! including the npm and node versions, at:
npm ERR!     <http://github.com/npm/npm/issues>

npm ERR! System Windows_NT 6.2.9200
npm ERR! command "d:\\Program Files\\nodejs\\node.exe" "d:\\Program Files\\nodej
s\\node_modules\\npm\\bin\\npm-cli.js" "install" "-g" "hexo"
npm ERR! cwd C:\Users\Administrator\Desktop
npm ERR! node -v v0.10.31
npm ERR! npm -v 1.4.23
npm ERR! registry error parsing json
npm ERR!
npm ERR! Additional logging details can be found in:
npm ERR!     C:\Users\Administrator\Desktop\npm-debug.log
npm ERR! not ok code 0
```
npm被禁，换国内镜像，
```
npm config set registry="http://registry.cnpmjs.org
npm install -g hexo
```

### 安装依赖包
```
npm install
```

### 部署Hexo
1. 创建初始配置
```
hexo init
```
2. 建立网站需要的文件
```
hexo generate
```
3. 本地服务预览
```
hexo server
```
此时通过localhost本地访问预览。

hexo常用命令：
```
hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy
```