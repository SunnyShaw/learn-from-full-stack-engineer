## 一、Introduce
### vue & react
1.virtual Dom
2.轻量
3.服务器端渲染
4.集成路由工具，打包工具，状态管理工具


###  vue VS react
> vue
 模板，渲染函数
  速度
  体积
 组件化
 MV*
 数据驱动，状态管理
 没有控制器

>  react
大型应用
 web ,app

### Vue核心思想基本原理
Object.defineProperty()
扩展属性，双向绑定
[https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)
get
一个给属性提供 getter 的方法，如果没有 getter 则为 undefined。该方法返回值被用作属性值。默认为 undefined。
set
一个给属性提供 setter 的方法，如果没有 setter 则为 undefined。该方法将接受唯一参数，并将该参数的新值分配给该属性。默认为 undefined。

### Vue全家桶：
1.vue-router（http://router.vuejs.org）
2.vuex（http://vuex.vuejs.org）， 3.vue-resource（https://github.com/pagekit/vue-resource）
4.构建工具vue-cli

## 二、Base
### 基础语法
1.模板语法

mustache
html
v-bind:id=""
表达式
v-text=""
v-if=""
过滤器：{{message | capitalize}}

2.class style绑定

v-bind:class="{}"
v-bind:style="{}"
对象，数组

3.条件渲染

v-if
v-else
v-else-if
v-show
v-cloak

4.事件处理器

* 事件：
  v-on:click 或 @click

* 事件修饰符：
v-on:click.stop
.stop
.prevent
.capture
.self
.once

* 键值修饰符
v-on:keyup.enter
全部的按键别名：
.enter
.tab
.delete (捕获 “删除” 和 “退格” 键)
.esc
.space
.up
.down
.left
.right

5.事件处理器

* 全局组件，局部组件

* 父子组件通讯-数据传递
          pass props
  Parent ---------------> Child


          emit events
  Parent <--------------- Child

* slot

### vue-cli
```
npm install -g vule-cli
```

```
vue init webpack-simple yourproject
```
或者
```
vue init webpack yourproject
```

[https://github.com/vuejs/vue-cli](https://github.com/vuejs/vue-cli)

### 配置文件
