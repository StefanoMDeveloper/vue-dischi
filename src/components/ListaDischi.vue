<template>
  <div class="container">
    <Seleziona 
    @filtra= "filtraDischi"/>
    <div class="row row-cols-5 justify-content-evenly">
      <Disco
        v-for="(disco, index) in dischiFiltrati"
        :key="index"
        :info="disco"
        class="col g-4"
      />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Disco from "./Disco.vue";
import Seleziona from "./Seleziona.vue";

export default {
  name: "ListaDischi",
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      arrayDischi: [],
      valueSelect: ""
    };
  },
  components: {
    Disco,
    Seleziona
  },
  computed: {
    dischiFiltrati(){
      return this.arrayDischi.filter( (disco) => {
        return disco.genre.toLowerCase().includes(this.valueSelect);
      })
    }
  },
  created() {
    this.getDischi();
  },
  methods: {
    filtraDischi(){
      this.valueSelect = document.getElementById("selezionaGenere").value;
      console.log(this.valueSelect);
    },
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