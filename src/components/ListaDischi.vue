<template>
  <div class="container">
    <div class="row row-cols-5 justify-content-evenly">
      <Disco
        v-for="(disco, index) in arrayDischi"
        :key="index"
        :info="disco"
        class="col m-3"
      />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Disco from "./Disco.vue";

export default {
  name: "ListaDischi",
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      arrayDischi: [],
    };
  },
  components: {
    Disco,
  },
  created() {
    this.getDischi();
  },
  methods: {
    getDischi() {
      axios
        .get(this.apiUrl)
        .then((risposta) => {
          this.arrayDischi = risposta.data.response;
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },
};
</script>

<style lang="scss" scoped>

</style>