#grid-template-areas说明
```css
.container{
  display: grid;
  grid-gap: 5px;
  grid-template-areas:
    "head"
    "aside-1"
    "sec"
    "aside-2"
    "foot";
}
.container>*{
  background-color: lightgreen;
}
header{
  grid-area: head;
}
aside:nth-of-type(1){
  grid-area: aside-1;
}
section{
  grid-area: sec;
}
aside:nth-of-type(2){
  grid-area: aside-2;
}
footer{
  grid-area: foot;
}
@media(min-width:700px){
  .container{
      grid-template-areas:
        "header header header"
        "aside-1 sec  aside-2"
        "foot    foot    foot";
   }
}
```
```html
<div class="container">
    <header>Header</header>
    <aside>aside-1</aside>
    <section>section</section>
    <aside>aside-2</aside>
    <footer>footer</footer>
</div>
```
##当小于700px时展示的效果
```
+-----------------------+
|       Header          |
+-----------------------+
+-----------------------+
|       aside-1         |
+-----------------------+
+-----------------------+
|       section         |
+-----------------------+
+-----------------------+
|       aside-2         |
+-----------------------+
+-----------------------+
|       Footer          |
+-----------------------+
```
### 当大于700px时
```
+---------------------------+
|           Header          |
+---------------------------+
+-------++---------++-------+
|aside-1|| section ||aside-2|
+-------++---------++-------+
+---------------------------+
|           Footer          |
+---------------------------+
```
