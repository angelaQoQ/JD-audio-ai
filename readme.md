# 使用JD-AI接口,网页端文字转语音.

## 1 功能实现: 
* 文字转语音
* 语速速度控制 .5-2.0倍
* 音色控制	  磁性男,自然女,老萌妹

## 2 技术支持: 
```js
vue.min.js		日后要嵌套到客户端的webview中,反正之前JQ,zp用着也一样
axios.min.js	这个随意选择,axios也提供了类似abort()的函数只要能终止请求,随意随意
md5.js  		语音接口需要将用户秘钥和时间戳进行MD5加密
```

## 3 纯前端配置项:
```html
推荐vscode编辑器,及插件live-server的代理服务器,可以纯前端开发
配置项:(设置-settings.json)中添加:

"liveServer.settings.proxy": {
        "enable": true, 
        // JD语音接口
        "baseUri": "/JD", //from where you want to proxy. 
        "proxyUri": "https://aiapi.jd.com/jdai/tts" // JD audio地址_vip
    },

```

## 4 自己看吧,附[京东AI地址](https://aidoc.jd.com/speech/tts_vip.html)
