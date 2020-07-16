【Vue.js】Modal Window - 做一个模态窗体吧，不能关闭的那种
===================================================

## 视频链接

https://youtu.be/hjk0jN-ZrGM

## 知识点

* 学会使用vue组件 - vuesence-modal-window

## 前提

采用bvue项目模板

## 官网

https://github.com/altrusl/vuesence-modal-window

## 实战演习

### 模板采用 - bvue

```bash
$ npm install @vuesence/modal-window --save
```

### About.vue

```html
...
<button class="btn btn-lg btn-warning ml-2" @click="showModal=true">打开一扇窗</button>
<modal-window
  :visible="showModal"
  :close-on-escape="true"
  :close-on-outside-click="true"
  :show-x-mark="true"
  @close="showModal=false"
>
<h2>用户登录</h2>
<p>请输入您的验证码：</p>
</modal-window>
...
<script>
// @ is an alias to /src
import ModalWindow from "@vuesence/modal-window";

export default {
  name: "about",
  components: {
    ModalWindow
  },
  data: function() {
    return {
      showModal: false
    };
  },
  methods: {}
};
</script>
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com
