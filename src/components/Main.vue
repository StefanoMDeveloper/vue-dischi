<template>
  <div class="container-fluid ms-bg-color">
      <div class="container">
          <div class="row">
              <div class="col">
                  <ListaDischi />
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import ListaDischi from "./ListaDischi.vue"

export default {
    name: "Main",
    components: {
        ListaDischi
    }
}
</script>

<style scoped lang="scss">
@import '../assets/style/partials/variables.scss';

.ms-bg-color{
    background-color: $bg-color-2;
    height: 95vh;
}

</style>