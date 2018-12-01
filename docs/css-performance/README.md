## CSS性能优化

### base64格式制作小图 => 网上很多转换base64的工具
* 可以减少一次请求
```
    // 注释解释这个图片是什么 => 为了方便维护
    background: url(data:image/png;base64,xxxxxxxxxx);
```
* base64图片是未经压缩的，所以比原图的体积更大，适合小图。如果大图使用base64的话，会导致加载很慢。

### 减少重绘repaint，回流reflow

* 回流和重绘的区别：
    * 重绘（重新绘制）：当render tree的一些元素需要重新更新属性，而这些属性只是影响元素的外观、风格，而不会影响布局，比如background-color
    * 回流：
        * 当render tree中的元素因为元素的规模尺寸，布局，隐藏等改变而需要重新构建，会引发回流
        * 一些属性的读取也会引起回流，比如读取某个 DOM 的高度和宽度，或者使用getComputedStyle方法。
        * 相比重绘来说，回流的性能开销更大。

* 如何减少重绘和回流
    * 多次对dom的改变，整合成只操作一次dom
    * 避免使用触发重绘、回流的CSS属性
        * 触发重绘的属性
        ```
        color, border-style, border-radius, visibility,   text-decoration, background, 
        box-shadow,outline-color, outline-style, outline-width
        ```

        * 触发回流的属性
        ```
         width, height, min-height, line-height, padding,margin, top, bottom, left, right, position,float, text-align, overflow-y, font-weight, overflow, font-family,    vertical-align, white-space, font-size
        ```

    * 将重绘、回流的影响范围限制在单独的图层之内，来新建图层，从而不影响其他图层上的元素，降低整个页面重绘和回流带来的性能消耗
        * 新建图层的缺点：合并图层需要时间的消耗
        * chrome怎么查看图层 ？
            * 右键检查 => More tools => Layers

        * 如何新建图层？
            * video新建图层
                * video视频频繁进行重绘和回流的标签，浏览器有这个机制新建图层
            * transform: translateZ(0);  因为它会启动GPU的3D加速。
            * canvas标签
            * flash

    * 用translate替代top改变
        * 因为top会触发回流，而translate不会回流，translate只会重绘
    * 用opacity替换visibility
        * 因为visibility会触发重绘，而opacity不会





