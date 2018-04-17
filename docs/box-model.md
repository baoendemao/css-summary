#### border

* 例如： 只设置border-left

```
<div style="
    width: 200px;
    height: 200px; 
    border-left: 20px solid lightskyblue">
</div>
```

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/border-left-only.png)
<br/>
可见border-left是长方形的，高度是内容区的height， 宽度是border-left设置的值

* 例如：只设置border-left和border-bottom, 而border-bottom-color: transparent

```
<div style="
    width: 200px;
    height: 200px;
    border-left: 20px solid lightskyblue;
    border-bottom: 20px solid lightskyblue;
    border-bottom-color: transparent;
"></div>

```

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/border-left-bottom.png)
<br/>

可见broder-left此时和border-bottom连接的地方变成了一个斜线, 这样可以很容易将border-left变成一个梯形的形状，只需加上border-top: 20px solid transparent, 效果如下图所示：
<br/>

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/tixing.png)

#### padding
* 注意: padding的百分比是根据父元素的宽度，不是高度。包括了padding-top, padding-right, padding-bottom, padding-left。

#### margin
* 注意：margin的百分比是根据父元素的宽度，不是高度。包括了margin-top, margin-right, margin-bottom, margin-left。

#### box-shadow
* 使用box-shadow画出两个一模一样的图形 
<br/>

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/box-shadow-copy.png)
<br/>

```
.button {
    height: 45px;
    width: 476px;
    background: #ffbfc9;
    box-shadow: 0 100px 0 0 #ffbfc9, 0 200px 0 0 #ffbfc9;
}
```

box-shadow的参数依次是：x轴的偏移，y轴的偏移，模糊距离，阴影尺寸，阴影颜色

* 使用box-shadow画出来边框
<br/>

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/box-shadow-border.png)
<br/>

```
.box {
    box-shadow: 0 0 0px 7px #ffbfc9;
}
```

#### border-radius
* 使用border-radius画半圆

```
width: 200px;
height: 100px;
border: 1px solid blue;
border-radius: 100px 100px 0 0;

```
<br/>

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/half-circle.jpeg)
<br/>

* 使用border-radius画扇形

```
width: 100px;
height: 100px;
border: 1px solid blue;
border-radius: 100px 0 0 0;
```

<br/>

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/fourth-circle.jpeg)
<br/>
