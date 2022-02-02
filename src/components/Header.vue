<template>
  <div class="header-container">
      <img src="../assets/img/logo.svg" alt="">
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

    img{
        height: 100%;
    }
}

.fa-brands{
    color: limegreen;
    font-size: 30px;
    
}
</style>