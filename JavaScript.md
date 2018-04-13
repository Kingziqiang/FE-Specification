#### 1、注释
**单行注释**
```js
// 单行注释
const foo = 1;
```

**多行注释**
```js
/**
 * 多行注释
 */
const foo = 1;
```

**函数注释**
```js
/**
 * 函数说明
 * @param {string} p1 参数1的说明
 * @param {string} p2 参数2的说明
 * @return {Object} 返回值描述
 */
function foo(p1, p2, p3) {
    // xxx
}
```

**文件注释**


#### 2、变量命名
**变量名称用驼峰**
```js
// 推荐
let firstName = 'Peter';

// 不推荐
let firstName = 'peter';
```

**函数**
- 构造函数：使用大驼峰
```js
// 推荐
function StudentGrade () {
  
}
```

- 其他：使用小驼峰
```js
// 推荐
function studentNrade () {
  
}
```

#### 3、总是使用 [===](https://www.zhihu.com/question/20348948/answer/14867031)
```js
// 推荐
if ('1' === 1) {
   // xxx
}

// 不推荐
if ('1' == 1) {
   // xxx
}
```

#### 4、注意[关键字和保留字](http://www.itxueyuan.org/view/6627.html)的使用
常见的保留字有: class, break, return等
```js
// 不推荐
let class = 1; // class 是保留字

// 推荐
let foo = 1;
```

#### 5、尽量不再使用 var
- 使用`const` 和 `let`
```js
// 不推荐
var foo = 'peter';

// 推荐
const foo = 'peter';
```

#### 6、使用字面量创建对象
```js
// 不推荐
let foo = new Object();

// 推荐
let foo = {};
```

#### 7、属性和方法用简写的形式
ES6 允许直接写入变量和函数，作为对象的**属性**和**方法**
```js
const foo = 'job';

// 不推荐
const baz = {
   job: foo
}

// 推荐
const baz = {
   foo
}

// 不推荐
const foo = {
  say: function() {
    return "Hello!";
  }
};

// 推荐
const foo = {
  say () {
    return "Hello!";
  }
};
```

#### 8、总是在JavaScript中使用`'`(单引号)
```js
// 不推荐
const foo = "job";

// 推荐
const foo = 'job';
```

#### 9、使用模板字符串拼接字符串
```js
// 不推荐
const foo = 'job' + dream;

// 推荐
const foo = `job${dream}`;
```

#### 10、模块不要混写
- export(default),import
- (module)exports,require
```js
// 不推荐
var helper = require('./helpers');
module.exports = helper;

// 推荐
import helper from './helpers';
export default helper;
```
