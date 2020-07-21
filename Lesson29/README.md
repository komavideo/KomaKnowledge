Vue 3.0 - 小试牛刀
==================

## 视频链接

https://youtu.be/vYpl3nojMe0

## 知识点

* Vue 3.0 beta的使用

## 实战演习

```bash
# 安装vue-cli
$ sudo npm install -g @vue/cli
$ vue -V
# 建立vue工程
$ vue create myvue3
$ cd myvue3
$ npm run build
>dist/js/chunk-vendors.b0f460c7.js    89.18 KiB          31.93 KiB
>dist/js/app.d6e55a1f.js              4.62 KiB           1.65 KiB
>dist/css/app.fb0c6e1c.css            0.33 KiB           0.23 KiB

$ vue add vue-next
$ npm run build
# 比较文件大小
>dist/js/chunk-vendors.9b539114.js    80.55 KiB          30.14 KiB
>dist/js/app.eb6a1669.js              4.53 KiB           1.63 KiB
>dist/css/app.fb0c6e1c.css            0.33 KiB           0.23 KiB

$ npm run serve
http://localhost:8080/
```

## Composition API(组合式 API)

## 官网

https://composition-api.vuejs.org/

### components/MyButton.vue

```html
<template>
  <button @click="increment" class="btn">
      点击次数: {{ state.count }} <br/>
      乘个2吧: {{ state.double }}
</button>
</template>

<script>
import { reactive, computed } from "vue";

export default {
  setup() {
    const state = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    });

    function increment() {
      state.count++;
    }

    return {
      state,
      increment
    };
  }
};
</script>

<style>
.btn {
    width: 280px;
    height: 100px;
    font-size: 24px;
    background-color: rebeccapurple;
    color: white;
}
</style>
```

### App.vue

```html
<template>
  <MyButton/>
</template>
<script>
import MyButton from './components/MyButton.vue'
...
components: {
  MyButton
}
</script>
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com
