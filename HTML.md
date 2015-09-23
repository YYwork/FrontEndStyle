# HTML 规范

## 编码规范

### 标签

- 不允许遗漏可选的关闭标签
- 使用尽可能少的标签嵌套
- 尽量不使用 JS 生成标签

- `实用高于完美`

  尽量遵循HTML标准和语义，但是不应该以浪费实用性作为代价；
  任何时候都要用尽量小的复杂度和尽量少的标签来解决问题。。

示例： 
`</li>` 和 `</body>`

- 自动闭合标签结尾处建议使用斜线

示例： 
```
  <br /> <hr /> <area /> <base /> <img /> <input /> <link /> <meta /> <basefont/> <param/> <col/> <frame/> <embed /> <keygen /> <source /> 
```

---

### 属性

- 属性上，使用`双引号`，不允许使用单引号，不允许不使用引号

示例：
```
  <input type="button" />
```

- 属性名`全小写`，用`中划线`做分隔符，不允许使用大写，例：`form-control`
- class 等非 JS 使用的属性值`全小写`，用`中划线`做分隔符，不允许使用大写

示例：
```
  <input class="form-control" data-role="getPic" type="button" />
```


- 自定义属性作为JS的hook，建议以data-为前缀
- JS 使用的属性值使用驼峰命名形式，例：`getPic`

示例：
```
  <input data-role="getPic" type="button" />
```

- 建议属性声明顺序

  class是为高可复用组件设计的，所以应处在第一位；
  id更加具体且应该尽量少使用，所以将它放在第二位。

  + class
  + id, name
  + data-*
  + src, for, type, href, value , max-length, max, min, pattern
  + placeholder, title, alt
  + aria-*, role
  + required, readonly, disabled

---

### DOCTYPE

使用 HTML5 doctype；

在页面开头使用这个简单地doctype来启用标准模式，使其在每个浏览器中尽可能一致的展现；

虽然doctype不区分大小写，但是按照惯例，doctype大写。

示例：
```
<!DOCTYPE html>
<html>
  ...
</html>
```

---

### 语言

建议为 html 根元素指定 lang 属性，从而为文档设置正确的语言。这将有助于语音合成工具确定其所应该采用的发音，有助于翻译工具确定其翻译时所应遵守的规则等等。

示例：
```
<!DOCTYPE html>
<html lang="zh-CN">
  <!-- ... -->
</html>
```

---

### 字符编码

通过声明一个明确的字符编码，让浏览器轻松、快速的确定适合网页内容的渲染方式，通常指定为'UTF-8'。

示例：
```
<!DOCTYPE html>
<html lang="zh-CN">
    <head>
        <meta charset="UTF-8">
    </head>
    ...
</html>
```

---

### IE兼容模式

用 <meta> 标签可以指定页面应该用什么版本的IE来渲染；

示例：
```
<!DOCTYPE html>
<html lang="zh-CN">
    <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=Edge" />
    </head>
    ...
</html>
```

---

### 引入 CSS, JS

- `link` 必须声明 `rel="stylesheet"`
- `CSS` 没有特殊要求的情况下写在 `head` 标签内部
- `JS` 没有特殊要求的情况下写在 `body` 内部末尾
- 引入 `CSS` 和 `JS` 时不需要指明 `type`，因为 `text/css` 和 `text/javascript` 分别是他们的默认值

示例：
```
<!-- External CSS -->
<link rel="stylesheet" href="code_guide.css">

<!-- In-document CSS -->
<style>
    ...
</style>

<!-- External JS -->
<script src="code_guide.js"></script>

<!-- In-document JS -->
<script>
    ...
</script>
```

---

### boolean 属性

boolean属性指不需要声明取值的属性，XHTML需要每个属性声明取值，但是HTML5并不需要；

示例：
```
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
    <option value="1" selected>1</option>
</select>
```


