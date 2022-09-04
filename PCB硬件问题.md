# PCB硬件

## 多层PCB

### 多通道ROOM复制

1. Design-create sheet symbol from sheet

![image-20220818160958856](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/image-20220818160958856.png)

![image-20220818161027740](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/image-20220818161027740.png)

2. 按要求连线，建立多个相同的通道

![image-20220818161121231](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/image-20220818161121231.png)

3. 更新PCB，在一个ROOM中布好线，Design——Room——copy Room

![image-20220818161356410](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/image-20220818161356410.png)

![image-20220818161509390](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/image-20220818161509390.png)

### 含BCA器件PCB绘制

####fanout扇出

[参考博客](https://blog.csdn.net/weixin_42204303/article/details/112731449)

1. 点击执行菜单命令Route-Create Fanout，进行扇出

2. 还需要对参数进行设置，如图5-124所示，在Options面板中进行选择

![img](F:/%E7%AC%94%E8%AE%B0.md/PCB%E7%A1%AC%E4%BB%B6%E9%97%AE%E9%A2%98/pic/o4YBAF-GYbWAG17OAABaxwvzn_Y436.png)

- Include Unassigned Pins：含义是扇出的时候，将没有网络的管脚也进行扇出，一般不用勾选，空网络的管脚不用进行扇出；
- Include All Same Net Pins：含义是当单独对某一个管脚进行扇出时，将跟这个管脚网络一致的管脚也进行扇出，一般不用勾选；
- Via：选择扇出所需要用到的过孔，过孔首先需要在物理规则里面添加好，不然这里没有可以选择的过孔；
- Via Direction：过孔的方向朝向，一般选择BGA类型的风格，给BGA器件留出十字通道，方便散热；
- Pin-Via Space：过孔到焊盘的间距，一般选择中心间距，将过孔扇出在周围四个焊盘的中心处。

3. 将上述参数社会好以后，在Find面板中选择Symbols，用鼠标左键去点击需要进行扇孔的BGA器件即可，完成对BGA器件的扇出.
