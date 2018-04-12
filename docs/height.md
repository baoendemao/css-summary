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

#### 元素在指定高度中垂直居中
* line-height
* display: table; vertical-align: middle;

```

<div style="display: table;">
    <div style="display: table-row;">
        <div style="display: table-cell; border: 1px solid #ccc; height: 100px; vertical-align: middle;">张三</div>
        <div style="display: table-cell; border: 1px solid #ccc; height: 100px; vertical-align: middle;">李四</div>
        <div style="display: table-cell; border: 1px solid #ccc; height: 100px; vertical-align: middle;">王五</div>
    </div>
</div>

```

* table布局: 自动垂直居中

```

<table>
    <tbody>
        <tr>
            <td class="text">张三</td> 
            <td class="text">李四</td> 
            <td class="text">王五</td> 
        </tr>
    </tbody>
</table>

.text {
    height: 100px;
    width: 100px;
    border: 1px solid #ccc;
}

```
 ![avatar](https://github.com/baoendemao/css-summary/blob/master/images/table-verticle.jpeg)
可见，在table标签中，可以自动垂直居中，但是水平居中要加上text-align: center




