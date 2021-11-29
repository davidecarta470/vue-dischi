<template>
  <div class="select-position">
    <select 
    
    class="my-4" 
    id=""
    >
      <option v-for="(option,index) in options" :key="index" @click="$emit('sendSelect',options[index])" value="option">{{option}}</option>
    </select>
  </div>
</template>

<script>
export default {
   name:"SelectGenre",
   data(){
     return{
       options:['all','Pop','Rock','Jazz','Metal'],
  
     }
   },
  
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.select-position{
  justify-content: end;
  display: flex;
    select{
      background-color:$primaryColor;
      margin-right:80px;
      color: white;
      border:2px solid lighten($primaryColor,10%);
    }

}
</style>