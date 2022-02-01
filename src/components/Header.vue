<template>
  <div class="header-container">
      <i class="fa-brands fa-spotify"></i>
  </div>
</template>

<script>
export default {
    name: "Header",
    components: {
    }
    
}
</script>

<style scoped lang="scss">
@import '../assets/style/partials/variables.scss';

.header-container{
    padding: 10px;
    height: 50px;
    background-color: $bg-color-1;
}

.fa-brands{
    color: limegreen;
    font-size: 30px;
    
}
</style>