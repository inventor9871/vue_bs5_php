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
// const message = ref('Vue.js 3');
<p v-pre> {{ message }}</p>
// HTML 只會顯示 {{ message }}
```
* v-text
```
<p>*******{{ message }}</p>
// HTML 會顯示 *******vue.js 3

<p v-text="message">*******這邊的文字不會顯示</p>
// HTML 只會顯示  vue.js 3
```
所以不建議在多層次裡使用 v-text
```
<p v-text="facebook">
  <i class="fa-facebook"></i>
</p>
```

### [bootstrap 5](https://getbootstrap.com/)、[六角中文版](https://bootstrap5.hexschool.com/docs/5.0/getting-started/introduction/)
* 載入 BS5 CDN (css、js)
```
<!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-F3w7mX95PdgyTmZZMECAngseQB83DfGTowi0iMjiWaeVhAn4FJkqJByhZMI3AhiU" crossorigin="anonymous">


<!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-/bQdsTh/da6pkI1MST/rWKFNjaCP5gBSY4sEBT38Q/9RBh9AH40zEOg7Hlq2THRZ" crossorigin="anonymous"></script>

```

### [Font Awesome](https://docs.fontawesome.com/)
* [fa 的官網說，CDN只支援 v5以下的版本](https://docs.fontawesome.com/web/setup/use-kit/)
* 來看一下 [w3schools](https://www.w3schools.com/icons/icons_reference.asp) 與 [TW版](https://w3schools.tw/icons/fontawesome_icons_intro.asp)
```
<script src="https://kit.fontawesome.com/yourcode.js" crossorigin="anonymous"></script>
```




