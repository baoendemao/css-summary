* 哪些元素具有层叠上下文？
    * 定位元素 + z-index。z-index只有和定位一起，z-index设置的值才有效。
    * 根元素
    * 其他
* z轴的层叠水平，从上往下，层叠水平依次增加
    * background和border
    * z-index < 0
    * block元素
    * float元素
    * inline和inline-block
    * z-index: auto 和 z-index: 0
    * z-index > 0
* z-index的取值

* 并列关系的z-index
    * 只关心并列的z-index，不关系其子元素的z-index
* 