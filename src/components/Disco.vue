<template>
  <div class="disco">
    <img :src="info.poster" :alt="info.title" />
    <h5>{{ info.title }}</h5>
    <div class="testo">
      <p>{{ info.author }}</p>
      <p class="anno">{{ info.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  nome: "Disco",
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";
h5 {
  text-transform: uppercase;
  color: white;
  margin: 20px 0;
}

.testo{

    p {
    color: grey;
}
}


.anno {
  font-size: 12px;
}

.disco {
  text-align: center;
  background: $bg-color-1;
  width: 160px;
  padding: 10px 10px 40px 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  img {
    width: 90%;
  }
}
</style>