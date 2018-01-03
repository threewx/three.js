# three.wx.js
[Three项目网址](https://github.com/mrdoob/three.js/releases)

来自QQ群 117844722 的群友 毒药的药 分享

将此行代码（各个Three.js的版本对应行数可能不同，所以无法提供具体行数，请善用文本搜索功能）
```javascript
var version = parseFloat( /^WebGL\ ([0-9])/.exec( gl.getParameter( gl.VERSION ) )[ 1 ] );
```
改为
```javascript
var version = 1.
```
即可在真机微信端预览。

本人实测Three.js的r88、r89可用。


请搭配 weapp-adapter 使用

**使用方法:**
```javascript
require('./path/weapp-adapter')
import * as THREE from './path/three.js'
```
