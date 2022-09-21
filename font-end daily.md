####2022.9.21

* 左右居中
```
marigin:auto
```
* 让一个元素快速居中在页面上
定义类的css
```
<style>
body{
        .eg{
                margin:auto;
        }
        display: flex;
}
</style>
<body>
        <div class="eg">
                <h1/>快速居中
        </div>
</body>
```
* padding 和 margin有什么区别
padding作用于自身，指自身边框到内部另一个容器边框之间的距离，容器内边距
margin作用于外部，指自身边框到另一个容器边框之间的距离，容器外边距  
* vw与百分比的区别
vw不管父级元素，只与屏幕的分辨率有关系
百分比有继承关系

* 行内元素与块级元素的区别
span行内元素：宽度设置不管用，宽高由内容决定
div块级元素：宽高有继承关系，且独占一行

* 如何让谷歌支持小字体
```
.eg{
        transform: scale(0.8)//变到原来的0.8倍
}
```

* let 和 var (不要用var，容易污染变量)
  * 声明提升（先上车后补票）
  ```
  console.log(name);//会输出test
  var name = "test";
  ```
  * 没有局部作用域（红杏出墙）
  ```
  function f(){
          for(var i = 0; i<4 ; i++)
          {}
          console.log(i);//输出5
  }
  f()
  ```
  * 声明覆盖（套牌车）
  ```
  var name = "test1";
  var name = "test2";
  console.log(name);\\会输出test2
  ```

* 深浅拷贝（深不影响）
  1. 基本数据类型，属于赋值，深拷贝
  ```
  let a = 1;
  let b = 2;
  console.log(a,b);//输出1，2
  ```
  2. 引用数据类型（对象，数组），属于浅拷贝

