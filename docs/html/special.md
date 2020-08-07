# HTML中的特别属性

有些很重要/常见的属性

## src属性

- src属性设置其来源，可以是相对或者是绝对路径
- 在Audio、Video标签中的src是设置或返回音频/视频元素的当前来源
- img标签的 src 属性是必需的。它规定图像的 URL
- input的src表示作为提交按钮使用的图像的 URL
- script标签的src表示规定外部脚本文件的 URL
- src 用于替换当前内容

**当浏览器解析到src ，会暂停其他资源的下载和处理，直到将该资源加载或执行完毕**

## href属性

- href 属性的值可以是任何有效文档的相对或绝对URL，或者是锚URL指向页面中的锚（href="#top"）
- `<a>` 标签的 href 属性用于指定超链接目标的 URL
- **href 用于在当前文档和引用资源之间确立联系**
- 当点击带有**href属性**的标签时才会下载文件或者跳转到指定的URL，**解析html时无影响**（区分src）

## defer属性(只有ie支持)

- defer 属性规定是否对脚本执行进行**延迟**，直到页面加载为止
- 如果您的脚本不会改变文档的内容，可将 defer 属性加入到 `<script>` 标签中，以便加快处理文档的速度
- defer属性主要**用于加载不会改变文档的script**，如果你的script在文档加载的时候需要通过js代码对DOM操作那么请不要用defer
- defer会延迟加载，以便可以快速加载文档而不会出现阻塞，优化用户体验
- 对于defer的兼容，**原则上只有ie支持**，至于各大厂家最新版本是否对其待验证

## async(html5新增)

- async 属性规定**一旦脚本可用**，则会**异步执行**
- async异步加载的script可能会**乱序执行**，所以加载的script尽量**不要包含依赖**，在加载完成后会立即执行
- 如果使用`async="async"`，脚本相对于页面的其余部分异步地执行（当页面继续进行解析时，脚本将被执行）
- 如果不使用async且使用`defer="defer"`，脚本将在页面完成解析时执行
- 如果既不使用async也不使用defer，在浏览器继续解析页面之前，立即读取并执行脚本
- **当script同时有async和defer属性时，执行效果和async一致**
- async与defer都只支持外部加载的script

## label的for属性

- label的for属性的值与其关联控件的id一样，这样当点击label时就会关联到控件

```html label的for属性
<!-- 显式的联系： -->
<label for="SSN">Social Security Number:</label>
<input type="text" name="SocSecNum" id="SSN" />

<!-- 隐式的联系： -->
<label>Date of Birth: <input type="text" name="DofB" /></label>
```

- 显式联系，通过for属性与控件id对应
- 隐式联系，直接把关联的控件包含在label双标签内，无需for属性

## 锚点链接

- 定义锚点
  `<a name="锚点名"></a>`
  `<a id="锚点名"></a>`
- 找到锚点
  `在浏览器网址最后加入#锚点名、或<a href="#锚点名">内容</a>`
- a 的 target 属性目标为框架名`framename`时，在指定的框架中打开被链接文档
- a 的 target 属性目标链接其他打开方式：
- `_blank`在新窗口打开目标文件
- `_parent`在父框架集中打开被链接文档。
- `_self`	默认。在相同的框架中打开被链接文档。
- `_top`在整个窗口中打开被链接文档。

### 持续补充。。。

<Vssue title="HTML issue" />