<template>
<div class="background">
    <div class="container">
      <div class="row ">
        <Album
        v-for="(group,index) in groups" :key="index"
        :group='group'
        />
      </div>
  </div>
</div>
</template>

<script>
import axios from 'axios';
import Album from './Album.vue';
export default {
   name:'Main',
   components:{
     Album:Album,
   },
   data(){
     return{
       groups:[]
     }
   },
   mounted(){
    this.getApi()
   },
   methods:{
     getApi(){
       axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then(r=>{
         this.groups=r.data.response;
          console.log(this.groups);
        })
        .catch(e=>{
          console.log(e)
        })
     }
   }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.background{
  background-color:darken($primaryColor,10%);
}

</style>