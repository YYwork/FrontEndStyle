# CSS 规范

## 文档目录

1. [语法](#1-语法)
2. [声明顺序](#2-声明顺序)
3. [文本排版](#5-文本排版)
4. [媒体查询](#7-媒体查询)
5. [兼容性](#8-兼容性)
6. [代码注释](#9-代码注释)

## 编码规范

### 1 语法

- 同 [统一代码风格基本规范](./README.md#统一代码风格基本规范)

- 为选择器分组时，将`单独的选择器`单独放在一行
- 为了代码的易读性，在每个声明块的`左花括号`前添加一个空格
- 声明块的`右花括号`应当单独成行
- 每条声明语句的` : `后应该插入一个空格， : 前没有空格
- 为了获得更准确的错误报告，每条`声明`都应该独占一行
- 所有声明语句都应当以`分号结尾`
- 对于以`逗号分隔`的属性值，每个逗号后面都应该插入一个空格
- 不要在 rgb()、rgba()、hsl()、hsla() 或 rect() 值的内部的逗号后面插入空格
- `十六进制值`应该全部小写，尽量使用简写形式的十六进制值 例如： `#fff`
- 为选择器中的属性添加双引号，例如，input[type="text"]
- 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;

### 2 声明顺序

推荐声明顺序

1. Positioning
2. Box model
3. Typographic
4. Visual
5. Misc

例: [完整属性列表及其排列顺序](https://github.com/twitter/recess)

```
.declaration-order {
  /* Positioning */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Box-model */
  display: block;
  float: right;
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


### 2 媒体查询

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

### 3 带前缀的属性
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

### 简写形式的属性

尽量限制使用简写形式的属性声明。

简写形式主要有
```
padding
margin
font
background
border
border-radius
```

[shorthand properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)

**[[⬆]](#)**
