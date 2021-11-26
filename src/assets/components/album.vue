<template>
  <div class="col-2 item m-3 p-0">
   
    <img :src="group.poster">
    
    <h4>{{group.title}}</h4>
    <p class="group m-0">{{group.author}}</p>
    <p class="data m-0 pb-2">{{group.year}}</p>
  </div> 
</template>
     
    

<script>
export default {
  name:'Album',
  props:{

    group:Object
  }
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.item{
  text-align: center;

    img{
      width: 100%;
      padding: 20px;
    
  }
   background-color:$primaryColor;
   h4{
     color:white;
     margin-bottom:2rem;
   }
   p{
     font-size:12px;
     color:lighten($primaryColor,40%);
   }
}

</style>