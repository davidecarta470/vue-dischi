<template>
<div class="background">
    <div class="container">
      <div class="row">
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
      </div>
  </div>
</div>
</template>

<script>
import Album from './album.vue'
export default {
   name:'Main',
   components:{
     Album:Album,
   }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.background{
  background-color:darken($primaryColor,10%);
  height: calc(100vh - 60px);
}

</style>