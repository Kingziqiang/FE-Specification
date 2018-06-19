### HTML编写规范
#### 1、结构、样式、行为分离
尽量确保文档和模板只包含 HTML 结构，样式都放到样式表里，行为都放到脚本里。

#### 2、指定HTML的文档类型
```HTML
<!DOCTYPE html>
```

如果不指定，很多浏览器都会自行解析，不一定会遵守标准，导致出现所谓的怪异模式

#### 3、在 HTML中指定编码
```html
<meta charset="utf-8">
```
> 这很重要

#### 4、资源引入方式
```html
<!-- CSS -->
<link rel="stylesheet" href="code-guide.css">

<!-- JavaScript -->
<script src="code-guide.js"></script>
````

不建议书写行内样式

#### 5、资源引入顺序
- CSS 放在head上
- JS 尽量放在后面

#### 6、HTML标签尽量小写
> HTML5时开始区分大小写
```html
<!--不推荐-->
<A href=""></A>

<!--推荐-->
<a href=""></a>
```

#### 7、常用属性书写顺序
`class`, `id`, `name`, `src`, `type` ...
```html
<!--推荐-->
<a class="" id="" href=""></a>
```

#### 8、标签语义化
书写具有特定的语义标签有助于提高可读性
```html
<!--不推荐-->
<div class="foot">
...
</div>

<!--推荐-->
<footer>
...
</footer>
```
#### 9、SEO优化
利用好 `keywords`，`description`，`author`这三个最基础且权重最高的特性
```html
<meta name="keywords" content="your keywords">
<meta name="description" content="your description">
<meta name="author" content="author,email address">
```

#### 10、减少标签数量
> 降低 dom 的复杂度

```html
<!--根据情况去掉不必要的 div 标签等-->
<div>
  <div>
     <span>...</span>
  </div>
</div>
```
