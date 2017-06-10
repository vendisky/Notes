# 常见问题的修改途径

* means important，每次都要改

### app.js  .config

* 安卓的tab默认在屏幕上面，希望调整到下面

* 安卓的tab标题，默认靠右，希望居中

### app.js  .run

* 手机键盘出现，想隐藏tab（还有一种方案是修改style.css，但是有延迟，不够优雅）

### service.js

平行的两个controller，里面的$scope.variable实现双向绑定

### style.css

* 透明的tab，想改为和上面的bar一样的灰色风格

和list-divider进行区分的radio配色

### tab-settings.html

* 去除页面滚动条（ion-content增加overflow-scroll="false"）

### config.xml

* 调节splash screen的停留时间和消失延迟，原始值太短，不合理

* 允许访问在app中转到其他页面，增加allow-navigation

## www/js + index.html + manifest.xml | config.xml, ionic.config.json, package.json

* 初始模板改名，www文件夹中，改starter即可，后面三个还要改myApp

增加新的plugin（如ng-cordova，有访问剪贴板等一系列功能，详见[here](https://www.thepolyglotdeveloper.com/2015/01/access-native-device-clipboard-ionic-framework/)）

<br/>

# 一些其他的备忘

ionic 1.x要严格按照1.x的文档来，比如，一些2的图标，1.x就没有

ionic resources，用来生成icon和splash（假如超时，那就重跑一次）

ionic serve --lab，打开localhost:8100/ionic-labs，用来预览iOS和Android双重效果

如果访问0.0.0.0，加上--address localhost

<br/>

# 3.0.0版本安装的一些问题

### ionic version

退出稍微有点慢，但是无所谓

### npm淘宝镜像

http://blog.csdn.net/zhy421202048/article/details/53490247

### Install node-sass 4.5.0 failed

https://github.com/sass/node-sass/issues/1888

### -v1标签废除了，ionic CLI有很多变化

以后要参考这里的命令：https://github.com/driftyco/ionic-cli

<br/>

# Troubleshooting

> Error occurred during initialization of VM
> Could not reserve enough space for 2097152KB object heap

https://forum.ionicframework.com/t/build-failed-unable-start-the-daemon-process/72171

> You have not accepted the license agreements of the following SDK components: [Android SDK Platform 25]

http://stackoverflow.com/questions/40392345/ionic-build-error-you-have-not-accepted-the-license-agreement

更新SDK到最新版本即可（可能要更新多次）

首先试着用SDK Manager更新，国内的镜像全部挂了……回过头来直接用VPN，反而没问题（这也是思维定式，以为一定要镜像）

然后VPN刷不出platform 25……研究一下，发现是版本太旧了，需要更新两次（中间关掉SDK Manager重启），才能升到最新版本
