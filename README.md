# bugLog
bug...log


#### vue3.0 install bug with "can not find module 'vue-loader-v16/package.json'"
```js
  npm version >= 6.9
```

#### 在Edge浏览器中，频繁点击elementUI的选择器会导致页面刷新
```html
<el-select @visble-change="visibleChange"></el-select>
```
```js
visibleChange(isVisible){
  const isEdge = window.navigator.userAgent.includes('Edge');
  if(isEdge && !isVisible) {
     document
       .querySelectorAll('body> .el-select-dropdown.el-popper')
       .forEach(it => it.remove());
  }
}
```

#### iframe src=*.PDF 时， el-dialog弹窗的层级在iframe 之下的问题
```html
  <iframe v-show="dialogVisible" id='iframebar' src="about:blank" frameBorder=0  marginHeight=0 marginWidth=0
      style="position:absolute;visibility:inherit; top:0px;left:0px;height:100%;width:100%;z-index:2;background:rgba(255, 255, 255,
             .2);filter='progid:DXImageTransform.Microsoft.Alpha(style=0,opacity=0)'">
  </iframe>
```
