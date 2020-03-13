<template>
  <div>home内容
    <div>
      <button @click="emitNews()">
        给news组件广播数据
      </button>
    </div>
  </div>
</template>
<script>
  import VueEvent from '../model/Eventvue.js';
  export default {
    data() {
      return {
        msg: "我是一个home组件",
        title: "首页"
      }
    },
    methods: {
      emitNews() {
        // 第一个参数是广播的名字，第二个参数是被传递的值
        VueEvent.$emit('to-news', this.msg);
      }
    },

  }
</script>
