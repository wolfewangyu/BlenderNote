Blender Colab渲染

# 概述
这两天有一些Blender的动画需要动画需然，主要是材质里面有视频，要体现完整播放的视频，M1的Macbook pro实在不行了，就招来了云渲染方案。使用的是google的colab, 使用jupiter。最早之前我用它跑过stable diffusion的web ui, 这回用它来渲染。

GitHub上找来资源，youtube 有教程，但是代码略有不同，使用的时候根据我自己的具体情况做调整。尤其是blender的版本这块。

原github地址如下，我也fork了一下，readme文件里面有youtube链接的教程
https://github.com/drmichaeldouglass/blenderGoogleGPU  


# 步骤

1. 新建一个colab笔记本，这里我从GitHub上直接下载（就是github上的BlenderColab.ipynb），然后“上传笔记本”  
2. 挂载Google drive
3. BLENDER下载，拷贝，解压缩到drive。（这一步如果google drive里面已经存好了，以后就不需要跑这一步了）
这里要注意：不要用太新的版本，起初我用的和Mac上一样的3.6, 总是报错找不到某个库，stackflow 上面也有很多人有这个问题。改到了3.3就可以了。（原链接的作者使用的是3.0版本）
4. 设置文件位置，注意上传blender待渲染文件要带着素材（材质等）一起传上去。我遇到了报错和不报错的情况。不报错更可怕。
5. 渲染，注意，如果渲染动画，一定在动画中间挑两帧渲出试试，看看画面运动是否对的上。然后再渲染动画（也是图片序列）
对于动画的设置，在上传之前先在blender里面设置好。  

(下面两条属于本地的blender设置，可能影响渲染的)
6. 在blender里面的Timeline视图：start, end frame要设置好设置关键帧，白模先走一遍动态看看时间点卡的对不对，这里一定要注意：比如我现在的视图和各个设置已经是Camera 2的情况，但是一渲染还是Camera 1。所以一定要测试好！（这个情况就到outline视图的Camera 2，点开绿色的图标，右键“set local”）  
   
7. 对于一些单独模型，不想让他自己运动的单独调整，可以在面板里面unlink 或者删除运动
上传文件
渲染等图：输出文件夹的设置注意，这只完了它并不放在文件夹内而是放在文件夹的上一级目录（出图和指定输出渲染的文件夹在同一层级），所以如果想放到output文件夹就要在output里面再创建一个文件夹（比如叫placeholder），然后o的部分选择place holder。

8. 浏览器不能关，除非colab pro+ （注意是colab pro+, 不是colab pro）
9. 关于上面这一点，有解决办法我还没有尝试，第一个是单租虚拟机来控制，第二个是本地安装jupiter notebook

上面一点，第一种方法，可以直接关电脑了，但是需要单独付一个虚拟机的费用，不一定是google的，第二个方法还是要开电脑，好像是不需要开浏览器了。

