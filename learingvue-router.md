#### 关于vue-router 使用
1. 肯定里面要有这个模块，然后引入，使用
```
import Router from 'vue-router'

Vue.use(Router)
```
#### 然后再开始使用

1. 引入组件
> 利用import
```
import heard from './components/heard'
import foot from './components/foot'

```
2. 注册router
```
const routes = [
    { path: '/heard', component: heard },
    { path: '/foot', component: foot }
]

```
3. 创建vue-router实例
```
const router = new VueRouter({
    routes
})
```
3. 使用
```
<script>
new Vue({
    el: '#app',
    router
})
</script>
```
```
<div id="app">
    <router-link to="/heard"> 我是头部 </router-link>
    <router-link to="/foot"> 我是尾部 </router-link>
    <!-- 渲染内容 -->
    <router-view></router-view>
</div>
```
