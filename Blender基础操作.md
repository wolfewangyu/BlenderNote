

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

锁平面，例如在x,y平面上移动，选中mesh， 按住键盘z，则只能在x，y轴向移动


中上部的三个菜单  
![xcVs5i](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/xcVs5i.png)


# 原点编辑Origin
在顶部Option菜单里面，有很多checkbox，里面有影响origin和位置，按住G可以移动
取消origin之后，物体本身的转动都是围绕新的origin旋转了
原点恢复：点击原点, 右键set origin,  选择set to 几何中心或质心


# snap 吸附
视图上部菜单有一个像磁铁一样的图标，有三种模式: vertex, edge, face
如果：A为固定的，参照吸附的mesh，B为需要移动的，吸附到A上的mesh。


# 变换坐标系
世界坐标系Global: 点选中上左的图标
局部坐标系Local：object, viewport display, Axes, yy
在坐标系下拉菜单连，zz,yy,xx,是全局跟当前坐标系之间的切换。
Gizmal view：万向，需要确定旋转轴和转向轴，并且在object, mode里面选择YXZ（在中间的是旋转轴，Z是转向轴），这部分细节比较多还是看一下原B站教程好一些


# Viewport Gizmo显示
变换工具选择的辅助线显示，在右上方弓箭图标，打开checkbox，显示小的局部坐标系  
Object Gizmos中，勾选Move, Rotatte, Scale, 点选mesh的时候，即可出现3个轴向的辅助线



修改单位，厘米
点击scene的小图标，里面的length可以选择单位

选择工具，框选
全选：a,aa取消全选


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
Evee渲染器调整, AO, screen, refraction(折射)打开，采样率Sample渲染和视图
object小图标：在需要记录的参数上光标按键盘i，即可记录当前帧的位置

焦观察：num 点.
单独显示： num  / 重新显示， / 比. 好用，.有的时候会有延迟
整个场景视图观察： HOME（这个大概只有大键盘才能用）