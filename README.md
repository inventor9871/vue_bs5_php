## 跟著 黃聰明的書(Vue.js 3 前端漸進式建構框架) 來進步

## Vue 範本(有兩種，一個是 option_API，另一個是 composition_API)
### option_API 範本
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







