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

可见broder-left此时和border-bottom连接的地方变成了一个斜线, 这样可以很容易将border-left变成一个梯形的形状，只需加上border-top: 20px solid transparent, 效果如下图所示：

![avatar](https://github.com/baoendemao/css-summary/blob/master/images/tixing.png)

