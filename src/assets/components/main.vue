<template>
<div class="background">
    <div class="container">
      <div class="row ">
        <Select @sendSelect="chosedGenra" />
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
import SelectGenre from './SelectGenre.vue'
export default {
   name:'Main',
   components:{
     Album:Album,
     Select:SelectGenre
   },
   data(){
     return{
       groups:[],
       genre:'all',
       groupsChosed:[]
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
          
          if (this.genre !== 'all') {
            this.groupsChosed=[]
            this.groups.forEach((group)=>{
              if (group.genre === this.genre){
                this.groupsChosed.push(group)
              }
            })
            this.groups=[];
            this.groups = this.groupsChosed
          }
             
        })
        .catch(e=>{
          console.log(e)
        })
     },
     chosedGenra(text){
       this.genre=text;
       this.getApi()
     }

   }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.background{
  background-color:darken($primaryColor,10%);
  min-height: 100vh;
}

</style>
       
           


            
          
        
