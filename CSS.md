# CSS 规范

## 文档目录

0. [代码组织](#1-代码组织)
1. [语法](#2-语法)
2. [声明顺序](#3-声明顺序)
3. [媒体查询](#4-媒体查询)
4. [带前缀的属性](#5-带前缀的属性)
5. [简写形式的属性](#6-简写形式的属性)
6. [注释](#7-注释)
7. [class 命名](#8-class-命名)
8. [选择器](9-选择器)

## 编码规范

### 1 代码组织 

- 以组件为单位组织代码段
- 如果使用了多个 CSS 文件，将其按照组件而非页面的形式分拆

### 2 语法

- 同 [统一代码风格基本规范](./README.md#统一代码风格基本规范)

* 分号
  - 所有声明语句都应当以`分号结尾`
* 空格
  - 每条声明语句的`:`后应该插入一个空格，前没有空格
  - 多个规则的分隔符`,`后应该插入一个空格，前没有空格
  - 属性值中`(`后和`)`前均没有空格
  - 选择器`>`, `+`, `~`前后有空格
  - 大括号`{` 前有空格，后没有空格
  - !important '!'前插入一个空格，后没有空格
  - 注释'/*'后和'*/'前
  - 不要在 rgb()、rgba()、hsl()、hsla() 或 rect() 值的内部的逗号后面插入空格
* 空行
  - 模块之间一个空行
  - 可按照属性声明顺序适当空行
* 换行
  - 为选择器分组时，将`单独的选择器`单独放在一行
  - 为了获得更准确的错误报告，每条`声明`都应该独占一行
  - 声明块的`右花括号`应当单独成行

* 引号

- 最外层统一使用双引号, 如：属性选择器 `li[data-type="single"] {}` ， url的内容`background-image: url(""); ` 

- `十六进制值`应该全部小写，尽量使用简写形式的十六进制值 例如： `#fff`
- 为选择器中的属性添加双引号，例如，input[type="text"]
- 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;
- 用 border: 0; 代替 border: none;

### 3 声明顺序

推荐声明顺序

0. display
1. Positioning
2. Box model
3. Typographic
4. Visual
5. Misc

例: [完整属性列表及其排列顺序](https://github.com/twitter/recess)

```
.declaration-order {
  display: block;
  float: right;
  /* Positioning */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Box-model */
  width: 100px;
  height: 100px;

  /* Typography */
  font: normal 13px "Helvetica Neue", sans-serif;
  line-height: 1.5;
  color: #333;
  text-align: center;

  /* Visual */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;

  /* Misc */
  opacity: 1;
}
```

[推荐的属性的顺序](./CSS-attribute.md)

### 4 媒体查询

将媒体查询（Media query）放在尽可能相关规则的附近。
不要将他们打包放在一个单一样式文件中或者放在文档底部。
如果你把他们分开了，将来只会被大家遗忘。

例: 
```
.u-header figure {
  width: 100%;
}
@media (min-width: 874px) {
  .u-header figure {
    width: 874px;
  }
}
.u-header .top-nav {
  margin-right: 10px;
}
@media (min-width: 874px) {
  .u-header .top-nav {
    margin-right: 0px;
  }
}
```

### 5 带前缀的属性
当使用特定厂商的带有前缀的属性时，通过缩进的方式，让每个属性的值在垂直方向对齐，这样便于多行编辑。

CSS3 前缀包括 

```
'-webkit' : Webkit内核：产要代表为Chrome和Safari
   '-moz' : Gecko内核：主要代表为Firefox
    '-ms' : Trident内核：主要代表为IE浏览器
      '-o': Presto内核：主要代表为Opera
```

推荐工具

[autoprefixer](https://github.com/postcss/autoprefixer)

### 6 简写形式的属性

尽量限制使用简写形式的属性声明。

简写形式主要有
```
padding
margin
font
background
border
border-radius
transition
animation
```

[shorthand properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)

### 7 注释
确保你的代码能够自描述、注释良好并且易于他人理解。好的代码注释能够传达上下文关系和代码目的。不要简单地重申组件或 class 名称。

对于较长的注释，务必书写完整的句子；对于一般性注解，可以书写简洁的短语。

### 8 class 命名


- class名称中只能出现小写字符和破折号（dashe）,破折号应当用于相关 class 的命名（类似于命名空间）（例如，.btn 和 .btn-danger）。
- 避免过度任意的简写。.btn 代表 button，但是 .s 不能表达任何意思。
- class 名称应当尽可能短，并且意义明确
- 使用有意义的名称
- 基于最近的父 class 或基本（base） class 作为新 class 的前缀
- 使用 .js-* class 来标识行为（与样式相对），并且不要将这些 class 包含到 CSS 文件中

### 9 选择器

- 对于通用元素使用 class , 禁止使用标签名
- 选择器要尽可能短，并且尽量限制组成选择器的元素个数，建议不要超过 3
- 只有在必要的时候才将 class 限制在最近的父元素内（推荐使用前缀，类似于命名空间）


**[[⬆]](#)**
