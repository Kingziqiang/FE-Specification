### CSS编写规范
#### 1、样式小写
样式选择器，属性名，属性值关键字全部使用小写字母书写
```css
<!--不推荐写法-->
.Title {
  HEIGHT: .5rem
}

<!--推荐写法-->
.title {
  height: .5rem
}
```

#### 2、样式命名
- 面向属性的命名方式：好处是复用性高，因为细化程度高
- 面向语义的命名方式：易于理解

```css
/*面向属性：标题 margin-left: 10px*/
.ml10 {
  margin-left: 10px
}

/*面向语义：标题 margin-left: 10px*/
.title {
  margin-left: 10px
}
```
> 没有孰好孰坏之分，结合业务，统一即可

样式过长如何命名？

建议用 `-` 进行分割
```css
.super-title {
   xxxx
}
```


#### 3、样式编写顺序
- 位置
- 盒模型
- 样式排版
- 外观
```css
.declaration-order {
    /* 位置 */
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 100;

    /* 盒模型 */
    display: block;
    float: right;
    width: 100px;
    height: 100px;

    /* 样式排版 */
    font: normal 13px "Helvetica Neue", sans-serif;
    line-height: 1.5;
    color: #333;
    text-align: center;

    /* 外观 */
    background-color: #f5f5f5;
    border: 1px solid #e5e5e5;
    border-radius: 3px;

    /* 其他 */
    opacity: 1;
}
```

#### 4、样式合并
```css
<!--不推荐写法-->
.title {
  position: relative;
}

.foot {
  position: relative;
}

<!--推荐写法-->
.title,.foot {
  position: relative;
}
```

#### 5、单位数值省略
```css
<!--不推荐写法-->
.title {
  height: 0.5rem
}

<!--推荐写法-->
.title {
  height: .5rem
}
```

#### 6、不要为0指定单位
```css
<!--不推荐写法-->
.title {
  margin: 0px 10px;
}

<!--推荐写法-->
.title {
  margin: 0 10px;
}
```

#### 7、色值采用十六进制与缩写
**十六进制**
```css
<!--不推荐写法-->
.title {
  color: white;
}

<!--推荐写法-->
.title {
  color: #fff;
}
```

**缩写**
```css
<!--不推荐写法-->
.title {
  color: #cccccc;
}

<!--推荐写法-->
.title {
  color: #ccc;
}
```

#### 8、CSS3添加[浏览器前缀](https://www.w3.org/TR/2011/REC-CSS2-20110607/syndata.html#vendor-keywords)
```css
<!--不推荐写法-->
.title {
  border-radius: 10px;
}

<!--推荐写法-->
.title {
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -o-border-radius: 10px;
  -ms-border-radius: 10px;
  border-radius: 10px;
}
```
