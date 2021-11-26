<template>
  <div class="col-2 item m-3">
    <div class="album">
      Album
    </div>
    <h3>
      Titolo
    </h3>
    <p class="group">Gruppo musicale</p>
    <p class="data">Data album</p>
  </div> 
</template>

<script>
export default {
  name:'Album'
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
.item{
  text-align: center;
  .album{
    height:100px;
    width:100px;
    background-color:darken($primaryColor,20%);
    margin:10px auto;
  }
   background-color:$primaryColor;
   h3{
     color:white;
   }
   p{
     font-size:12px;
     color:lighten($primaryColor,40%);
   }
}

</style>