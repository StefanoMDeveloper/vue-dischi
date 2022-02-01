<template>
  <select name="genere" 
  id="selezionaGenere" 
  @change="$emit('filtra')"
  >
      <option value="">All</option>
      <option value="jazz">Jazz</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="metal">Metal</option>
  </select>
</template>

<script>
export default {
    name: "Seleziona",
    data() {
        return{
            inputSelect: ""
        }
    }
}
</script>

<style scoped lang="scss">

</style>