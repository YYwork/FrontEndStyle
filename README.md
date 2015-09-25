# 前端规范

编写灵活、稳定、高质量的 HTML 和 CSS 代码的规范。

目标：无论团队人数多少，代码应该同出一门。

### 目录结构

* [统一命名规范](#统一命名规范)
  - [目录命名](#目录命名)
  - [文件命名](#文件命名)
* [统一代码风格基本规范](#统一代码风格基本规范)
* [HTML 规范](./HTML.md)
* [CSS 规范](./CSS.md)
* [JavaScript 规范](./JavaScript.md)

推荐技术(非强制)

##### 自动化

* [grunt](./Gruntfile.md)

##### 移动端

* [移动端适配](./flexible.md)

### 统一命名规范

##### 目录命名

+ 采用小写方式， 以下划线分隔。
+ 有复数结构时，要采用复数命名法。

    例：templates, scripts, styles, images, data_models

##### 文件命名

- 同 [目录命名](#目录命名)

- js, JSX 文件命名

    例：account_model.js

- css, less, sass, stylus 文件命名

    例：image_sprites.css

- HTML, Jade 文件命名

    例：error_report.html

### 统一代码风格基本规范

- 缩进使用 2 个空格，禁止使用 4 个空格 和 `tab` 键；(2 个空格 -- 这是唯一能保证在所有环境下获得一致展现的方法。)
- 嵌套的语法应该缩进一次（即两个空格）

- 保存文件时，删除尾部的空白符
- 设置文件编码为 UTF-8
- 在文件结尾添加一个空白行

[editorconfig](http://editorconfig.org/)

### 推荐注释

- 难于理解的代码段
- 可能存在错误的代码段
- 浏览器特殊的HACK代码
- 业务逻辑强相关的代码


---

#### 参考：

- [bootcss](http://codeguide.bootcss.com/)
- [alloyteam](http://alloyteam.github.io/CodeGuide/#html-syntax)
- [duowan](https://github.com/duowan/fe-guide)
- [suning](https://github.com/suning-wireless/Front-End-Standards)
- [猎豹移动](https://github.com/CMCM-F2E/fe-standards)
- [亚信UED](https://github.com/Alsiso/AICG)
- [豆瓣CSS Code Guideline](https://github.com/kejun/CSS-Code-Guideline)
- [spec css style guide](https://github.com/ecomfe/spec/blob/master/css-style-guide.md)