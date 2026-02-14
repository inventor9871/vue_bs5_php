## 跟著 黃聰明大大的書(Vue.js 3 前端漸進式建構框架) 來進步

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
    //     data (){
    //         return {
    //             message: 'vue.js 3',
    //             button_title: '開始學習',
    //             number: [1,2,3],
    //         }
    //     }
    })
    app.mount('#app')
</script>
```
* 在 < body> 新增一個 DIV
```
<div id="app"></div>
```
### composition API 範本
* 所有的 VUE 程式碼都寫在 setup 裡面，最後 return 資料或方法
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

### {{ 放資料或運算 }} mustache ，放在 HTML中 顯示 資料
```
<h2> {{ message }}</h2>
<button> {{ button_title}} </button>
{{ number.map(x => x*2) }}

```

### vue 的屬性
* v-pre，輸入甚麼，顯示甚麼
```
<p v-pre> {{ message }}</p>
// HTML 只會顯示 {{ message }}
```
* v-text
```
<p> {{ message }}</p>
<p v-text="message">這邊的文字不會顯示</p>
```
所以不建議在多層次裡使用 v-text
```
<p v-text="facebook">
  <i class="fa-facebook"></i>
</p>
```








