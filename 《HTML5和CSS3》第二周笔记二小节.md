### 《HTML5和CSS3》第二周笔记二小节

#### 伪类选择器

**伪类选择器**是一种允许通过未包含在 HTML 元素的状态信息来定位 HTML 元素的用法。**伪类选择器**的具体用法就是向已有的选择器增加关键字，表示定位的 HTML 元素的状态信息。

代码示例：

```HTML
<!DOCTYPE html>       
<html lang="en">      
<head>                
    <meta charset="UTF-8">      
    <meta name="viewport" content="width=device-width, initial-scale=1.0">    
    <title>伪类选择器</title>
    <style>
        <!--
          伪类选择器：
          *概念：用来表示定位元素的某种状态所显示的样式
          *语法：：关键字，例如：hover
     -->
        button:hover{
            background-color:lightcoral;
        }
    </style>
</head>
<body> 
    <button>按钮</button>
</body>
</html>
```

#### 伪类选择器的分类

**伪类选择器**的数量很庞大，为了更好地梳理**伪类选择器**，我们可以按照用途的不同分为如下 5 种类型：

1. 动态伪类选择器：常与 <a> 元素配合使用，用来表示用户的某种行为状态。
2. 目标伪类选择器：常与 <a>元素配合使用，用来定位当前 HTML 页面中唯一一个目标元素。
3. 元素状态伪类选择器：常与表单组件元素配合使用，用来表示表单组件的某种状态。
4. 结构伪类选择器：常与  <table> 元素配合使用，利用 HTML 元素之间的关系定位目标元素。
5. 否定伪类选择器：用来定位与指定选择器不匹配的 HTML 元素。

#### 伪元素选择器

CSS 中**伪元素选择器**的用法与伪类选择器的用法类似，都是在指定 CSS 选择器增加关键字。但这两者的作用并不相同，伪类选择器是用来描述某个指定元素的状态信息，而伪元素选择器是用来描述某个指定元素的特定部分设定样式。

语法格式：

```

/* CSS3 语法 */
选择器::伪元素 {
  属性 : 属性值;
}
/* CSS2 过时语法 (仅用来支持 IE8) */
选择器:伪元素 {
  属性 : 属性值;
```

### CSS颜色

**颜色的概念：**

- 色调：很接近通俗意义上的颜色。
- 饱和度：是指颜色中灰色的含量。
- 亮度：是指颜色中黑色的含量。
- 对比度：前景色与背景色之间的差异。
- Web 安全色：不需要担心颜色在不同硬件环境、操作系统和浏览器之间的差异.

**前景色与背景色**

前景色

CSS 的 color 属性不仅仅表示前景色，更多地是用来表示 HTML 元素的文本内容颜色.

代码示例：

```HTML
p {
  color: lightcoral;
}
```

背景色

CSS 的 background-color 属性是用来设置 HTML 元素的背景色，该属性的默认值是 transparent（透明）。

代码示例：

```HTML
p {
  background-color: lightcoral;
}
```

**颜色值的类型**

在上述无论是 color 属性还是 background-color 属性都需要应用到颜色值，这个颜色是一种标准 RGB 色彩空间（sRGB color space）的颜色。

颜色值可以通过如下 3 种类型进行定义：

- 色彩关键字
- RGB 色彩模式
- HSL 色彩模式

**色彩关键字**

**色彩关键字**是一个不区分大小写的标识符，其表示一个具体的颜色，例如 red 表示红色、blue 表示蓝色等。而且从 CSS1 版本发展到 CSS3 版本，色彩关键字的数量变化也是比较大的：

- CSS1 版本时只有 16 个基本颜色，称为 HTML 基本颜色。
- CSS2 版本时增加了 orange 这种颜色。
- CSS3 版本时增加的颜色数量比较多，具体可以参考 [MDN 网站的色彩关键字文章](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color_value#色彩关键字)。 

注意：除了 16 个 HTML 基本颜色之外，其他任何颜色都需要通过特定的计算程序转换，最终导致不同浏览器呈现出的效果可能会不一致。

**transparent** 关键字表示一个完全透明的颜色，并且 transparent 是 background-color 属性的默认值。

**提示**：在 CSS2 版本中 transparent 并不是一个真实的颜色，到 CSS3 版本中重新定义为一个真实的颜色。

**RGB模式**

**RGB**是一个简称，全称为 **Red-Green-Blue**，即**红-绿-蓝**。RGB 色彩模式是工业界的一种颜色标准，是通过对红、绿、蓝三个颜色通道的变化以及它们相互之间的叠加来得到各式各样的颜色的。

在 CSS 中使用 RGB 色彩模式有如下 2 种方式：

1. 十六进制符号 `#RRGGBB` 和 `#RGB`

- `#RRGGBB`：是 `#` 符号后面编写 6 个十六进制字符（0-9，A-F）
- `#RGB`：是 `#` 符号后面编写 3 个十六进制字符（0-9，A_F）

​        说明：当 `#RRGGBB` 格式中的两个 R 或 G 或 B 值相同时，就可以改写为 `#RGB` 格式。例如 `#ff0033` 可以改写成 `#f03`。

​    2.函数符 `rgb(R, G, B)`

- 这里的 R、G、B 的值可以使用 0 ~ 255 之间的值
- 这里的 R、G、B 的值也可以使用 0% ~ 100% 之间的值

​         说明：`rgb(R,G,B)` 的 255 和 100% 是一致的，相当于十六进制符号中的 FF。

代码示例RGB模式的几种用法：

```HTML

#p1 {
  background-color: #FFCC33;
}
#p2 {
  background-color: #FC3;
}
#p3 {
  background-color: rgb(255, 204, 51);
}
```

**HSL模式**

**HSL**是一个简称，全称为 **Hue-Saturation-Lightness**，即 **色调-饱和度-亮度**。HSL 色彩模式是一种将 RGB 色彩模型中的点在圆柱坐标系中的表示法。

在 CSS 中使用 HSL 色彩模式是通过 `hsl(H, S, L)` 函数实现的，具体含义如下：

- **H** 表示色调，其值范围为 0 ~ 360 之间的一个角度。
- **S** 表示饱和度，其值范围为 0% ~ 100% 之间的百分值。
- **L** 表示亮度，其值使用百分值表示。0%表示黑色，50%表示标准色，100%表示白色。

代码示例HSL模式的几种用法：

```HTML
p {
  background-color: hsl(50, 33%, 25%);
}
```

**透明度**

在 CSS3 版本中新增了 opacity 属性用来设置 HTML 元素的透明度，该属性的值范围介于 0 ~ 1 之间。具体情况如下所示：

- 如果值为 0 或 0.0 则表示完全透明
- 如果值为 0.5 则表示半透明
- 如果值为 1 或 1.0 则表示不透明

 代码示例opacity属性的用法：

```HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>透明度</title>
  <style>
    div {
      background-color: lightcoral;
    }
    .light {
      opacity: 0.2;
    }
    .medium {
      opacity: 0.5;
    }
    .heavy {
      opacity: 0.9;
    }
  </style>
</head>
<body>
  <div class="light">这是一个测试内容.</div>
  <div class="medium">这又是一个测试内容.</div>
  <div class="heavy">这还是一个测试内容.</div>
</body>
</html>
```

CSS 中的透明度除了提供了 opacity 属性用法之外，还可以结合 RGB 模式和 HSL 模式共同使用。具体如下所示：

- RGB 模式增加了 `rgba(R,G,B,A)` 函数，其中 A 为 alpha 表示透明度。
- HSL 模式增加了 `hsl(H,S,L,A)` 函数，其中 A 为 alpha 表示透明度。

**颜色模式**

到这，我们会发现 CSS 除了色彩关键字来描述颜色之外，主要拥有 RGB 模式提供的 `rgb()` 函数和 HSL 模式提供的 `hsl()` 函数两种方式来描述颜色。如果再增加透明度之后，又增加了 `rgba()` 函数和 `hsla()` 函数两种方式。

属于 CSS2 版本的是 `rgb()` 函数，CSS3 新增加了 `rgba()`、`hsl()` 和 `hsla()` 函数。这样就形成了四种具体的颜色模式。

### CSS单位

**CSS的值**

CSS 中的值是一种定义允许子值集合的方法。例如我们现在可以使用色彩关键字、RGB 色彩模式或 HSL 色彩模式不同类型来描述颜色值。

在 CSS 中除了**颜色值**需要不同类型描述之外，比较常见的还有**长度值**也需要不同类型描述，例如 10px 或 50% 等。

CSS单位

在使用不同类型描述**长度值**时，需要附加**单位**。不同的单位表示的含义是不同的，例如 100 厘米等于 1 米。在 CSS 中具有 2 种不同类型的长度单位：

- 绝对长度单位
- 相对长度单位

像素值（px）

**像素**的英文为 Pixel，简写为 px。**像素**是指在由一个数字序列表示的图像中的一个最小单位。简单来说，如果我们把一张图片放大数倍，会发现这些连续色调其实是由许多色彩相近的小方点所组成，而这些小方点就是构成影像的最小单元就是**像素**。

目前几乎所有的数码设备都具有**分辨率**的概念，这里的分辨率更多是指**图像分辨率。**该图像分辨率指的是图像中存储的信息量，毕竟典型的是以每英寸的像素数（PPI，pixel per inch）来衡量。

这也很好地解释了为什么在一块屏幕中，分辨率的值越大，显示的字体反而越小。因为在屏幕尺寸固定不变的情况下，分辨率的值越大，每英寸的像素数（PPI）越大，单个像素所占的大小就越小。而一般屏幕显示的字体都是通过像素来设置的，例如 18px。

  **注意**：像素（px）是绝对单位，显示器的（PPI）一般都是由物理元件决定的。

**百分比（%）**

**百分比（%）**总是将某个值作为参考，设置为这个参考值的百分比，例如 40%。在 CSS 中一般情况下，百分比（%）多是将当前 HTML 元素的父级元素作为参考值。例如如果一个父级元素拥有两个子级元素，一个子级元素的宽度为 40%，另一个子级元素的宽度为 80%，那么第二个子级元素的宽度就是第一个子级元素的宽度的 2 倍。

代码示例：

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>百分比</title>
  <style>
    .parent {
      width: 200px;
      height: 100px;
      border: 1px solid lightcoral;
    }
    #child1 {
      width: 40%;
      height: 50px;
      background-color: limegreen;
    }
    #child2 {
      width: 80%;
      height: 50px;
      background-color: lightslategray;
    }
  </style>
</head>
<body>
  <div class="parent">
    <div id="child1"></div>
    <div id="child2"></div>
  </div>
</body>
</html>
```

​    **注意**：在 CSS 中并不是所有所有的属性值都可以使用百分比来描述，具体使用情况可以参考 [MDN 网站的 CSS 参考](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference)。

**em 与 rem**

em 与 rem 都是相对单位，目前更多应用于移动端设备，例如手机、平板电脑的显示。具体的含义如下所示：

- em：是相对于当前 HTML 元素的父级元素来进行设置。
- rem：是相对于当前 HTML 根元素<style>来进行设置。

上述 2 种单位都具有如下 3 种情况：

- 小于 1 时：表示相对于父级元素或根元素缩小。例如 0.5em 表示是父级元素的 0.5 倍，0.5rem 表示是根元素的 0.5 倍。
- 等于 1 时：表示与父级元素或根元素的大小保持一致。
- 大于 1 时：表示相对于父级元素或根元素放大。例如 1.5em 表示是父级元素的 1.5 倍，1.5rem 表示是根元素的 1.5 倍。

例如我们将 `` 元素的字体大小设置为 16px，然后编写两个列表，一个列表使用 em 单位，一个列表使用 rem 单位，具体示例代码如下所示：

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>em与rem</title>
  <style>
    html {
      font-size: 16px;
    }
    .ems li {
      font-size: 1.3em;
    }
    .rems li {
      font-size: 1.3rem;
    }
  </style>
</head>
<body>
  <ul class="ems">
    <li>One</li>
    <li>Two</li>
    <li>Three
      <ul>
        <li>Three A</li>
        <li>Three B
          <ul>
            <li>Three B 2</li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
  <ul class="rems">
    <li>One</li>
    <li>Two</li>
    <li>Three
      <ul>
        <li>Three A</li>
        <li>Three B
          <ul>
            <li>Three B 2</li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</body>
</html>
```

