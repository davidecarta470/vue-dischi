<template>
 <div>
   <Header/>
   <Main/>
 </div>
</template>

<script>
import Header from './assets/components/header.vue';
import Main from './assets/components/main.vue'
export default {
  name: 'App',
   components:{
     Header:Header,
     Main:Main,

   }
}
</script>

<style lang="scss">
@import './assets/style/generals.scss';
@import './assets/style/vars.scss';
</style>