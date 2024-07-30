Noise 是一切纹理的基础，就如同“差异”是一切信息的基础。不同的纹理无非就是不同的noise的变换
今天看了几个视频，自己操作了一下，有了一些小小的理解：Textures 的制作及一个工作流的搭建

# Noise 为核心的工作流

## 基础设定
这里有一个基础设定，在什么都没有的情况下，如果新建（add）一个material，是会有两个node:
一个是principle BSDF: 这里有一些roughness, metalic在没有材质的情况下就可以调整的一些物理特性
一个是material output: 这是这个材质最终输出的材质情况

![Pvux5Z](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/Pvux5Z.png)
## Noise + color ramp: 通过noise来影响渐变色的分布
颜色贴图Color map: noise (fab) - color ramp: noise对两个渐变的color分布的影响
Displacement： noise的color 直接控制output material的displacement
roughness(平滑度)：noise来控制不平滑的程度
Emission(自发光)：和colormap的逻辑一样，使用noise对颜色进行噪波扰动
原则上来说，可以通过noise控制principled BSDF的所有参数，制造扰动  

## 细节调整Map的分布
texture coordinate + Mapping(使用generated 和vector链接)
为了更加精确的调整，可以详细调整大小，位置，旋转了。  


关于blender中texture的node
Texture出来之后可以控制color map, roughness, displacement, 可以建立几个texture 分别控制（如noise ）,也可以作为fab, 输出给color ramp, 产生噪波

这种模式下，以noise作为fab 输入给color ramp, 相当于把两个渐变色做一个noise pattern的混合
![qdKaYC](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/qdKaYC.png)


可以单独做一个noise texture控制displacement, 产生凹凸，岩石效果
另一个控制color，产生波纹效果


![Miq5Qw](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/Miq5Qw.png)


控制emissions , mapping旋转图案角度

![K2jvRV](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/K2jvRV.png)


整体的工作流程效果

![Me1owr](https://para-1255470189.cos.ap-nanjing.myqcloud.com/uPic/Me1owr.png)


另外，nodes编辑模式下，节点很多，有以下总结可以有个大概的全貌：

## 常见节点介绍
以下是一些常见的Blender节点及其用途简要介绍：

1. **Noise Texture**：
   - **用途**：生成噪声纹理，用于创建随机性和自然纹理效果。
   - **参数**：Scale, Detail, Distortion等。

2. **Voronoi Texture**：
   - **用途**：生成Voronoi图案，用于创建蜂窝状或细胞状纹理效果。
   - **参数**：Scale, Randomness, Feature Output等。

3. **Musgrave Texture**：
   - **用途**：生成各种形式的噪声纹理，如多层噪声、Ridged多层噪声等。
   - **参数**：Scale, Detail, Dimension, Lacunarity等。

4. **Gradient Texture**：
   - **用途**：生成渐变纹理，用于创建颜色渐变或其他渐变效果。
   - **参数**：Type (Linear, Quadratic, Easing等)。

5. **Brick Texture**：
   - **用途**：生成砖块图案，用于创建墙壁、地板等效果。
   - **参数**：Color 1, Color 2, Mortar等。

上面提到的Voronoi Texture，后面也想深入分析一下，今天也看到了相关内容
