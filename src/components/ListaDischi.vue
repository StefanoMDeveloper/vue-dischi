<template>
  <div></div>
</template>

<script>
import axios from "axios";
import Personaggio from "../commons/Disco.vue";

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
          this.arrayDischi = risposta.data;
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },
};
</script>

<style>
</style>