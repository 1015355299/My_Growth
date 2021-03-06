# HTML基础

## 说明与注意

- 双边、单边标签（单边一般有特殊功能）
- 标签属性与标签要有空格,有些标签没属性
- 标签名建议小写
- 标签之间顺序嵌套

### 属性

### body 属性

- background 背景--默认垂直水平方向平铺
- backgroundcolor 背景色

## 标签功能

1. b 给文本设置加粗属性
2. strong 表示重要文本
3. mark表示突出、标注文本
4. address定义文档作者的联系信息
5. area定义图像映射内部区域
6. article定义文章
7. aside页面内容之外的内容
8. audio定义声音
9. canvas定义图形
10. caption定义表格标题
11. datalist定义下拉列表
12. dd定义定义列表中项目的描述
13. del删除线
14. details定义元素细节
15. dl定义定义列表
16. dt定义定义列表的项目
17. em强调文本，显示为斜体
18. select定义下拉列表
19. section定义段
20. option定义选择项
21. fieldset用来分组
22. legend用来分组描述，为fieldset元素定义标题（caption）
23. table定义表格
24. th定义表格头单元格
25. title定义文档标题
26. tr定义表格行
27. video定义视频
28. td定义表格单元格
29. base定义页面所有链接的默认地址
30. i 给文本设置斜体
31. u 给文本设置下划线
32. s 给文本设置删除线
33. sup 上标`y<sub>2</sub>=>y^2`
34. sub 下标同理
35. font 给文本设置 size 大小、color 颜色、face 字体设置
36. `<br />`换行
37. p 段落标签--align 控制内容水平对齐--left 居左对齐默认--center 居中对齐--right 居右对齐
38. `<hr />`水平线--color 水平线颜色--with 设置宽度（固定和%值）%比一定有参照物（当前 hr 的父元素）--size 设置粗细--noshade（值为自己）除去阴影
39. **pre 格式换行--空格和换行会保留**
40. font 强调文本标签
41. **label 标签有个 for 属性，与 for 属性值对应的标签 id 值一致的标签点击 label 会链接到有 id 的标签**
42. div 块级元素无实际意义--主要通过 css 修饰
43. span 行内标签无实际意义--主要通过 css 修饰
44. 块级元素独占一行，不能与其他元素并列，能接收宽高，如果不设置默认为父亲的 100%
45. 行内元素与其他行内元素并排，不能设置宽高。默认的宽度就是文字宽度

- 块级元素：p、h1-h6(标题) 排版标签一般都是块级元素
- 行内元素：b、i、u、font、sup、sub 文本标签一般为行内元素
- 字符实体：空格`&nbsp;` 大于>`&gt;` 小于<`&it;` 与&`&amp;` 人民币￥`&yen;` 版权`&copy;` 注册`&reg;` 乘x`&times;` 除÷`&divide;`

### 图片标签

- jpg(jpeg)、png、gif、bmp
- 不能使用的 psd、ai
- img=>image 图片 单边标签

1. src=>source 图片资源
2. **alt 属性 alternate 替代无图片时的文字**
3. **title 当鼠标放在图片上面时，显示的文字**
4. width 图片宽度
5. height 图片高度
6. 最好不要同时给图片设置高度和宽度，否则会拉伸图片

#### 文件位置

- 文件在磁盘上的位置
- 相对路径：相当于当前位置的某个文件位置，平级关系：目标文件与当前文件同目录用`./`,上层目录:`../`
- 绝对路径：一个文件在磁盘上的真实位置，windows 上带盘符

#### 超级链接

- 网站通过超链接跳转，形成网
- a（anchor 锚）标签 href（hypertext reference **超级链接地址**）属性内容为链接地址
- a 标签 title 鼠标移上时显示的文字信息
- **a 的 target 属性目标链接打开方式**：
  - `_blank`在新窗口打开目标文件
  - `_parent`在父框架集中打开被链接文档。
  - `_self`	默认。在相同的框架中打开被链接文档。
  - `_top`在整个窗口中打开被链接文档。
  - `framename`在指定的框架中打开被链接文档
- href 内容为 javascript:void(0);空链接 不跳转
- a标签不能嵌套a, h不能直接套h标签, p标签是不可以套块标签的

##### 锚点链接

- 定义锚点
  **`<a name="锚点名"></a>`**
  `<a id="锚点名"></a>`
- 找到锚点
  **`在浏览器网址最后加入#锚点名、或<a href="#锚点名">内容</a>`**

#### 列表标签

##### 无序列表

- 没有先后顺序
- ul（unordered list）无序列表 前面默认小圆点
- li（list item）列表项
- type 表示前面符号类型取值
  - disc 默认实心圆点
  - circle 空心圆
  - square 实心小方块

##### 有序列表

- 有先后顺序
- ol（ordered list） 有序列表 1.、2.、3.、、、
- type 设置列表前面序号 默认数字1、2...，可取a、A、i（小罗马）、I（大罗马数字）
- **start** 属性内容开始序号
- 少用

#### 定义列表

- dl（defintion list）定义列表
- dt（defintion title）定义标题
- dd（defintion description）定义描述
  
  > 注意：dt 与 dd 只能出现在 dl 里

#### 表格标签

- table 表示表格开始结束
- tr 表示表格行
- td 表示表格单元格、一行有多少个单元格
- **只有 td 标签才能存放内容**
- th 表格标题单元格，内容会加粗、居中显示

##### table 常用属性

- border 给表格设置边框 默认 0，单位像素可不写
- width 表格宽度，固定值和%
- height 高度，一般不用，由内容决定
- background 背景图片
- backgroundcolor 背景颜色
- align 表格水平方向对齐方式 left 默认、right、center
- **cellpadding** 单元格内容到边框距离，内填充
- **cellspacing** 单元格与单元格距离

##### tr 属性

- align 水平对齐方式 left、center、right
- valign 设置行里内容垂直对齐方式，top 顶部对齐、middle 居中对齐（默认）、bottom 底部对齐
- backgroundcolor 背景色
- height 行高
- width 单元格宽度
- **rowspan** 跨行合并，表示相当于几个格，合并后要删除 n-1 个格子
- **colspan** 跨列合并，表示相当于几个格，合并后要删除 n-1 个格子

#### 注释

- `<!--注释内容-->`

## 框架网页

### 什么是框架网页

- 把一个网页划分为若干个小窗口，每个窗口都可以存放一个独立网页
- 框架网页多用于后台系统

#### 框架网页基本使用

- 框架网页由框架集和框架页组成
- frameset 框架集
- frame 框架页、小窗口、单边标签
- **使用框架页面 frameset 时它就可以替代 body 功能**

```html 框架
<frameset>
  <frame/>
  <frame/>
</frameset>
```

##### frameset 属性

- rows：将一个网页分割为上下型
  - `rows="180"`上窗口占 180px
  - `rows="180,100,*"`上窗口占 180px,中窗口 100px，其他给下
- cols：将一个网页分割为左右型,同上设置
- **只有框架集才能分割**

##### frame 属性

- src 小窗口显示网页的地址
- name 小窗口名称,用于跳转显示，**a 标签的 target 跳转显示内容**
- noresize 不能调整小窗口大小
- frameborder 是否显示框架周围边框线，0 默认不显示，1 显示

#### 浮动框架

- iframe 这一对可放在 body 里面
- src 放入页面地址
- width 浮动框架宽度
- height 浮动框架高度
- name 浮动框架名称
- **用 a 标签的 target 属性跳转到 name 对应的网页**

## 表单

- 用于收集用户输入

### 表单基本使用

- form 标签和表单控件组成一个表单

#### form 属性

- **action** 将表单中收集的用户数据提交给表单处理程序（地址），**这个属性可以不写，如果不写（#）则将表单数据提交给当前页面处理**
- method 表单数据提交方式

  - get 默认值，以 get 提交的数据会显示在地址栏中，地址栏显示=>`表单处理程序?name1=数据1&name2=数据2` 以此类推
  - post 方式，不会显示在地址栏中，直接发送给处理程序
  - 优缺点：get 方式不安全，get 只能提交少了数据；post 相对安全，可提交大量数据

#### 表单控件标签

##### input 行内元素

- name 提交数据名称
- value 提交数据的值
- type 表单类型
  - type="text"单行文本框
  - type="password"单行密码框
  - **type="radio"单选按钮**，同 name 只能选一个，相互排斥，checked 属性表示选中，值为本身或不写
  - **type="checkbox"多选按钮**，name 属性要一样,checked 选择
  - type="submit" 提交按钮
  - **type="reset" 重置按钮**
  - **type="image"** 图片按钮，src 图片地址，具有表单提交功能，**会提交点击时的坐标属性**
  - type="file" 文件上传，name提交文件名
  - type="button" 普通按钮没什么重要功能，配合 js 使用
  - **type="hidden"** **隐藏域**里面的表单控件在浏览器看不见 但是也能提交数据处理，php 常用
- button 标签实现提交

  - `<button type="submit">提交</button>`
  - `<button type="reset">提交</button>`

##### 标签中通用属性

- title 鼠标移上显示文字信息
- class 类名，同类名属性同类，多用与 css 设置样式
- id 属性必须唯一 一般多用于 js 中
- style 样式属性，多设置 css 样式

##### 下拉列表

- **select 列表**
- **option 选项**，属性 select 选中项

```html 下拉列表
<select name="名称">
  <option value="值" select="select"></option>
  <option ></option>
  <option ></option>
</select>
```

##### 文本域

- textarea 显示文本内容

## 计算机单位与进制

### 单位

- 1bit（比特）2 种状态
- 1byte（字节）= 8bit 256 种状态
- 1kb = 1024 字节
- MB
- GM
- T 同上换算

### 进制

- 二进制 0、1
- 八进制 0-7
- 十进制 0-9
- 十六进制 0-15（0-9，A-F）

#### 进制转换

- 其他转十进制，按权展开
- 十转二，除 2 取余后倒排

### 字符编码

- 计算机只能识别二进制
- ASCII, 编码，美国标准信息交换码，使用 1 字节存储字符 256 个字符
- GB2312, 中国标准化局 1980 制度，2 字节存储字符共可存储 65536 个字符，只存了 6000 多汉字
- GBK, 2 字节存储，共存储 2w 多汉字
- **Unicode, 全世界编码集合，万国码**，100+w 字符，每个字符 4 个字节表示可表示 42 亿，比较浪费资源
- UTF-8, 编码对 Unicode 改进，**不同字符占用不同字节**，最大4字节,以8位为一个编码单位的可变长编码,英文使用8位（即一个字节），中文使用24位（三个字节）来编码

### head 标签

- title 标签主要用于网页设置标题，**浏览器最上方窗口显示文字信息**
- `<meta charset="utf-8">`使用 utf-8 编码，用于**告诉浏览器用什么编码来解析**，使之不出现乱码，浏览器中文默认使用 gbk 解析
- 记事本默认使用 gbk 编码
- 代码编写环境和解析环境一致

### font 标签

- color 属性设置文本颜色
- 英文颜色：red、blue
- 十进制：rgb（255，255，255）
- 十六进制：#ffffff
- rgb 红绿蓝三基色
- **每个基色使用 1 个字节表示**
- 共可表示 `256*256*256=1677w` 种颜色
- 最好使用十六进制表示颜色，**兼容性最好**

## HTML5

- W3C 万维网联盟
- WHATWG 是 web 超文本技术工作组
- XHTML 中有 DTD 为文档类型定义
- HTML5=HTML+CSS+Javascript
- HTML5 移动发展非常多

> HTML5 文档定义

```html 基本框架
<!--文档定义-->
<!DOCTYPE html>
<!--中文来解析语言-->
<html lang="zh-CN">
<!--英文来解析语言-->
<!--<html lang="en">-->
<head>
    <!--utf-8编码来解析-->
    <meta charset="utf-8">
    <!-- 网页标题 -->
    <title>Document</title>
</head>
<body>

</body>
</html>
```

## HTML5 新增标签

- 同 div，span 标签
- 有语义化标签实现盒子
  - header 页头标签
  - nav 导航标签
  - aside 侧边栏标签
  - footer 页脚标签
  - section 栏目标签

### 表单控件新增属性

- required 属性值为本身，作用为，此表单控件一定要有内容，需填写内容才能提交
- **placeholder** 属性内容为：显示提示内容
- **autofocus** 值为本身，自动获取焦点
- 新增 type 属性
  - color：用于指定颜色的控件。
  - date：用于输入日期的控件（年，月，日，不包括时间）。
  - month：用于输入年月的控件，不带时区。
  - week：用于输入一个由星期-年组成的日期，日期不包括时区
  - time：用于输入不含时区的时间控件。
  - datetime：基于UTC时区的日期时间输入控件（时，分，秒及几分之一秒）。
  - datetime-local：用于输入日期时间控件，不包含时区。
  - email：用于应该包含 e-mail 地址的输入域。在提交表单时，会自动验证 email 域的值。
  - number: 用于应该包含数值的输入域。只能输入数字
  - range：用于应该包含一定范围内数字值的输入域。range 类型显示为滑动条。
  - search：用于输入搜索字符串的单行文本字段。换行会被从输入的值中自动移除。
  - tel：用于输入电话号码的控件。在移动端输入会显示数字键盘，PC端无效果
  - url：用于编辑URL的字段。
  - 如果浏览器不解析 type 的值，则当成**文本框**使用

### 视频

- video 标签，支持格式 Ogg，MPEG4,WebM,MP4
- src 属性为资源，播放 url
- autoplay 自动播放视频
- controls 播放控制控件
- loop 重复播放视频
- width 视频宽
- height 视频高度，一般不设置
- 解决兼容性问题

  - 多写几种格式，只会按顺序应用一个

  ```html 兼容性
  <video controls>
    <source src="xx.mp4">
    <source src="xx.ogg">
    <source src="xx.webm">
  </video>
  ```

### 音频

- audio 标签同视频控件
- autoplay loop controls 等
- 支持格式 Ogg Vorbis，MP3，Wav

<Vssue title="HTML issue" />