## 跟著 黃聰明的書(Vue.js 3 前端漸進式建構框架) 來進步

## Vue 範本(有兩種，一個是 option_API，另一個是 composition_API)
### option_API 範本(本書採用)
* < /body>下方加入 vue 的 CDN
```
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
```
* 在 CDN 下面加上 vue 的 <script>
```
<script>
    const app = Vue.createApp({

    })
    app.mount('#app')
</script>
```
* 在 < body> 新增一個 DIV
```
<div id="app"></div>
```
### composition API 範本
* 所有的 VUE 程式碼都寫在 setup 裡面，最後 return 狀態或方法
```
<script>
    const { ref } = Vue;
    const app = Vue.createApp({
        setup(){
            const message = ref('Vue.js 3');
            
            return {
                message
            }
        }
    })
</script>
```







