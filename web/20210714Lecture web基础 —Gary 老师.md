# Lecture web基础 —Gary 老师

### 1 各类元素的选择器优先级。inline> id> class

### 2 BEM(Block, Elements-head/arm/feet, Modifiers-red/stick) 命名规则

Block   .stick-man{}

Elements  .stick-man__head{}

Modifiers  .stick-man—blue{}

### 3 Responsive web design

- CSS3 media queries 区分像素大小不同布局
- set viewport, <meta name="viewport" content="width=device-width, initial-scale=1.0">不因缩放影响布局
- Grid话， 用Bootstrap库或其他库的，~~不用本身的css grid~~.

### 4 Scss

1. Css可复用不高， sass(pre css) 可以编译成css.

**`npm install sass -g`**

Scss—css的超体，大多用这个

Sass—更快速的写css,

### 5 Component library

  有的库有design language 比如material-ui库， 有的没有比如bootstrap。

大公司都会有自己的UI库。

### 6 HTML tag分为两种:

- block element: `<div> <header> <main> <section> <h1>-<h6>`
    - i: 占据整行
    - ii: 上下有空间
    - <section>: content inside is grouped, should appear as an entry in an outline of page.
- inline element: 等 <a> <label>
    - i: 不会换行，默认在同一行中
    - ii: 上下不占空间

### **. 7 常用tag:**

- h1, h2, h3, h4, h5, h6: h1每个配置里只能有一个，有层级关系，需要依次使用，不能挑选使用，搜索引擎SEO会注重这一点
- `<p>`: Paragraph 很常用
- `~~<b> <strong> <i> <em> <mark> <small> <del> <ins>`:~~ Text - Format element格式调整，但大多标签最好不使用，因为在不同浏览器中可能有不同效果，因此要用css实现。除`<strong>`有语义以外。
- `<br>`: 换行
- `<span>`: 可使用span圈中某部分，再用css添加效果，本身不带有style
- `<ul> <ol> <li>`: list标签。ul (unsorted list) ol (ordered list)。会在navigation bar中使用
- `<table>`: 表。一般不会直接用html写，会通过React等framework写。
- `<div>`: default block element
- `<a>`: Link。包含target，_blank在新标签页打开
- `<img>`: 图片。要加alt，对图片的描述。可以用height width调整，但更多要用CSS调整。建议技巧：将图片作为一个background-image放在一个

    中。

- `~~<form> <input> <select> <textarea>~~`: 不再在html中使用，通过JavaScript异步实现。要对应一个会在测试中使用。
- `HTML5 <input>`: require, type可以对input的内容制定输入规则
- `<audio> <video>`: 很少使用通过html做，播放音乐，视频。
- `<!— —>`: comment，主要用于解释一些比较复杂的business logic
- caniuse.com：Browser Compatibility。查询哪些浏览器支持哪些tag。

### 8 **File path 文件路径:**

- `../` （相对路径）退到上一层目录
- `./` （相对路径）当前目录
- `/`（绝对路径）从root开始
- 绝对路径使用更多

### 9 **units**

- `px` 像素是一种绝对单位，指定的值不会变化
- `%` 相对单位，会在responsive中用到
- `vh vw`占视窗的大小
- `auto 0` 很早之前水平居中等使用
- `em rem` 基于字体大小，em继承父元素大小，rem直接找到最原始的大小

### 10 live-server插件: 命令行安装 npm install -g live-server

浏览器可实时查看效果

## 小技巧：

**在HTML文件中输入 html:5,按tab键后，自动生成代码**