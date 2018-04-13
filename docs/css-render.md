#### 浏览器的主要组成
* 用户界面: 地址栏，前进和后退按钮，书签，菜单等部分
* 浏览器引擎: 操作渲染引擎的接口
* 渲染引擎: 解析html和css，呈现解析后的内容
* 网络：http请求
* UI后端：绘制基本的构件，如下拉框和窗口
* JS解释器
* 数据存储

#### 渲染引擎
* 了解渲染引擎
先看一段代码：

```

<div class="container">
    <div class="detail">
        <span class="text">hello world</span>
    </div>
</div>

.container .detail .text {
    font-size: 20px;
}

```

浏览器处理CSS结构“.container .detail .text”，是按照从右往左的顺序的，
即首先处理.text，然后再找到.detail，最后是.container。
可以将该结构看作是一棵树, 从子节点到父节点有唯一的一条路径，
而如果从父节点找到子节点，需要遍历父节点的所有孩子节点来查找，则比较耗时。
这就是渲染引擎要做的事情。

