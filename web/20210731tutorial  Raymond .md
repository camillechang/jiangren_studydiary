# 20210731 Raymond tutorial

- Margin 不同值的区别

> margin: 20px;（上、下、左、右各20px。）
margin: 20px 40px;（上、下20px；左、右40px。）
margin: 20px 40px 60px;（上20px；左、右40px；下60px。）
margin: 20px 40px 60px 80px;（上20px；右40px；下60px；左80px。）

- z-index 一张纸，上面盖住下面。有时候起作用，有时候不行。The `z-index` property specifies the stack order of an element. An element with greater stack order is always in front of an element with a lower stack order.

- inline-block: 内部是block不能被打断。外表是Inline的样式。纯Block是整个占一行。

- color: #fffffff15 = rgb(ff,ff,ff,0.15)

- div :frist-child， 所有div的 第一孩子。div:first-child,第一个div的孩子。 所以最好直接用 div *:first-child来表示。

- **html写代码快速方式 html>body>header.header_one>nav>ul>li*3,很多编译器都支持**

  一些vscode 快捷键：

  https://blog.csdn.net/ycx60rzvvbj/article/details/105775469

- github图片 可以通过link add  ?**raw=true**;下载图片

- css是可压缩的，真正商业项目中。

- border-sizing:border-box; 使内容不比父元素大。