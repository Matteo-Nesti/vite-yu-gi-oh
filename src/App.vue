<script>
import AppMain from './components/AppMain.vue'
import axios from 'axios';
import { store } from './store/store.js';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';

export default {
  components: { AppMain },
  created() {
    axios.get(endpoint).then((res) => {
      store.pokemonList = res.data.docs
    })
  }
}
</script>

<template>
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
