<template>
  <div>
    <header>Logo</header>
  </div>
</template>


<script>
export default {
  name:'Header',
}
</script>

<style lang="scss" scoped>
@import '../style/vars.scss';
header{
  min-height:60px;
  background-color:$primaryColor;
  color:white
}

</style>