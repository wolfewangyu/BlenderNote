# 资源
B站辣椒酱

shortcut
https://docs.google.com/document/d/1wZzJrEgNye2ZQqwe8oBh54AXwF5cYIe56EGFe2bb0QU/edit


人形模型，make human Community创造人物形象
网站：make human Community

Blender 贴video texture教程：UV edit
https://www.youtube.com/watch?v=E1COCnMUIhQ



# 其他
线框模式： shift + Z

# mesh的基础信息
N键，右侧出现菜单包括：Location, Rotation, Scale


# 移动
摇头：
鼠标中键+鼠标移动
点右上角圆球里面的小坐标系
小键盘numpad：
7，4 分别是正对z，4是-y。9是不管什么视角，都是取相反视角
5 正交视图 / perspective视图的切换

pan:平移
shift + cmd + 鼠标左键
锁轴移动
选中，x，x轴向移动，点击确定位置

位置归零：opt + G

输入数字移动（快速精准）
Gx 6 (x轴平移6) Gx-1(x轴负向移动1，基于上面的6，那现在坐标x师5)


中上部的三个菜单  
![xcVs5i](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/xcVs5i.png)



# 原点编辑Origin
在顶部Option菜单里面，有很多checkbox，里面有影响origin和位置，按住G可以移动


# snap 吸附
视图上部菜单有一个像磁铁一样的图标，有三种模式: vertex, edge, face
如果：A为固定的，参照吸附的mesh，B为需要移动的，吸附到A上的mesh。


# 变换坐标系
世界坐标系Global: 点选中上左的图标
局部坐标系Local
object, viewport display, Axes, yy
在坐标系下拉菜单连，zz,yy,xx,是全局跟当前坐标系之间的切换。

法向
万向：旋转轴x，转向轴z，MODE: YXZ(中间，最后)
线框模式shift+z
tab选中
, 菜单

移动远点,options, G



Shift + cmd/ alt + left
camera, num 0
ZHENGJIAO, 5
Camer move, N, view Lock ,  Camera to.. , 视频4:44
分辨率，比例修改，小打印机图标
相机to 观察者视角(取消Camera to 先)： cmd/ ctrl + opt/ alt + num0
四视图：
num7: 顶视图
Num5: 回到原位，正交和透视相机的切换
Num1: -y朝前
Num3: x 侧视图
Cmd/ ctrl + 数字，相反
Num 9 反转到另一面

聚焦观察：num 点.
单独显示： num  / 重新显示， / 比. 好用，.有的时候会有延迟
整个场景视图观察： HOME

变换工具选择的辅助线显示，在右上方弓箭图标，打开checkbox，显示小的局部坐标系
移动快捷键归零 alt/option + G
锁轴向：G, 按x, y, z
快速输入数值移动， Gx 5, 直接x轴移动5， 相对数值，可以加减，在当前位置比如已经是2,0,0, 希望移动到-3，0，0就输入Gx -5即可

锁平面移动，找垂直轴，如：xy轴移动，要g, shift+Z
归零：alt/opt + G, alt/opt + R/RR


修改单位，厘米
点击scene的小图标，里面的length可以选择单位

选择工具，框选
全选：a,aa取消全选


基础知识动画
Evee渲染器调整, AO, screen, refraction(折射)打开，采样率Sample渲染和视图
object小图标：在需要记录的参数上光标按键盘i，即可记录当前帧的位置



