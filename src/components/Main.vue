<template>
  <div class="container-fluid ms-bg-color pt-5">
      <ListaDischi />
  </div>
</template>

<script>
import ListaDischi from "./ListaDischi.vue";

export default {
  name: "Main",
  components: {
    ListaDischi,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/style/partials/variables.scss";

.ms-bg-color {
  background-color: $bg-color-2;
  height: 1000px;
}
</style>