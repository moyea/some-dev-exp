# 在网页中多次使用svg
## 通过defs定义多个symbol
```html
<svg display="none" width="0" height="0" version="1.1" xmlns="http://www.w3.org/2000/svg"
xmlns:xlink="http://www.w3.org/xlink">
  <defs>
    <symbol id="my-sym" viewBox="0 0 100 100">
      <path d=""/>
    </symbol>
  </defs>
</svg>
```
## 通过use使用symbol
```html
<svg>
  <!-- xlink:href指向symbol的id -->
  <use xlink:href="#my-sym" />
</svg>
```
