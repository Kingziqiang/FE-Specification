### 解耦
#### 1、实践处理和业务逻辑分离
JavaScript 在页面中除了写业务，还有非常大的比重是实现页面交互。

比如：处理鼠标拖动页面元素，事件处理函数代码如下
```js
const move_while_dnd = function (e) {
  let lb = scheduler._get_lightbox(); //获取元素

  // 设置元素位置
  lb.style.top = `${e.cleentY}'px'`;
  lb.style.left = `${e.cleentX}'px'`;
}
```
这里存在两个问题：
- 业务逻辑与事件处理耦合紧密
- 业务逻辑与事件处理的分离不利于测试

所以，我们需要改下代码：
```js
const setLightBoxPosition = function (top, left) {
  let lb = scheduler._get_lightbox(); //获取元素

  // 设置元素位置
  lb.style.top = `${top}'px'`;
  lb.style.left = `${left}'px'`;
}

const move_while_dnd = function (e) {
  setLightBoxPosition(e.clientY, e.clientX);
}
```
这样`setLightBoxPosition`与事件毫无关联，且测试代码不需要模拟事件，可以直接调用函数实现测试。

#### 2、配置数据与代码逻辑分离
JavaScript 代码基本都是由业务逻辑和数据组成。

这个其实在我们开发中是经常遇到的。比如我们请求接口的时，会有一大堆接口URL
```js
get('xxx/list');

get('xxx/title');

get('xxx/banner');
```
这样写完全可以实现业务，但是，这样不利于维护整个接口。

所以，我们需要改下代码：
```js
/**
 *@file xxx接口管理
 */
const list = 'xxx/list';

const title = 'xxx/title';

const title = 'xxx/banner';

export {
  list,
  title,
  title
}
```
这样，接口被分离处理，即使后面数据变更，我们也可以只修改配置文件。完全不需要修改业务代码。

#### 3、逻辑与结构样式分离