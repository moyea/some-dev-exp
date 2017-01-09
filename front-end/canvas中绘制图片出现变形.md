##canvas中绘制图片出现变形
```html
<style>
	#canvas{
		width: 400px;
		height: 400px;
		margin: 10px;
		border: 1px solid #ccc;
	}
</style>

<canvas id="canvas"></canvas>

<script type="text/javascript">
	var ctx = document.getElementById('canvas').getContext('2d');
	ctx.beginPath();
	ctx.strokeStyle = "rgb(0,0,0)";
    ctx.arc(50,50,30,0,2*Math.PI,true);
    ctx.closePath();
    ctx.stroke();
</script>
```
在浏览器中显示的结果  
![image](https://github.com/muyea/some-dev-exp/blob/master/front-end/img-1001.png)  
可以看到本来应该绘制的圆形被拉伸，变成了一个椭圆
原因：canvas（默认大小：300px*150px）相当于一张
图片，css或style设置canvas的属性与设置img属性一样，不
会改变原来图像，只会对这张图片进行拉伸变化，换句话说，你
现在看到的圆是在默认大小上经过拉伸变换后的样子
##解决方式
* 通过设置canvas的width和height属性
```html
<canvas id="canvas" width="400px" height="400px"></canvas>
```
* 通过js设置canvas的width和height属性

```
<canvas id="canvas"></canvas>
<script>
	var canvas=docuemnt.getElementById('canvas');
	canvas.width=400;
	canvas.height=400;
</script>
```

##修改后的代码
```html
<canvas id="canvas" width="400px" height="400px"></canvas>

<script type="text/javascript">
	var ctx = document.getElementById('canvas').getContext('2d');
	ctx.beginPath();
	ctx.strokeStyle = "rgb(0,0,0)";
    ctx.arc(50,50,30,0,2*Math.PI,true);
    ctx.closePath();
    ctx.stroke();
</script>
```
显示结果
![image](https://github.com/muyea/some-dev-exp/blob/master/front-end/img-1002.png)

