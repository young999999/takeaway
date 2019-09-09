<template>
  <div id="app">
    <router-view></router-view>
    <FooterGuide v-show="$route.meta.showFooter"/><!--判断当前路由的meta的showFooter的值-->
  </div>
</template>

<script>
  import FooterGuide from './components/FooterGuide/FooterGuide.vue'
  import {reqFoodCategorys} from './api'

  export default {
    async mounted(){
      this.$store.dispatch('getAddress')
    },
    components: {
      FooterGuide
    }
  }
</script>

<style  lang="stylus" rel="stylesheet/stylus">
  .app
    width 100%
    height 100%
    background #f5f5f5
</style>
