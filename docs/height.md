本节介绍元素在页面中的高度相关的内容。

---

#### height
如果不定义高度，height是由内容撑起的。

#### line-height
line-height指的是两个元素基线之间的距离

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/line-height-baseline.jpeg)

从上图可以看出，基线并不在文字的中间位置，中文和底线之间还有一段距离。
line-height会撑起外边容器的高度。

* 例子： 父级的高度被撑起

```

<div class="container">
    <span class="text" style="line-height: 100px;">hello world</span>
</div>

```
![avatar](https://github.com/baoendemao/css-summary/blob/master/images/span-line-height.png)

可见虽然父级div盒子没有定义高度，但将line-height作用于inline元素，父级的盒子的高度撑高了到了子元素line-height的值。

* 例如：子元素垂直居中

```
<div class="container" style="height: 100px; line-height: 100px;">
    <span class="text">hello world</span>
</div>
```
![avatar](https://github.com/baoendemao/css-summary/blob/master/images/span-line-height.png)

可见父级的line-height也是作用于子inline元素的，使得子元素垂直居中


#### verticle-align
默认值：baseline。还可以取值: bottom, middle, top 等等。
其中top, middle, baseline, bottom分别指的是line-height部分中的图片里的顶线，中线，基线，底线。

#### 怎么让元素垂直居中
* 通过line-height


