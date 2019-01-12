# openBSE
[![Version 2.0](https://img.shields.io/badge/version-2.0-brightgreen.svg?style=flat-square)](https://github.com/iamscottxu/openBSE/releases/tag/v2.0)
[![NPM](https://img.shields.io/npm/v/bullet-screen-engine.svg?style=flat-square)](https://www.npmjs.com/package/bullet-screen-engine)
[![MIT](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square)](https://github.com/iamscottxu/openBSE/blob/master/LICENSE)

[English Version](https://github.com/iamscottxu/openBSE/blob/master/README.en.md) |
[wiki](https://github.com/iamscottxu/openBSE/wiki) |
[Demo](https://iamscottxu.github.io/openBSE/demo/openBSEDemo.html) |
[2.0-Alpha Docs](https://iamscottxu.github.io/openBSE/docs/2.0-Beta/index.html)

高性能 JavaScript 弹幕引擎。同屏弹幕1000+

## 简介
一个高性能 JavaScript 弹幕引擎，简单易用。支持 CSS3 、 Canvas 2D 、 WebGL 和 SVG 渲染方式。支持顶部、底部、逆向弹幕渲染。使用 Canvas 2D 渲染方式可同屏渲染至少1000条弹幕（可达1600条，与电脑配置有关）。

## 安装和使用
### 安装
你可以直接点击[这里](https://github.com/iamscottxu/openBSE/releases/tag/v2.0)下载最新发行版本，也可以用以下命令安装NPM包。
```Bash
> npm install bullet-screen-engine
```

### 使用
安装完成后，在 Html 页面引入。

压缩版：
```Html
<script src="bulletScreenEngine.all.min.js"></script>
```
调试版：
```Html
<script src="bulletScreenEngine.all.js"></script>
```
添加一个 id 为 `BulletScreensDiv` 的固定大小的 div 标签用于显示弹幕，并插入以下 JavaScript 代码。
```JavaScript
var bulletScreenEngine = new BulletScreenEngine(document.getElementById('BulletScreensDiv'));
var _startTime = 5000;
for (var i = 0; i < 10000; i++) {
    bulletScreenEngine.addBulletScreen({
        text: "这是一个长长长长长长长长长长长长长长长长长长长长长长长长的测试(^_^)",
        color: 'white',
        startTime: _startTime
    });
    _startTime += parseInt(Math.random() * 300);
}
bulletScreenEngine.play();
```

用浏览器打开网页即可显示弹幕。

详细使用说明请查看 [wiki](https://github.com/iamscottxu/openBSE/wiki) 。

## 联系作者
如果有任何问题请写下 [issues](https://github.com/iamscottxu/openBSE/issues) 。<br/>
E-mail：[scottxu@scottxublog.com](mailto:scottxu@scottxublog.com)

## 版权声明
这个项目是一个开源项目，遵循 MIT 开源协议。要查看协议，请点击[这里](https://github.com/iamscottxu/openBSE/blob/master/LICENSE)。