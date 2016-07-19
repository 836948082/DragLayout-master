# DragLayoutExpand

DragLayout的拓展，增加了右侧功能选项，类似与qq，

主界面listview新增滑动删除选项，另增加粘性控件，

主界面长按头像可屏蔽菜单滑出时主界面缩放，再次长按可取消屏蔽

基于https://github.com/Qiang3570/DragLayout的拓展功能

![](https://github.com/Qiang3570/DragLayoutExpand/blob/master/sample.gif)

修复第一次滑动打开左、右菜单，缩放问题
onStartOpen 重写方法中先执行一遍adapter刷新(可解决)
            adapter.notifyDataSetChanged();

解决长按头像切换动画后右侧菜单不显示问题
dispathDragEvent 方法中增加逻辑判断(可解决)
            animBackView(1.0f);
