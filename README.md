# three.wx.js

[Three.js引擎最后Release](https://github.com/mrdoob/three.js/releases/latest)

[微信小游戏开发文档](https://mp.weixin.qq.com/debug/wxagame/dev/index.html)


来自QQ群 117844722 的群友 毒药的药 分享

将此行代码（各个Three.js的版本对应行数不同，所以无法提供具体行数，请善用文本搜索功能）
```javascript
var version = parseFloat( /^WebGL\ ([0-9])/.exec( gl.getParameter( gl.VERSION ) )[ 1 ] );
//改为
var version = 1.
//或
var version = parseFloat( /^(WebGL|OpenGL ES)\ ([0-9])/.exec( gl.getParameter( gl.VERSION ) )[ 1 ] );
```
将three.js出现多处的
```javascript
document.createElementNS('http://www.w3.org/1999/xhtml','canvas');
document.createElementNS('http://www.w3.org/1999/xhtml','img');
//替换为
document.createElement('canvas');
document.createElementNS('img');
```
即可在真机微信端预览。

实测Three.js的r88、r89可用。

提示：
请搭配 weapp-adapter 使用

**使用方法:**
```javascript
require('./path/weapp-adapter')
import * as THREE from './path/three.js'
```
