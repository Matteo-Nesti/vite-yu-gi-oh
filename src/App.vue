<script>
import AppMain from './components/AppMain.vue'
import AppSelect from './components/AppSelect.vue'
import axios from 'axios';
import { store } from './store/store.js';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';

export default {
  data() {
    return {
      filteredType: null,
    }
  },
  components: { AppMain, AppSelect },
  created() {
    this.fetchCharacters(endpoint)
  },
  methods: {
    fetchCharacters(url) {
      axios.get(url).then((res) => {
        store.pokemonList = res.data.docs
      })
    },

    onSelectChange(select) {
      this.filteredType = select
      const filterEndpoint = `${endpoint}?eq[type1]=${this.filteredType}`
      this.fetchCharacters(filterEndpoint)
    },

  }
}
</script>

<template>
  <header>
    <AppSelect @select-change="onSelectChange" />
  </header>
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
