<template>
  <div class="select-position">
    <select 
    v-model="selected"
    class="my-4" 
    id=""
    >
      <option @click="$emit('sendSelect',selected)" value="all">All</option>
      <option @click="$emit('sendSelect',selected)" value="Pop">Pop</option>
      <option @click="$emit('sendSelect',selected)" value="Rock">Rock</option>
      <option @click="$emit('sendSelect',selected)" value="Jazz">Jazz</option>
      <option @click="$emit('sendSelect',selected)" value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
   name:"SelectGenre",
   data(){
     return{
       selected:'all'
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