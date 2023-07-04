<template>
    <section id="characters" class="container">
        <div class="row row-cols-5 grayBg">
            <div v-for="character in store.pokemonList">
                <CharacterCard :name="character.name" :image="character.imageUrl" :type1="character.type1" :type2="character.type2" :color="character.color" :number="character.number" />
            </div>
        </div>
    </section>
</template>

<script>
import CharacterCard from './CharacterCard.vue'
import { store } from '../../store/store.js';

export default {
    components: { CharacterCard },
    data() {
        return { store }
    }
}
</script>

<style lang="scss" scoped>
.grayBg {
    border-radius: 10px;
    background-color: #666a6f;
}
</style>