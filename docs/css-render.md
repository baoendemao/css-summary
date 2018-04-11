#### 浏览器的主要组成部分
* 用户界面。包括：地址栏，前进和后退按钮，书签，菜单等部分。
* 浏览器引擎。用于操作渲染引擎的接口。
* 渲染引擎
* 网络
* UI后端
* JS解释器
* 数据存储

#### CSS解析引擎
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