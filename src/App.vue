<template>
  <div id="app">
    <router-view></router-view>
    <FooterGuide v-show="$route.meta.showFooter"></FooterGuide>
  </div>
</template>

<script>
  import FooterGuide from './components/FooterGuide/FooterGuide.vue'
  //import {reqFoodCategorys} from './api'
  import {mapActions} from 'vuex'

  export default {

   /* async mounted () {
      const result = await reqFoodCategorys()
      console.log(result)
    },*/
   mounted(){
     //this.$store.dispatch('getAddress')
     this.getAddress()
   },

    methods:{
      ...mapActions(['getAddress'])
    },

    components:{
      FooterGuide
    }
  }


</script>

<style lang="stylus" rel="stylesheet/stylus">
  .app
    width 100%
    height 100%
    background #f5f5f5
</style>
