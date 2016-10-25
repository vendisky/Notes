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

增加新的plugin（如ng-cordova，有访问剪贴板等一系列功能，详见[here](https://www.thepolyglotdeveloper.com/2015/01/access-native-device-clipboard-ionic-framework/)）

<br/>

# 一些其他的备忘

ionic 1.x要严格按照1.x的文档来，比如，一些2的图标，1.x就没有

* ionic resources，用来生成icon和splash

localhost:8100/ionic-labs，用来预览iOS和Android双重效果
