<template>
  <div>  
    <h1>{{ titulo }}</h1>

    <ul>
      <li v-for="foto of fotos">
        <img :src="foto.url" :alt="foto.titulo">
      </li>
    </ul>
  
  </div>
</template>

<script>
export default {

  data() {

    return {
      titulo: 'BANK$LIFE',
      fotos:[]
    }
  },

  created() {

    let promise = this.$http.get('http://localhost:3000/v1/fotos');
    promise.then(res => {

      res.json()).then(fotos => this.fotos = fotos);
  });

}
</script>

<style lang="scss">

h1 {
  font-family: -apple-system, BlinkMacSystemFont,
     'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
      'Open Sans', 'Helvetica Neue', sans-serif;
  text-align: center;
}

</style>
