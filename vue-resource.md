### Vue-Resource
npm :
[https://www.npmjs.com/package/vue-resource](https://www.npmjs.com/package/vue-resource)

github:
[https://github.com/pagekit/vue-resource](https://github.com/pagekit/vue-resource)

#### 安装
```
npm install vue-resource --save
```
#### HTTP
[https://github.com/pagekit/vue-resource/blob/master/docs/http.md](https://github.com/pagekit/vue-resource/blob/master/docs/http.md)
```
get(url, [options])
head(url, [options])
delete(url, [options])
jsonp(url, [options])
post(url, [body], [options])
put(url, [body], [options])
patch(url, [body], [options])
```

#### Interceptors
```
Vue.http.interceptors.push(function(request, next) {

  // modify method
  request.method = 'POST';

  // modify headers
  request.headers.set('X-CSRF-TOKEN', 'TOKEN');
  request.headers.set('Authorization', 'Bearer TOKEN');

  // continue to next interceptor
  next();
});
```

v-resource:挂载在实例上
axios:没有挂载在实例上，暴露一个全局变量