# HTML 规范

## 编码规范

### 标签

- 不允许遗漏可选的关闭标签，例：</li> 和 </body>
- 自动闭合标签结尾处建议使用斜线；

### 属性

- 属性上，使用`双引号`，不允许使用单引号，不允许不使用引号；
- 属性名`全小写`，用`中划线`做分隔符，不允许使用大写，例：form-control；
- 自定义属性作为JS的hook，建议以data-为前缀；

示例：
```
  <input data-role="getPic" type="button" />
```

- 建议属性声明顺序

  + class
  + id, name
  + data-*
  + src, for, type, href
  + title, alt
  + aria-*, role

### 