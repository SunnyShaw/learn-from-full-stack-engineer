## router
###SPA（single page web application）
* 优点
不需每次从服务器获取，快速展现给用户

* 缺点
1.不利于SEO
2.点击浏览器前进后退按钮会重新发送请求，没有合理利用缓存
3.单页面无法记住之前滚动的位置


### vue-router
[https://router.vuejs.org/zh-cn/](https://router.vuejs.org/zh-cn/)
* <router-link></router-link>或者this.$router.push({path:""})
* <router-view></router-view>


公用组件：模态框、登录注册、导航、底部公共
其他单独建立文件

### 动态路由匹配
#### hash VS history
默认hash，可修改，例如
```
export default new Router({
  mode:'history',
  routes: [
    {
      path: '/goods/:goodsId/user/:name',
      name: 'GoodsList',
      component: GoodsList
    }
  ]
})
```

```
$route.params.name
```

### 嵌套路由
声明式
<router-link :to="...">

### 编程式路由
#### router.push(location)
router.replace(location)
router.go(n)

例如：
```
export default {
		methods: {
			jump() {
				//this.$router.push({path:'/cart'});
				//this.$router.push("/cart?goodsId=21");
				//this.$router.go(-1)
				this.$router.push({
					path: 'cart',
					query: {
						goodsId: '26'
					}
				})
			}
		}
	}
```
### 命名路由
带参数的命名路由
```
<router-link v-bind:to="{name:'cart',param:{cartId:121}">购物车</router-link>
```

### 命名视图
例如：
```
<router-view class="view one"></router-view>
<router-view class="view two" name="a"></router-view>
<router-view class="view three" name="b"></router-view>
```

```
components: {
        default: Foo,
        a: Bar,
        b: Baz
      }
```
