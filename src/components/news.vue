<template>
  <div>
    news页面
    <div>
      接收home组件传过来的msg: {{message}}
    </div>
  </div>
</template>
<script>
  import VueEvent from '../model/Eventvue.js';
  export default {
    data() {
      return {
        message: "hello news"
      }
    },
    mounted() {
      VueEvent.$on('to-news', (data) => {
        this.message = data;
      })
    },
  }
</script>
