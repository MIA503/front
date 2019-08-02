<template>
<el-container style="height: 1000px; border: 1px solid #eee" id="app">
  <Aside :menus="menus" @hello="hello"/>
<Container :content="content"/>
</el-container>
</template>

<script>
import Aside from './components/Aside.vue'
import Container from './components/Container.vue'

export default {
  name: 'app',
  components: {
    Aside,
    Container
  },
  methods: {
    hello: function (msg) {
        this.content = msg;
    }
  },
  data() {
    return {
      content: "Hello Vue",
      menus: [
          {
            id: "1",
            menuTitle: "Installed CLI Plugins",
            menuGroupDatas: [
              {
                groupTitle: "he",
                items: [
                   {
                     "url": "https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel",
                     "content": "babel"
                   },
                   {
                     "url": "https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint",
                     "content": "eslint"
                   },
                ]
              }
            ]
          },
          {
            id: "2",
            menuTitle: "Essential Links",
            menuGroupDatas: [
              {
                groupTitle: "xi",
                items: [
                   {
                     "url": "https://vuejs.org",
                     "content": "Core Docs"
                   },
                   {
                     "url": "https://forum.vuejs.org",
                     "content": "Forum"
                   },
                   {
                     "url": "https://chat.vuejs.org",
                     "content": "Community Chat"
                   },
                   {
                     "url": "https://twitter.com/vuejs",
                     "content": "Twitter"
                   },
                   {
                     "url": "https://news.vuejs.org",
                     "content": "News"
                   },
                ]
              }
            ]
          },
          {
            id: "3",
            menuTitle: "Ecosystem",
            menuGroupDatas: [
              {
                groupTitle: "xi",
                items: [
                   {
                     "url": "https://router.vuejs.org",
                     "content": "vue-router"
                   },
                   {
                     "url": "https://vuex.vuejs.org",
                     "content": "vuex"
                   },
                   {
                     "url": "https://github.com/vuejs/vue-devtools#vue-devtools",
                     "content": "vue-devtools"
                   },
                   {
                     "url": "https://vue-loader.vuejs.org",
                     "content": "vue-loader"
                   },
                   {
                     "url": "https://github.com/vuejs/awesome-vue",
                     "content": "awesome-vue"
                   },
                ]
              }
            ]
          }
      ]
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
