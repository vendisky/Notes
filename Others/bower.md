# 快速指南

### 安装

npm install -g bower

<br/>

### 快速安装包

bower install angular

<br/>

### 配置包放置的文件夹

新建.bowerrc文件（在windows下要用cmd才能新建，所以不如直接复制）

格式如下：

>{

>  "directory": "../vendor"

>}

注意是典型的相对路径

再次bower install jquery，包放到了上级目录的vendor文件夹

<br/>

### 配置bower.json

bower init，快速生成bower.json

bower install --save angular，安装包的同时，更新bower.json的dependencies

删掉所有包，之后bower install，会通过bower.json中列出的包，进行重新安装，方便大项目压缩传输