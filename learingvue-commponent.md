在component里面有多种情况，其实很多情况下都是从别的组件导入此组件

1. 导入组件
> 本组件写
```
<script>
const heard = { template: '<div>this is heardComponent</div>' }
</script>
```
导入组件
```
<script>
import heard from './components/heard.vue'
</script>
```
2. 注册component
全局注册组件
```
<script>
import Vue from 'vue'

Vue.component ('heard',{
    template: heard
})
</script>
```
局部注册component
```
<script>
new Vue ({
    el:'#app',
    components: {
        'heard': heard
    }
})
</script>
```
3. 使用component
```
// xxx.vue 文件里面使用
<div id="app">
    <heard></heard
</div>
```
