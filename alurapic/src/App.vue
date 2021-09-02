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
      fotos: [
        {
          url: 'https://curtamais.com.br/uploads/conteudos/861776e1ba57c8d51f31db8f7702b7d0.jpg',
          titulo: 'Lehi leite nollie flip no bancão' 
        },
        {
          url: 'https://latitude15.files.wordpress.com/2011/06/img_0915.jpg',
          titulo: 'o PICO'
        }
      ]
    }
  }

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
