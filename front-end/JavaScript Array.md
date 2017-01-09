#JavaScript数组相关操作

```javascript
var arr=[0,1,2,3,4,5,6];
//尾部插入
arr.push(7);//arr.length，返回数组当前长度
console.log(arr);//[0,1,2,3,4,5,6,7]
arr.push(8);//arr.length
console.log(arr);//[0,1,2,3,4,5,6,7,8]

//头部插入
arr.unshift(-1);//arr.length
console.log(arr);//[-1,0,1,2,3,4,5,6,7,8]
arr.unshift(-2);//
console.log(arr);//[-2,-1,0,1,2,3,4,5,6,7,8]
//数组合并，注意:将会生成一个新的数组，原数组不变
var anotherArr=arr.concat([9,10]);
console.log(arr);//[-2,-1,0,1,2,3,4,5,6,7,8]
console.log(anotherArr);//[-2,-1,0,1,2,3,4,5,6,7,8,9,10]
//在原数组上合并(其实是将合并后的数组赋值给原数组)
arr=arr.concat([9,10]);
console.log(arr);//[-2,-1,0,1,2,3,4,5,6,7,8,9,10]
//头部删除
arr.shift()//-2,删除的元素
console.log(arr);//[-1,0,1,2,3,4,5,6,7,8,9,10]
arr.shift();//-1
console.log(arr);//[0,1,2,3,4,5,6,7,8,9,10]
//尾部删除
arr.pop();//10,删除的元素
console.log(arr);//[-1,0,1,2,3,4,5,6,7,8,9]
arr.pop();//9
console.log(arr);//[-1,0,1,2,3,4,5,6,7,8]

//指定位置删除,
//index 删除起始位置，<0 从末尾开始向前数几位，>=0从头部开始数
//count 删除元素的个数 <=0不删除元素，>0则删除该
//数值个数的元素,若该值大于数组的长度，则删除该值+1到数组长度的元素
//insertEle... 插入的元素,可以有多个insertEle，多
//个insertEle均会在指定的位置插入
//splice(index,count,insertEle...);

/**
  * 删除数组中指定位置的元素，并返回删除的元素
  * @param arr {Array} 待删除的数组
  * @param index {Number} 删除元素的位置,小于零表示从末尾开始数
 **/
function delSpecialIndexEle(arrayObj,index){
  return arrayObj.splice(index,0)[0];
}

/**
  * 删除数组中指定位置的元素，并返回删除的元素
  * @param arr {Array} 待插入的数组
  * @param index {Number} 插入元素的位置,小于零表示从末尾开始数
  *                       若该值大于数组的长度，该方法同Array.push()
  *						  若该值小于0，且该值的绝对值大于数组的长度，该方法的作用同Array.unshift()
  * @param ele {Obj} 待插入的元素
 **/
function insertEleInSpecialIndex(arrayObj,index,ele){
  arrayObj.splice(index,0,ele);
}
```
