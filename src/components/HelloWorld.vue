<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="flexStyle">
      <div>
        子组件1：home
        <v-home></v-home>
      </div>

      <div>
        子组件2：news
        <v-news></v-news>

      </div>
    </div>

  </div>
</template>

<script>
  import home from "./home.vue";
  import news from "./news.vue";
  export default {
    name: "HelloWorld",
    props: {
      msg: String
    },
    components: {
      "v-home": home,
      "v-news": news
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }

  .flexStyle {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
</style>
