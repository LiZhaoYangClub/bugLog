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
